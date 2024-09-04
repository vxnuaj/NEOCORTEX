```
import jax.numpy as jp
import jax.random as rdn
from termcolor import colored

class KMeans:

    def __init__(self, verbose=False, seed=0):
        self.verbose = verbose
        self.seed = seed
        self.__key = rdn.key(seed=self.seed)

    def cluster(self, X, n_clusters, kpp=False, max_iter=25):
        '''
        Cluster your dataset, `X`

        :param X: The unlabeled dataset.
        :type X: jax.numpy.ndarray
        :param n_clusters: The number of total clusters.
        :type n_clusters: int
        :param kpp: If True, use kmeans++. If False, default to random centroid initialization
        :type kpp: bool
        :param max_iter: Maximum number of iterations or 'auto' for convergence-based stopping
        :type max_iter: int or str
        '''
        self.X = X
        self.n_clusters = n_clusters
        self.kpp = kpp
        self.max_iter = max_iter
        self.centroids = None

        self._init_centroid()

        if isinstance(self.max_iter, int):
            for self.i in range(self.max_iter):
                converged = self._fit()
                if converged:
                    return
        elif self.max_iter == 'auto':
            self.i = 0
            while True:
                converged = self._fit()
                if converged:
                    return
                self.i += 1

    def _init_centroid(self):
        '''
        Initialize Centroids
        '''
        self.centroids = rdn.choice(key=self._rdn_key(), a=self.X, shape=(self.n_clusters,), replace=False, axis=0)
        distances = [] 
        cent_dict = {}

        for i, centroid in enumerate(self.centroids):
            distance = jp.linalg.norm(self.X - centroid, ord=2, axis=1)  # Distances are 1-dimensional of shape: (samples, )
            distances.append(distance)
        
        cent_idxs = jp.argmin(jp.array(distances), axis=0)
       
        for idx, sample in zip(cent_idxs, self.X):
            idx = int(idx) 
            if idx not in cent_dict:
                cent_dict[idx] = []
            cent_dict[idx].append(sample)

        self.cent_dict = cent_dict
        print(f"Iteration: {1} | Loss: {self._wcss()}")

    def _fit(self): 
        if self.max_iter == 'auto':
            for i in self.cent_dict.keys():
                centroid = jp.mean(jp.array(self.cent_dict[i]), axis=0)
                self.centroids = self.centroids.at[i].set(centroid)
            loss = self._wcss()
            print(f"Iteration: {self.i + 1} | Loss: {self._wcss()}")
            if self._eval_stop(loss):
                return True

        else:
            for i in self.cent_dict.keys():
                centroid = jp.mean(jp.array(self.cent_dict[i]), axis=0)
                self.centroids = self.centroids.at[i].set(centroid)

            loss = self._wcss()
            print(f"Iteration: {self.i + 1} | Loss: {self._wcss()}")
            if self._eval_stop(loss):
                return True

    def _wcss(self):
        '''
        Loss Function: WCSS (Within-Cluster Sum of Squares)
        '''
        distances = []
        for i, centroid in enumerate(self.centroids):
            sample = jp.array(self.cent_dict[i])
            distances.append(jp.sum(jp.square(jp.linalg.norm(sample - centroid, ord=2, axis=1))))

        loss = jp.sum(jp.array(distances))
        return loss

    def _eval_stop(self, loss):
        '''
        Evaluate Convergence
        '''
        n = 5

        try:
            self._loss_arr.append(int(loss))
        except:
            self._loss_arr = []
            self._loss_arr.append(int(loss))

        if len(self._loss_arr) >= 5 and len(set(self._loss_arr[-n:])) == 1:
            print(f'{colored("\nCONVERGED", "green", attrs=["bold"])} | Final Loss: {self._wcss()}')
            return True

    def _rdn_key(self):
        '''
        Generate a new random key
        '''
        return rdn.split(self.__key, num=1)[0]

```
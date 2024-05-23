> *Yann LeCun, Yoshua Bengio, & Geoffrey Hinton*

Deep Learning, computational models of multiple processing layers that process data of high complexity to learn it's complex representations

Used in object detection, speech recognition, drug discovery, genomics, and much more.

[[Convolutional Neural Networks]] have been able to bring breakthroughs in image processing, video, speech, and audio, while [[Recurrent Neural Networks]] shine on sequential data such as text and speech (EEG as well!)

>*CNNs, typically for spatial features whilst RNNs for temporal / sequential features*

Much of modern society is powered by machine learning, such as search engines, content filtering, and shopping recommendations to smartphones and cameras.

More traditional ML techniques were previously more limited to process natural data, as for decades it required precise engineering and domain expertise to properly design feature extraction pipelines for data processing.

Deep learning models, on the other hand, are capable of representation learning where they can be fed raw data without a need for data processing.

> *An big example can be EEG data, where traditionally, one would have to pre-process the data by filtering, normalizing, and epoching a signal to then extract the unique time-domain, frequency-domain features which would finally then be fed into a model through a combined feature vector.*
> 
> *Modern deep learning on the other hand, is able to learn features from raw EEG data without the need for extensive pre-processing.*

With the introduction of enough non-linear transformation, a model can essentially learn all the needed features from a data sample. The deeper a model is, the more complex features it can derive from, for example, an image.

The key aspect is that these models can learn these features on their own, with minimal intervention from a human engineer 

> *What's sick about these models are their applicability to complex tasks, where as models become increasingly accurate, they might be able to change the world.
> 
> "...predicting the activity of potential drug molecules, analyzing particle accelerator data, reconstructing brain circuits, and predicting the effects of mutations in non-coding DNA on gene expression."*

#### **Supervised Learning**

Supervised learning is the most common form of machine learning, where the data fed into a model is labeled with its category.

Essentially, a model is shown an image and produces an output in the form of a vector of the size of total categories or classes.

> *This is typically done through passing the raw weighted sum of a final layer through a [[Softmax]] activation function*

An objective function ([[Loss function]]) is used to gauge the total error between the prediction of a model and the true labels

> *In classification tasks, the objective function is typically [[Categorical Cross Entropy Loss]], where it's fed a [[One hot encoding]] of the true labels and the predicted probabilities of labels*

The objective function is then used as a guide to minimize the error of the model. To do so, a gradient is computed that's then used to update the weights

>*This is [[Backward propagation]] where the gradient of the loss is computed with respect to a specific parameters $\theta$ and [[Gradient descent]], where we want to find the optimal parameters of a model that find the global minima of the [[Loss function]] with respect to a param θ*

Traditional linear classifiers can be used to make predictions on a dataset but won't be able to detect subtle changes to, as an example, images very well without robust feature extraction.

A deeper model on the other hand will be able to get more specific representations of an image and learn from it, in order to compute more precise predictions without feature extraction. 

> *This form of representation learning is crucial for advanced applications.*

#### **Neural Networks and [[Backward propagation]]**

The training of a neural network involves a forward pass through multiple layers each involving the summation of linear combinations to get a weighted sum and an activation function applied to the weighted sum to introduce non-linearity.

This type of non-linearity allows for a model to capture more complex features within a given sample.

The forward pass, using matrix notation, is mathematically defined as:

$Z_l = W_l \cdot X + B_l$
$A_l = g(Z_l)$

where $Z$ is the matrix multiplication of a weighted matrix $W$ with input vector $X$ and the element-wise addition of a bias matrix $B$.

The activation function $g$, which may be Softmax, Tanh, ReLU, Sigmoid, or any other depending on the context, is applied to the weighted sum $Z$. In a traditional feed forward neural network, this process is repeated for all layers, $L$.

Once the final activation, $A_L$, is computed, a loss function, as an example [[Categorical Cross Entropy Loss]], is used to get the total loss or cost between the prediction and the true labels.

$CCE = \frac{1}{m} \sum Y \cdot \log{A_L}$, where $m$ is the total training samples per batch.

Let's assume we have a 2-layer neural network, applied to a multiclass classification task, where the loss function is [[Categorical Cross Entropy Loss]] and the activation function for the output layer is [[Softmax]]. 

The backpropagation takes the gradients as:

**Output Layer:**

$\frac{∂CCE}{∂Z_2} = (\frac{∂CCE}{∂A_2})(\frac{∂A_2}{∂Z_2}) = A_2 - Y$

$\frac{∂CCE}{∂W_2} = (\frac{∂CCE}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂W_2}) = (\frac{∂CCE}{∂Z_2})(\frac{∂Z_2}{∂W_2}) = (\frac{∂CCE}{∂Z_2})(A_1^T)$

$\frac{∂CCE}{∂B_2} = (\frac{∂CCE}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂B_2}) = \frac{∂CCE}{∂Z_2}$

**Hidden Layer:**

$\frac{∂CCE}{∂Z_1} = (\frac{∂CCE}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂$


---
**Thoughts / Questions / Action Items.**
- "*reconstructing brain circuits*", check out source 11 on the paper.
- when using sparse cross entropy given that you take in integer encoded labels, you'd take the argmax of the softmax activation and then use that as the parameter for the loss alongside the true labels. otherwise, then you wouldn't be able to learn, given that softmax outputs are from 0 to 1 and labels are from 0 to 9. this might've been why I couldn't implement sparse ce, right? will try this out if i get time.
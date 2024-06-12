Hyperparameter Tuning is the process of experimenting with the value of a set of hyperparameters in an attempt to find the optimal design for a neural network.

The means in which you optimize your hyperparameters can heavily vary per context 

>*(i.e., if you're using [[RMSprop]] or [[Adam]], or if you've introduced [[Learning Rate Decay]] or [[Cyclical* Momentum]] / [[Cyclical Learning Rate]])

though there are some general guidelines to do so:

1. The type of optimizer is key as most of your hyperparameters will depend on it.

2. Tuning your learning rate is important as most is dependent on it.

3. Afterwards, the mini-batch size and number of hidden units / layers can come into play into deciding how accurate or fast your neural network learns.

5. When the model is pre-trained you can gauge if you need to schedule your learning rate and by how much.

You can search a hyperparameter space using [[Grid Search]] or [[Random Search]]
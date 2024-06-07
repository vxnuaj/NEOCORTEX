A form of [[gradient descent]], which instead of processing an entire dataset at once (through vectorization), it processes the dataset with a mini-batch size of a simple sample.

The downside to this is it essentially takes up too much time, taking away the speed benefits of introducing vectorization as you process data a single sample at a time.

What works better is [[Mini-Batch Gradient Descent]]
#hardware

A TPU is an AI accelerator [[ASIC]] designed by Google for accelerating the training of their deep learning architectures using their proprietary [[Tensorflow]] software.

TPUs train models more efficiently as they use hardware that's specifically designed for performing large matrix operations found in deep learning algorithms.

##### How they work:

Now a [[TPU]] is a matrix processor that's hyper-specialized for deep learning workloads. They can't run word processors, run rocket engines, or bank transactions but are specifically made for matrix operations at fast speeds. 

They contain thousands of [[multiply-accumulators]] that are connected to each other to form a [[systolic array]] that can perform operations in parallel.

A TPU host streams the data onto an infeed queue which then loads data onto the TPU and stores it into the HBM memory. The data is sent through the [[systolic array]] to perform the needed computations and the output is loaded into the outfeed queue which is then read by the host and stored onto the host's memory.

For example, in the context of matrix multiplications:

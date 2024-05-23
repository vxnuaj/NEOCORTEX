> *Yann LeCun, Yoshua Bengio, & Geoffrey Hinton*

Deep Learning, computational models of multiple processing layers that process data of high complexity to learn it's complex representations

Used in object detection, speech recognition, drug discovery, genomics, and much more.

[[Convolutional Neural Networks]] have been able to bring breakthroughs in image processing, video, speech, and audio, while [[Recurrent Neural Networks]] shine on sequential data such as text and speech (EEG as well!)

>CNNs, typically for spatial features whilst RNNs for temporal / sequential features

Much of modern society is powered by machine learning, such as search engines, content filtering, and shopping recommendations to smartphones and cameras.

More traditional ML techniques were previously more limited to process natural data, as for decades it required precise engineering and domain expertise to properly design feature extraction pipelines for data processing.

Deep learning models, on the other hand, are capable of representation learning where they can be fed raw data without a need for data processing.

> An big example can be EEG data, where traditionally, one would have to pre-process the data by filtering, normalizing, and epoching a signal to then extract the unique time-domain, frequency-domain features which would finally then be fed into a model through a combined feature vector.
> 
> Modern deep learning on the other hand, is able to learn features from raw EEG data without the need for extensive pre-processing.

With the introduction of enough non-linear transformation, a model can essentially learn all the needed features from a data sample. The deeper a model is, the more complex features it can derive from, for example,.
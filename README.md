# TLift

This MATLAB/Octave code is proposed in our paper [1]. To explore the prior spatial-temporal structure of a camera network, a model-free temporal cooccurrence based score weighting method is proposed, which we call Temporal Lifting (TLift). This is computed on the fly for each query image, without statistical learning of a transition time model in advance. Therefore, it does not require training data, and can be readily applied by many person re-identification methods.

The code is tested in Octave 4.2.2. For usage please read the help in the TLift function. Usually, images in person re-identification databases are named with frame numbers. This code uses time stamps in seconds, which can be obtained by dividing frame numbers with the FPS.

# Reference:
[1] Shengcai Liao and Ling Shao, "Interpretable and Generalizable Deep Image Matching with Adaptive Convolutions." In arXiv preprint, arXiv:1904.10424, 2019.

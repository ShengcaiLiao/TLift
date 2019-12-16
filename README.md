# TLift

This code is proposed in our paper [1]. The code includes both python and MATLAB/Octave impelmentations. 
The MATLAB/Octave impelmentation is tested in Octave 4.2.2. 

To explore the prior spatial-temporal structure of a camera network, a model-free temporal cooccurrence based score 
weighting method is proposed, which we call Temporal Lifting (TLift). This is computed on the fly for each query image, 
without statistical learning of a transition time model in advance. Therefore, it does not require training data, and 
can be readily applied by many person re-identification methods.

For usage please read the help in the TLift function. Usually, images in person re-identification databases are named 
with frame numbers. This code uses time stamps in seconds, which can be obtained by dividing frame numbers with the FPS.

The DukeMTMC-reID dataset has a good global and continuous record of frame numbers, and it is synchronized by providing 
offset times. In contrast, the Market-1501 dataset only has independent frame numbers for each session of videos from 
each camera. For several sessions from each camera, we roughly calculated the overall time frames of each session as 
offset, and made a cumulative record by assuming the video sessions were continuously recorded. After that, frame 
numbers were converted to seconds in time by dividing the Frames Per Second (FPS) in video records, where FPS=59.94 
for the DukeMTMC-reID dataset and FPS=25 for the Market-1501 dataset.

Default parameters are K = tau = sigma = 100, and alpha = 0.1.


# Reference:
[1] Shengcai Liao and Ling Shao, "Interpretable and Generalizable Person Re-identification with Query-adaptive Convolution and Temporal Lifting." In arXiv preprint, arXiv:1904.10424, 2019.

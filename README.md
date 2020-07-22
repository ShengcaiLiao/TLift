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

Default parameters are tau=100, sigma=200, K=10, and alpha=0.2. They are not sensitive in a broad range, as analyzed in the Appendix of our paper [1].


# Citation
[1] Shengcai Liao and Ling Shao, "Interpretable and Generalizable Person Re-Identification with Query-Adaptive Convolution and Temporal Lifting." In the 16th European Conference on Computer Vision (ECCV), 23-28 August, 2020.

@inproceedings{Liao-ECCV2020-QAConv,  
  title={{Interpretable and Generalizable Person Re-Identification with Query-Adaptive Convolution and Temporal Lifting}},  
  author={Wen, Yandong and Zhang, Kaipeng and Li, Zhifeng and Qiao, Yu},  
  booktitle={European conference on computer vision (ECCV)},  
  year={2020}  
}

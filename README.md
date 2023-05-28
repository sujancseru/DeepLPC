# DeepLPC: A deep learning approach to augmented Kalman filter-based single-channel speech enhancement

DeepLPC is a Deep Learning framework proposed in [[1]](https://ieeexplore.ieee.org/document/9411829)[DeepLPC.pdf](https://github.com/sujancseru/DeepLPC/files/11584544/DeepLPC.pdf)


Introduction:
1. LPC is a key parameter for speech coding, speech recognition, and speech enhancement using Kalman Filter. However, in noisy conditions the accuracy of LPC estimates become deteriorate and degrades the performance of speech processing systems requireing accurate LPCs.
2. DeepLPC is a Deep Learning framework for accurately estimating the LPC parameters in noisy condition. 
3. The accurate estimates of LPC are used in designining Augmented Kalman Filter for Speech Enhancement as shown in Fig. 1.

Key Contributions: 

1. Develop a new deep learning framework, namely DeepLPC within the residual network and temporal network (ResNet-TCN). 
2. DeepLPC learns a mapping from the noisy speech LPC power spectra to the clean speech and noise LPC power spectra from where the corresponding LPC parameters are computed. 
3. By producing less biased clean speech and noise LPC estimates, DeepLPC enables the AKF to produce enhanced speech at a higher quality and intelligibility in real-life noise conditions.

Implementation: 
1. DeepLPC utilize ResNet-TCN as used in [Deep Xi](https://github.com/anicolson/DeepXi).
2. In DeepLPC, ResNet-TCN learns a mapping from the noisy speech LPC power spectra to the clean speech and noise LPC power spectra from where the corresponding LPC parameters are computed.
3. To facilated the convergency of the gradient optimization algorith, it is necessary to generate normalized training target. It was shwon in [[1]](https://ieeexplore.ieee.org/document/9411829) that the log LPC power spectra of clean speech and noise signal can be fitten with Gaussian Distribution. Therefore, the Gaussian CDF has been used to normalize the log LPC power spectra. 

![fig1](https://github.com/sujancseru/DeepLPC/assets/130210435/483d4468-29f4-4621-88c1-4fd9dcf6ef71)

[1] [S. K. Roy, A. Nicolson, and K. K. Paliwal, "DeepLPC: A Deep Learning Approach to Augmented Kalman Filter-Based Single-Channel Speech Enhancement," in IEEE Access, vol. 9, pp. 64524-64538, 2021, doi: 10.1109/ACCESS.2021.3075209.](https://ieeexplore.ieee.org/document/9411829)


# Water-Net-flood-extraction-network-combining-Transformer-and-CNN-from-SAR
# requirement：
- python 3.7.12
- TensorFlow 2.6.4
- gdal 3.1.4
- numpy 1.19.0
- opencv-python 4.5.4
- matplotlib 3.5.3
# Training data and model parameters
- https://www.kaggle.com/zhaotengsir/datasets?search=0.779
# **Abstract:**


   Due to the trend of high frequency and wide range of flood disasters in China and the advantage that synthetic aperture radar (SAR) images 
are not restricted by climatic conditions, it is of great significance to extract flood from SAR images for flood monitoring. Method Aiming 
at problems of over-segmentation and water boundary positioning in SAR image flood extraction, this paper designs a Multi-Scale Aggregation 
Model by combining the local inductive bias ability of CNN and the global semantic capture ability of transformer to fuse multi-scale semantic 
features and strengthen the global semantic features, and then proposes a new deep neural network, Water-Net which has an asymmetric encoder-decoder
structure for flood extraction. Firstly, The Sentinel-1 Dual-Polarized Water Index (SDWI) is introduced into the network, along with VV, VH bands, 
to draw the rich spectral features of SAR images; Then, in the network’s encoder part, the EfficientNet-B0 Module which achieved state-of-the-art 
accuracy in image classification is used to acquire abundant semantic features; Composed of convolution and Swin Transformer, the Multi-Scale Aggregation 
Module is added to the network’s decoder part for deep mining of multi-scale and global semantic features, and then the CBAM is added to gather important
features while repressing invalid features. Result Experimental results on two public flood datasets show that, compared with other mainstream segmentation
networks based on pure CNN or transformer structure, such as U-Net, HRNet, Swin-Unet, etc, the proposed Water-Net network achieves 87.6% and 91.1% F1 score 
respectively while surpassing the U-net by 2.7% and 2.8%, 77.9% and 83.7% mean Intersection over Union (IOU) respectively while surpassing the U-net by 4.1% 
and 4.6%. Conclusion This paper proposes a flood extraction network, Water Net, integrating CNN and transformer, can performs well in terms of completeness 
and connectivity of flood extraction by ingeniously designing each part of the network.

**this paper's code will be upload here soon!**
# model：
### Overall architecture of the model is below：
![our_model.png](https://s2.loli.net/2022/11/27/9CLhqd5PlufB7Je.png)
### MSAM is below：
![image.png](https://s2.loli.net/2022/11/27/SoCJMRhluZVQEg7.png)

# experiment：
![image.png](https://s2.loli.net/2022/11/27/yV1B3aGcRqJn5ZD.png)
![image.png](https://s2.loli.net/2022/11/27/wTqbLSe9tizFkMu.png)
![image.png](https://s2.loli.net/2022/11/27/WbezTx3U2sOX6oq.png)

Note: Speed is defined as: processing single sheet 512 × Time required for 512 size images (seconds)


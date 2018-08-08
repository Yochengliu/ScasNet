Semantic Labeling in VHR Images via A ScasNet
===
by Yongcheng Liu, Bin Fan, Lingfeng Wang, Shiming Xiang, Chunhong Pan.  

## VGG ScasNet
The encoder is based on VGG-Net variant (Chen et al., 2015), which is to obtain finer feature maps (about 1/8 of input size rather than 1/32). On the last layer of encoder, multi-scale contexts are captured by dilated convolutional operations with dilation rates of 24, 18, 12, 6. As a trade-off, we only choose three shallow layers for refinement. Moreover, BN layer is not used in VGG ScasNet.    

## ResNet ScasNet
The configuration of ResNet ScasNet is almost the same as VGG ScasNet, except for four aspects: the encoder is based on ResNet variant (Zhao et al., 2016), four shallow layers are used for refinement, seven residual correction schemes are designed for feature fusions and BN layer is used.  

## Finetuned Models
###For initializing the encoder part in ScasNet    
The encoder in VGG ScasNet is finetuned by [VGG-Net_variant_caffemodel](http://liangchiehchen.com/projects/DeepLabv2_vgg.html)   
The encoder in ResNet ScasNet is finetuned by [ResNet_variant_caffemodel](https://drive.google.com/open?id=0BzaU285cX7TCNVhETE5vVUdMYk0)  

## Caffe Framework
The Caffe Framework we used to train VGG ScasNet is released on [DeepLab_v2](https://bitbucket.org/aquariusjay/deeplab-public-ver2).   

The Caffe Framework we used to train ResNet	ScasNet is released on [PSPNet](https://github.com/hszhao/PSPNet).      
### Installation
Please follow the instructions of [Caffe](https://github.com/BVLC/caffe), [DeepLab_v2](https://bitbucket.org/aquariusjay/deeplab-public-ver2) and [PSPNet](https://github.com/hszhao/PSPNet).  

The code has been tested successfully on Ubuntu 14.04 with CUDA 8.0.    

## References

Chen, L., Papandreou, G., Kokkinos, I., Murphy, K., Yuille, A. L., 2015. Semantic image segmentation with deep convolutional nets and fully connected crfs. In: International Conference on Learning Representations.
     
     
Zhao, H., Shi, J., Qi, X., Wang, X., Jia, J., 2016. Pyramid scene parsing network. arXiv preprint arXiv:1612.01105.

## Citation
We would be very glad if ScasNet is helpful for your research, and please consider cite our paper:

## Contact
We would be very glad if you have some ideas or questions about ScasNet to share with us, please contact <yongcheng.liu@nlpr.ia.ac.cn>

Semantic Labeling in VHR Images via A Self-Cascaded CNN (ScasNet)
===
by [Yongcheng Liu](https://yochengliu.github.io/), [Bin Fan*](http://www.nlpr.ia.ac.cn/fanbin/), [Lingfeng Wang](https://scholar.google.com/citations?user=PaRak2AAAAAJ&hl=en), [Jun Bai](https://www.researchgate.net/profile/Jun_Bai), [Shiming Xiang](https://scholar.google.com/citations?user=0ggsACEAAAAJ&hl=zh-CN), [Chunhong Pan](https://www.researchgate.net/lab/Chunhong-Pan-Lab).  

[vai]: ./images/vai.jpg
![vai]

## ScasNet

#### VGG ScasNet

- The encoder is based on VGG-Net variant (Chen et al., 2015), which is to obtain finer feature maps (about 1/8 of input size rather than 1/32).
- On the last layer of encoder, multi-scale contexts are captured by dilated convolutional operations with dilation rates of 24, 18, 12, 6.
- As a trade-off, we only choose three shallow layers for refinement. Moreover, BN layer is not used in VGG ScasNet.    

#### ResNet ScasNet

The configuration of ResNet ScasNet is almost the same as VGG ScasNet, except for four aspects: 

- the encoder is based on ResNet variant (Zhao et al., 2016) 
- four shallow layers are used for refinement 
- seven residual correction schemes are designed for feature fusions
- BN layer is used.  

## Finetuning

#### For initializing the encoder part in ScasNet
    
- The encoder in VGG ScasNet is finetuned with [VGG-Net_variant_caffemodel](http://liangchiehchen.com/projects/DeepLabv2_vgg.html)
   
- The encoder in ResNet ScasNet is finetuned with [ResNet_variant_caffemodel](https://drive.google.com/open?id=0BzaU285cX7TCNVhETE5vVUdMYk0)  

## Caffe

- The Caffe we used to train VGG ScasNet is released on [DeepLab_v2](https://bitbucket.org/aquariusjay/deeplab-public-ver2).
   
- The Caffe we used to train ResNet	ScasNet is released on [PSPNet](https://github.com/hszhao/PSPNet).
      
#### Installation

Please follow the instructions of [Caffe](https://github.com/BVLC/caffe), [DeepLab_v2](https://bitbucket.org/aquariusjay/deeplab-public-ver2) and [PSPNet](https://github.com/hszhao/PSPNet).  

The code has been tested successfully on Ubuntu 14.04 with CUDA 8.0.    

## References
1. Chen, L., Papandreou, G., Kokkinos, I., Murphy, K., Yuille, A. L., 2015. Semantic image segmentation with deep convolutional nets and fully connected crfs. In: International Conference on Learning Representations.   
2. Zhao, H., Shi, J., Qi, X., Wang, X., Jia, J., 2016. Pyramid scene parsing network. arXiv preprint arXiv:1612.01105.

## Citation

We would be very glad if ScasNet is helpful for your research, and please consider citing our paper ([arXiv](https://arxiv.org/abs/1807.11236)):   

        @article{liu2018scasnet,   
          author = {Yongcheng Liu and    
                    Bin Fan and    
                    Lingfeng Wang and   
                    Jun Bai and   
                    Shiming Xiang and   
                    Chunhong Pan},   
          title = {Semantic Labeling in Very High Resolution Images via A Self-Cascaded Convolutional Neural Network},   
          journal = {ISPRS J. Photogram. and Remote Sensing.},   
          volume = {145},  
          pages = {78--95},  
          year = {2018}   
        }   

## Contact

We would be very glad if you have some ideas or questions about ScasNet to share with us, please contact <yongcheng.liu@nlpr.ia.ac.cn>

An Effective Cloud Detection Method for Gaofen-5 Images via Deep Learning
===================================================================

Recent developments in hyperspectral satellites have dramatically promoted the wide application of large-scale quantitative remote sensing. As an essential part of preprocessing, cloud detection is of great significance for subsequent quantitative analysis. For Gaofen-5 (GF-5) data producers, the daily cloud detection of hundreds of scenes is a challenging task. Traditional cloud detection methods cannot meet the strict demands of large-scale data production, especially for GF-5 satellites, which have massive data volumes. Deep learning technology, however, is able to perform cloud detection efficiently for massive repositories of satellite data and can even dramatically speed up processing by utilizing thumbnails. Inspired by the outstanding learning capability of convolutional neural networks (CNNs) for feature extraction, we propose a new dual-branch CNN architecture for cloud segmentation for GF-5 preview RGB images, termed a multiscale fusion gated network (MFGNet), which introduces pyramid pooling attention and spatial attention to extract both shallow and deep information. In addition, a new gated multilevel feature fusion module is also employed to fuse features at different depths and scales to generate pixelwise cloud segmentation results. The proposed model is extensively trained on hundreds of globally distributed GF-5 satellite images and compared with current mainstream CNN-based detection networks. The experimental results indicate that our proposed method has a higher F1 score (0.94) and fewer parameters (7.83 M) than the compared methods.


[[Paper]](https://www.mdpi.com/2072-4292/12/13/2106/htm)
[[Code]](https://github.com/JunchuanYu/MFGNet_Cloud_Detection_Remote_Sensing)

<hr>

<div align=center><img src="./Figure/architecture.jpg?raw=True" width="800" > </div>

####  <center> Architecture of MFGNet

<hr>

#### Dependencies
- Tensorflow==1.13.1
- Keras==2.2.4
- Gdal==2.4.1

<hr>

Specifics of the learning algorithm
-----------------------------------

The following are the details of the learning algorithm used:

* Parameter update algorithm used: [Adagrad](http://www.jmlr.org/papers/volume12/duchi11a/duchi11a.pdf)
	* Batch size: 200
	* Learning rate: 0.01

* Number of steps: until best validation performance
<hr>

#### CASIA-SURF validation score (ACER)


| Single-modal Model                 | Color  | Depth  | ir     |
| --------------------- | ------ | ------ | ------ |
| FaceBagNet            | 0.0672 | 0.0036 | 0.1003 |
| ConvMixer             | 0.0311 | 0.0025 | 0.1073 |
| MLPMixer              | 0.0584 | 0.0010 | 0.2382 |
| VisionPermutator(ViP) | 0.0570 | 0.0304 | 0.2571 |
| VisonTransformer(ViT) | 0.0683 | 0.0036 | 0.2799 |

| Multi-modal Model         | patch size 32 | patch size 48 | patch size 64 |
| ----------------- | ------------- | ------------- | ------------- |
| FaceBagNetFusion  | 0.0009        | 0.0006        | 0.0007        |
| ViTFusion         | 0.0169        | 0.0778        | 0.0375        |
<hr>

## Citation
If you find this work or code is helpful in your research, please cite:
```
Yu, J.; Li, Y.; Zheng, X.; Zhong, Y.; He, P. An Effective Cloud Detection Method for Gaofen-5 Images via Deep Learning. Remote Sens. 2020, 12, 2106. https://doi.org/10.3390/rs12132106
```
#### Bibtex:
```
@Article{rs12132106,
AUTHOR = {Yu, Junchuan and Li, Yichuan and Zheng, Xiangxiang and Zhong, Yufeng and He, Peng},
TITLE = {An Effective Cloud Detection Method for Gaofen-5 Images via Deep Learning},
JOURNAL = {Remote Sensing},
VOLUME = {12},
YEAR = {2020},
NUMBER = {13},
ARTICLE-NUMBER = {2106},
URL = {https://www.mdpi.com/2072-4292/12/13/2106},
ISSN = {2072-4292},
DOI = {10.3390/rs12132106}
}
```
<hr>

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
<hr>

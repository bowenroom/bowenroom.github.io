---
layout: post
title: Semantic Representation Fusion-Based Network for Robust Land Cover Classification in Foggy Conditions
date: 2023-10-19 5:38:28.000000000 +09:00
categories: bowenroom
tags: paper
---
**Weipeng Shi, Wenhu Qin<sup>*</sup>, Zhonghua Yun, Chao Wu, Yukun Yang, and Tao Zhao**
<div style="text-align:center;">
  <img src="https://s2.loli.net/2023/11/11/N5XiEebTSd4YM7a.png" width="300" height="280" style="display: inline-block; vertical-align: middle;">
</div>


# Abstract
![Static Badge](https://img.shields.io/badge/NJLCC2022-passing-brightgreen)
![Static Badge](https://img.shields.io/badge/Latest_Date-20230228-violet)
![Static Badge](https://img.shields.io/badge/Progress-40%25-blue)
[![license](https://img.shields.io/github/license/open-mmlab/mmsegmentation.svg)](https://github.com/open-mmlab/mmsegmentation/blob/main/LICENSE)
[![open issues](https://isitmaintained.com/badge/open/open-mmlab/mmsegmentation.svg)](https://github.com/bowenroom/bowenroom.github.io/issues) 




The existing land cover classification dataset are collected under clear weather conditions. In practical applications, adverse climate conditions can significantly impact the model's classification performance. However, the existing datasets, while suitable for model training and accuracy testing, are inadequate for evaluating classification robustness under adverse weather conditions like haze and fog. Consequently, when models trained on clean remote sensing images perform well on test datasets, the frequent occurrence of fog in real-world scenarios can severely interfere with the quality of remote sensing images, leading to reduced model classification accuracy and poor generalization. Therefore, this study collected remote sensing data in Nanjing under both sunny and foggy conditions using drones and named the dataset NJLCC2022 (NanJing Land Cover Classification in 2022). This approach helps: 
-  better assess the degradation in model classification performance under foggy conditions compared to clean conditions.
- investigate the commonalities in visual representations in remote sensing images under foggy conditions, thereby designing models with strong robustness.
- use real remote sensing data from both clear and foggy conditions to enhance model transfer learning.

# Dataset 
## Description
This dataset was collected using the DJI Mavic 3 drone for remote sensing imagery. The optical imagery primarily includes three spectral bands: red, green, and blue. The drone flew at an altitude of 200 meters, with a ground sampling distance of 4 cm/pixel. As of April 1, 2023, this dataset contains a total of 22 orthorectified images. Among these, 9 images were affected by fog, while the remaining 13 were acquired under clear sky conditions. The average resolution of the images is 9000×9000 pixels. In order to reduce model bias and to compare land cover differences between urban and rural areas, the sampling locations of the 22 images are scattered between the urban area (Xuanwu District) and rural area (Jiangning District) of Nanjing, Jiangsu Province. The NJLCC2022 dataset includes annotations for 5 classes of objects, namely Clutter Background, Car, Playground, Water, and Building. Each class is annotated with a different color: `Clutter Background (RGB: 0, 0, 0), Car (RGB: 0, 128, 0), Playground (RGB: 128, 0, 128), Water (RGB: 0, 0, 128), and Building (RGB: 128, 0, 0)`.
## Details
### Locations and Data Collection Dates

| Sample ID | Collection Date | Fog Type | Longitude | Latitude |
|-----------|-----------------|----------|-----------|----------|
| ortho1    | 2023-02-06      | Thick     | 118.818251| 32.064312|
| ortho2    | 2023-02-06      | Thick     | 118.823017| 32.065051|
| ortho3    | 2023-02-06      | Thick     | 118.816626| 32.066614|
| ortho4    | 2022-11-03      | Clear     | 118.809120| 32.054298|
| ortho5    | 2022-12-07      | Moderate  | 118.819967| 32.072009|
| ortho6    | 2022-12-09      | Thin      | 118.825302| 32.072846|
| ortho7    | 2022-12-07      | Moderate  | 118.861529| 31.914914|
| ortho8    | 2022-12-09      | Thin      | 118.869680| 31.925127|
| ortho9    | 2022-12-09      | Thin     | 118.870319| 31.915301|
| ortho10   | 2022-12-07      | Moderate  | 118.874873| 31.914486|
| ortho11   | 2022-10-11      | Clear | 118.801179| 32.069022|
| ortho12   | 2022-12-13      | Clear | 118.805841| 32.058883|
| ortho15   | 2022-12-15      | Clear | 118.793864| 32.060306|
| ortho16   | 2022-12-15      | Clear | 118.783131| 32.068561|
| ortho17   | 2022-12-19      | Clear | 118.779321| 32.062508|
| ortho18   | 2022-12-22      | Clear | 118.784110| 32.066938|
| ortho19   | 2022-12-17      | Clear | 118.795185| 32.056631|
| ortho20   | 2022-12-17      | Clear | 118.798349| 32.058409|
| ortho21   | 2022-12-22      | Clear | 118.799249| 32.054417|
| ortho22   | 2023-01-06      | Clear | 118.788154| 32.058070|
| ortho25   | 2022-10-18      | Clear | 118.795385| 32.063230|
| ortho26   | 2022-10-19      | Clear | 118.813055| 32.057664|

### Location Map
![](https://s2.loli.net/2023/11/12/CSVOQIgz65kvdmT.png)
# Images
## Annotation
![](https://s2.loli.net/2023/11/12/N3Ons2gcFrqfvEp.png)
## Samples
![](https://s2.loli.net/2023/11/12/tmJ2AlSHzT5nUPv.png)

# Download
# Citation
```
@article{shiSemanticRepresentationFusionBased2023,
  title = {Semantic {{Representation Fusion-Based Network}} for {{Robust Land Cover Classification}} in {{Foggy Conditions}}},
  author = {Shi, Weipeng and Qin, Wenhu and Yun, Zhonghua and Wu, Chao and Yang, Yukun and Zhao, Tao},
  year = {2023},
  journal = {IEEE Transactions on Geoscience and Remote Sensing},
  volume = {61},
  pages = {1--16},
  issn = {1558-0644},
  doi = {10.1109/TGRS.2023.3280158}
}

```
# Contact
`E-mail: qinwenhu@seu.edu.cn,bowenroom1@gmail.com`


 

 




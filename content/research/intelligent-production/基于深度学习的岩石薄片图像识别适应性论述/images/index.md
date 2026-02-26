---
title: "基于深度学习的岩石薄片图像识别适应性论述"
date: 2022-07-14
categories: 
  - "分享推荐"
coverImage: "1.png"
---

[https://blog.csdn.net/weixin\_45638544/article/details/124580781](https://blog.csdn.net/weixin_45638544/article/details/124580781)

# 基于深度学习的岩石薄片图像识别适应性论述

**摘要**

当前油藏地质相关领域对岩石薄片的分析提出更细粒度的要求，一方面探索岩石的大尺度识别，另一方面分析像素级的识别与分割的任务。尽管深度学习领域各类算法层出不穷，但研究的主要领域集中到人像和大尺度物体，更多的研究以无人驾驶为契机，探索车辆的语义问题。然而这与油气田地质工程一体化的专业需求存在矛盾。因此，本文尝试从模型适应性方面论证当前的主要模型存在的特点和局限性，并探索通用神经网络在专业领域结合的可能性。

# 一、传统方法的总结与剖析

## 1.1 Mask R-CNN背景与改进点

目前Mask R-CNN\[1-3\]与2017年从Faster R-CNN模型的基础上提出的新型分割模型，该模型将特征提取器同时关注于目标检测、目标分类和像素级分割。该模型在Faster R-CNN的结构基础上加上了Mask预测分支，并且改良了ROI Pooling结构，形成ROI Align。 ![在这里插入图片描述](images/3d2c9007098a4c158616899eb1e98ae7.png#pic_center)

图1 Mask R-CNN改进点

## 1.2 Mask R-CNN的优缺点分析

优势方面：Mask R-CNN引入了Mask-Head头掩码结构增强模型的预测效果，实现了像素级别的分割掩膜预测，取得了良好的效果；用ROI Align替代了ROI Pooling，去除了RoI Pooling的粗量化，使得提取的特征与输入良好对齐。 劣势方面：该模型的评价函数同时共享了分类框与预测掩膜，在低时间复杂度的基础上对模型预测性能造成了一定的影响；这一局限性在后期的Mask Scoring R-CNN给予了一定的补偿。尽管如此，改进后的模型采用ResNet骨干网络，并打匹配了多种Head头结构完成各类任务的信息增强，因此仍然具有过大的网络结构。

# 二、新方法的讨论与展望

## 2.1 Squeeze Excitation & Pyramid Scene Parsing适应性分析

论文提出在场景分割是，大多数的模型会使用FCN的架构，但是FCN在场景之间的关系和全局信息的处理能力存在问题，其典型问题有：1.上下文推断能力不强；2.标签之间的关系处理不好；3.模型可能会忽略小的东西。 有研究指出\[4\]，岩石薄片的小尺度颗粒细节需要更多的通道间注意力。因此Squeeze Excitation块通过自适应全局平均池化方法对通道维度的信息进行激活。SE块更是具有即插即用特性，因此可以嵌入到其他模型结构中。 ![在这里插入图片描述](images/7287a75ba73348b9b424c01072d647d2.png#pic_center)

图2 SE即插即用块

与此同时，因为薄片具有尺寸小、全局相似性高的特点常采用子区域划分方法。因此Pyramid模型的多尺度信息可以纳入考虑。通过同和不同层级的尺度信息，来捕捉整个岩石薄片的赤化特征，同时在全局特征权重角度，可以考虑嵌入SE块进行Rescale计算。经过全局和局部的特性标定，可以更大幅度的提升网络的性能。

图3 Pyramid end2end分割模型  

# 参考文献

_\[1\] ZYUZIN V, RONKIN M, PORSHNEV S, et al. Automatic Asbestos Control Using Deep Learning Based Computer Vision System\[J\]. APPLIED SCIENCES-BASEL, 2021,11(22). \[2\] LEE K B, SHIN H S, HONG S C, et al. Identification of Targeted Regions on an Analogue Site of the Moon by Using Deep Learning Segmentation Algorithm: EARTH AND SPACE 2021: SPACE EXPLORATION, UTILIZATION, ENGINEERING, AND CONSTRUCTION IN EXTREME ENVIRONMENTS\[Z\]. VANSUSANTE P J, ROBERTS A D. 17th Biennial International Conference on Engineering, Science, Construction, and Operations in Challenging Environments (Earth and Space): 20211037-1046. \[3\] HUANG H, LUO J, TUTUMLUER E, et al. Automated Segmentation and Morphological Analyses of Stockpile Aggregate Images using Deep Convolutional Neural Networks\[J\]. TRANSPORTATION RESEARCH RECORD, 2020,2674(10): 285-298. \[4\] MA H, HAN G, PENG L, et al. Rock thin sections identification based on improved squeeze-and-Excitation Networks model\[J\]. COMPUTERS & GEOSCIENCES, 2021,152._

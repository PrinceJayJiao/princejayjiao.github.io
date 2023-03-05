---
title: transforms
date: 2023-03-05 14:08:17
tags: ['pytorch','transforms']
---

# pytorch深度学习笔记（一）--transforms

## 介绍

​	torchvision.transforms模块主要用于对图像进行转换等一系列预处理操作，其主要目的就是对图像数据进行增强，进而提高模型的泛化能力。对图像预处理操作主要有数据中心化、缩放、裁剪、旋转、翻转、填充、添加噪声、灰度变换、线性变换、仿射变换、亮度、饱和度、对比变换等等。

## 导入transforms

常见的代码模型如下：

```python
from torchvision import transforms
preprocess = transforms.Compose([
    transforms.Resize(256),
    transforms.CenterCrop(224),
    transforms.ToTensor(),
    transforms.Normalize(
        mean=[0.485,0.456,0.406],
        std=[0.229,0.224,0.225]
    )
])
```

## transforms.Compose

​	这个方法是将一系列的图像转换函数进行组合，能够按照组合的顺序依次对图像进行处理操作。示例代码如上面的代码块所示。

## transforms常用方法

### transforms.ToTensor()

​	作用是将一个PIL Image格式的图片或者是取值范围为[0,255]，形状为[H,W,C]的numpy.ndarray数组转换为取值范围为[0.0,1.0],形状为[C,H,W]的tensor

### transform.RandomCrop(size)

​	依据给定的size随即裁剪，size可以为sequence 或者int

1. size is sequence 裁剪后图像为 (h,w)

2. size is int ,裁剪后图像为（size,size)

### Transforms.Resize(size)

重置图像分辨率

1. size is int 图像就会被转化为(size*height/width,size)
2. size 为h w,图像就会转为h w

### Transforms.Normalize

​	对数据按通道进行标准化，即先减去均值，再除以标准差。

常见代码如下

```python
transforms.Normalize([
    mean = [0.485,0.456,0.406],
    std = [0.229,0.224,0.225]
])
```




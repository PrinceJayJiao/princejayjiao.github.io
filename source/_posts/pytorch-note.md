---
title: pytorch-note
date: 2023-03-05 13:50:22
tag: ['pytorch']
---



## pytorch

## pytorch 常用import

1. import torch
2. from torch import nn
3. from torchvision import models

## torchvision中常见models

1. AlexNet
2. ResNet



## pillow

这是一个图像操作模块

### 使用

```python
from PIL import Image
img = Image.open('./booby.png')
```



## tensor

pytorch中基本的数据单元：张量

### 创建张量的方法

1. torch.ones(size)

创建一个大小为size的，数据均为1.0 的张量

2. torch.zeros(size)

创建一个大小为size的，数据均为0.0 的张量

3. torch.tensor(list)

以python list为输入创建一个张量

### 张量命名




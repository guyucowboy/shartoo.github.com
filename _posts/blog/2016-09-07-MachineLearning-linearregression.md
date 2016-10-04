---
layout:     post
title:      机器学习笔记：线性回归和牛顿下降法
category: blog
description: 斯坦福大学公开课-机器学习笔记
---

## 案例

 根据房子的数据预测房价。
 样本数: 47
 数据示例如下:

 |面积|卧室数|...|售价(万美元)|
 |---|---|---|---|
 |210.4|4|...|400|
 |120.5|3|...|22-|
 |....|...|...|...|

 ## 课程之前需要明白的符号定义

 + $m$ : 训练样本数，此案例中为 47
 + $x$: 输入变量，或者特征。此案例中房子各项指标数据
 + $y$: 目标变量。此案例中为房子售价
 + $(x,y)$ : 表示一个训练样本，其中x为特征，y为目标变量。
 + $x^{(i),y^{i}}$:为第$i$个训练样本，或表格中第$i$行数据。
 + $\theta$: 参数。学习算法的任务就是找到合适的参数

 对于我们的案例数据
  + $x$  : 输入数据，假设每个房子有2个指标，分别为房屋面积，卧室数。
    + $x_1$: 房子大小
    + $x_2$: 卧室数
    + $h(x)=h_{\theta}(x)=\theta_0+\theta_1x_1+\theta_2x_2$ 若令 $x_0=1$则$h(x)=\sum_{i=1}^{2}\theta_ix_i=\theta^Tx$
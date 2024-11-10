---
aliases:
  - 有源滤波器
tags:
  - analog
  - 这个ppt做得真棒大赏
---
# 传递函数（一点基础）

一个传递函数基本长这样：$$T(s)=\frac{P(s)}{Q(s)}=b_0\frac{(s-z_1)(s-z_2)(s-z_3)\cdots(s-z_n)}{(s-\lambda_1)(s-\lambda_2)(s-\lambda_3)\cdots(s-\lambda_n)}$$
在上式中$P(s)$为极点（Pole），$Q(s)$为零点（Zero）

在一个特定值$s=p$时，这个传递函数的值就是把$p$带进去算

如果用零极点图的参数来表示传递函数的值：$$\left|T(p)\right|=b_0\frac{\text{Product of distances of zeros to }p}{\text{Product of distances of poles to }p}$$$$\angle T(p)=\text{sum of zero angles to }p\ -\ \text{sum of pole angles to }p$$
反正学过信号与系统的应该很熟这个

系统的频率响应是通过在零极点图中沿着$y$轴分析得到的。

## 极点的影响

频率响应的幅度在极点$p$附近增强，相位减小

## 零点的影响

频率响应的幅度在零点$p$附近减弱，相位增加

# Active Filter

- A passive filter consists of passive components, such as inductors (_L_), resistors (_R_), and capacitors (_C_).
- Value of _L_ becomes large and its size bulky as frequency reduces (e.g. < 1 MHz), making compact filter design challenging.
- Active filters use operational amplifiers in combination with _R_ and _C_ without _L,_ and the size of the filters become very compact.
- The modular approach used in the synthesis of higher-order active filters simplifies the design without worrying the loading effects.
（See应该没有丧心病狂到考默写的地步）

## 一阶低通有源滤波器

根据反相放大器的公式（可以用虚短和虚断推出来，并不难），第二级那个电容给系统添加了一个极点。

# Frequency Scaling（频率缩放）

- 一个**线性**的滤波器可以把它的频率归一化到1，它的幅度和相位响应可以通过乘一个因子$\alpha$缩放到目标频率$\omega=\alpha$。这一个过程基本就是复合函数$$T(j\omega)\implies T(j\frac{\omega}{\alpha})$$

## 缩放后的电容值

$$\frac{1}{\frac{j\omega}{\alpha}C^\prime}=\frac{1}{j\omega\frac{C}{\alpha}}\implies C^\prime=\frac{C}{\alpha}$$

## 缩放后的电感值

反正也和电容差不多：$$$$
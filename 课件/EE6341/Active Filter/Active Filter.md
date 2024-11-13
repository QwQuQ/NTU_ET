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

# Frequency Scaling（频率缩放）

- 一个**线性**的滤波器可以把它的频率归一化到1，它的幅度和相位响应可以通过乘一个因子$\alpha$缩放到目标频率$\omega=\alpha$。这一个过程基本就是复合函数$$T(j\omega)\implies T(j\frac{\omega}{\alpha})$$

## 缩放后的电容值

$$\frac{1}{\frac{j\omega}{\alpha}C^\prime}=\frac{1}{j\omega\frac{C}{\alpha}}\implies C^\prime=\frac{C}{\alpha}$$

## 缩放后的电感值

反正也和电容差不多：$$j\omega L^\prime=j\frac{\omega}{\alpha}L\implies L^\prime=\frac{L}{\alpha}$$

看完之后就会发现，往高频缩放时，电容电感变小；往低频缩放时，这俩变大

## Impedance Scaling

滤波器设计完成后要保证各个阻抗元件的值都是比较正常的，所以阻抗也可以缩放。这玩意的核心就是$$R^\prime=\beta R$$
然后带进去电容和电感的值就可以算出来：$$\beta j\omega L\implies L^\prime=\beta L$$ $$\beta\frac{1}{j\omega C}\implies C^\prime=\frac{C}{\beta}$$

# 一阶低通

$$T(s)=-1\cdot\frac{-(1)(1/s)}{1+1/s}=\frac{1}{1+s}$$
滤波器在$s=-1$处有一个极点

# 一阶高通

$$T(s)=-1\cdot\frac{\frac{-(1)(1/s)}{1+1/s}}{1/s}=\frac{s}{1+s}$$
一个零点，一个极点

# 二阶低通

二阶低通基本都带个*Q*值：$$T(s)=\frac{P(s)}{Q(s)}=\frac{1}{s^2+\frac{1}{Q}s+1}$$*Q*值用来控制频率响应中的峰值

这个二阶低通有两个极点：$$s=\frac{1}{2Q}\pm j\frac{\sqrt{4-(1/Q)^2}}{2}$$

# Sallen Key 二阶低通

$$T(s)=\frac{A}{s^2+(3-A)s+1}\implies \frac{1}{Q}=3-A$$

# 二阶高通

$$$$
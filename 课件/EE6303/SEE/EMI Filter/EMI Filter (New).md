	受到某佬的启发，重新整理一下Filter，See圣虽然PPT写得不错但还是有提升的空间（

# LISN

在50Hz频率下，LISN会将市电传递给EUT（Equipment Under Test）；在EMI频率下（很高的频率），LISN会将这些电流送到频谱仪（50欧输入阻抗）。

所以差模阻抗是$50+50=100\Omega$，而共模阻抗是$50//50=25\Omega$

差模噪声电流在LN线之间流动，共模噪声电流在L//N线与地线之间流动。

# 滤波器们（See的妙妙近似）

我其实本来不想写这个的，但是期末考试有些东西怪怪的，所以还是写一下吧

## 并联的电容当低通滤波器

![[Pasted image 20241125013826.png#pic_center|]]

$$\frac{V_L}{V_L^\prime}=1+\frac{j\omega CZ_sZ_L}{Z_S+Z_L}$$
$$A=20lg\left|1+\frac{j\omega CZ_sZ_L}{Z_S+Z_L}\right|$$
令$Z_P=Z_S//Z_L$，有：$$A=20lg\left|1+\frac{Z_P}{Z_{\text{cap}}}\right|$$
- 当频率低的时候，$|Z_{cap}|$很大，衰减是0
- 当频率达到$\left|\frac{Z_P}{Z_{cap}}\right|=1$时，电容开始提供衰减
- 当$\left|Z_{cap}\right|\ll \left|Z_P\right|$时，可以近似为：$$A_{\mathrm{dB}}\approx20lg\left|Z_P\right|-20lg\left|Z_{\text{cap}}\right|$$
这一个近似在使用阻抗图时非常好用，但感觉这玩意阶数高了会很难算。
## 串联的电感当低通滤波器

![[Pasted image 20241125014552.png#pic_center|]]

也差不多$$\frac{V_L}{V_L^\prime}=1=\frac{j\omega L}{Z_S+Z_L}$$
$$A_{\mathrm{dB}}=20lg\left|1+\frac{j\omega L}{Z_S+Z_L}\right|=20lg\left|1+\frac{Z_{\text{ind}}}{Z_{\text{sum}}}\right|$$
- 低频时，没有衰减
- 高频时近似为：$$A_{\mathrm{dB}}=20lg\left|Z_{\text{ind}}\right|-20lg\left|Z_{\text{sum}}\right|$$

## 总结

![[Pasted image 20241125045016.png]]
要注意两种二阶滤波器中电容的位置（23年3c要分析这个），电容总是放在阻抗较大的一侧。

## 差模的EMI滤波器

![[Pasted image 20241125015121.png|记住这张图]]
由于是差模，所以LISN的阻抗为100欧
![[Pasted image 20241125015416.png#pic_center|差模滤波器的模型]]

![[Pasted image 20241125015531.png#pic_center|实际看起来是这样的]]
## 共模的EMI滤波器

![[Pasted image 20241125015236.png|共模的等效电路图]]
由于是共模，所以LISN的阻抗为25欧
![[Pasted image 20241125015342.png#pic_center|共模滤波器的模型]]
![[Pasted image 20241125015502.png#pic_center|实际看起来是这样的]]

## 很奇怪的阻抗图

### 并联

两个元件并联阻抗取下面的，也就是说交点处以下面的为准。

数据都是23年第3题的，懒得编数据了。Mathmatica告诉我们：![[Pasted image 20241125141716.png#pic_center|阻抗图]]

如果忽略蓝线的尖峰，单纯用直线表示的话，就是取下面的部分。

![[Pasted image 20241125141817.png#pic_center|电容和电阻并联也是一样]]
![[Pasted image 20241125141843.png#pic_center|图已经够多了]]

### 串联

两个元件串联阻抗取上面的，交点处以上面为准。还是Mathematica丢图流。
![[Pasted image 20241125141945.png#pic_center|串联取上面的]]
![[Pasted image 20241125142107.png#pic_center|挺清楚的]]
![[Pasted image 20241125142206.png#pic_center|图要满出来了]]

# Exercise 3

A SMPS is connected to the AC mains through a line impedance stabilization network (LISN). The equivalent DM noise source impedance of the SMPS is found to be a $0.1\Omega$ resistance in series with a $\text{10nH}$ inductance. To suppress the high frequency DM conducted noise from the SMPS, a low pass filter must be added in the SMPS. With the help of impedance graph, estimate the filter attenuation at $\text{100kHz}$, $\text{1MHz}$ and $\text{10MHz}$ for a second order LC low pass filter.

The selected components:
- DM inductor in each line = $\mathrm{100\mu H}$ with a SRF of $\mathrm{2MHz}$.
- X-capacitor = $\mathrm{0.01\mu F}$ with a SRF of $\mathrm{30MHz}$.

## 霸王硬上弓的精确解

串联进电路的电感值为$$2\times100\mathrm{\mu H}=200\mathrm{\mu H} \text{ SRF}=1\mathrm{MHz}$$
画出差模电路的等效模型：![[Pasted image 20241125020508.png#pic_center|差模电路的等效模型]]

非理想器件使用的模型：
![[Pasted image 20241125034146.png#pic_center|电容，忽略串联等效电阻]]
![[Pasted image 20241125034205.png#pic_center|电感，忽略并联等效电阻]]

这俩玩意的谐振频率公式为：$$f_{\text{SRF}}=\frac{1}{2\pi\sqrt{LC}}$$

根据谐振频率算出$Z_{\text{CAP}}$的串联等效电感：$$L_{\text{CAP}}=2.814\mathrm{nH}$$
$$Z_{\text{CAP}}=L_{\text{CAP}}+C_{\text{CAP}}$$

同理可得$Z_{\text{IND}}$的并联等效电容：$$C_{\text{IND}}=63.33\mathrm{pF}$$
$$Z_{\text{IND}}=C_{\text{IND}}//L_{\text{IND}}$$
Z
没有滤波器时的$Z_{\text{LISN}}$两端电压：$$V_L=V_S\frac{Z_{\text{LISN}}}{Z_{\text{LISN}}+Z_S}$$
有滤波器时的$Z_{\text{LISN}}$两端电压：$$V_L^\prime=V_S\frac{Z_{\text{LISN}}//Z_{\text{CAP}}}{Z_S+Z_{\text{IND}}+Z_{\text{LISN}}//Z_{\text{CAP}}}$$

滤波器的衰减是：$$A_{\mathrm{dB}}=20log\frac{V_L}{V_L^\prime}$$

![[Pasted image 20241125041622.png#pic_center|用万能的Mathematica画图1]]
![[Pasted image 20241125041205.png#pic_center|用万能的Mathematica画图2]]

带入求值：$$A=2.12\mathrm{dB@100kHz}=40.47\mathrm{dB@1MHz}=51.37\mathrm{dB@10MHz}$$
See的画图法还挺准的，就是有点费笔。
- 记住，并联取下面的，串联取上面的

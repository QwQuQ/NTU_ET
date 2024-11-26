	穿花蛱蝶兰间舞～
# Exercise 1

A CMOS gate is powered by 3.3V supply voltage. During the low to high transition at the output with 1ns rise time, the output has to drive 5 identical CMOS gates. The input capacitance of each CMOS gate is10 pF. What is the peak transient load current during the transition?

## 解

$$I_L=\frac{5\times10\mathrm{pF}\times3.3\mathrm{V}}{1\mathrm{ns}/2}=330\mathrm{mA}$$
需要注意的点：
- 噪声电流上升时间是方波上升时间的一半，所以这里是$0.5\mathrm{ns}$

# 三角波的傅立叶级数

$$\left|I_n\right|=\frac{2It_{\text{rise}}}{T}\left[\frac{\mathrm{sin}\left(\frac{n\pi t_{\text{rise}}}{T}\right)}{\frac{n\pi t_{\text{rise}}}{T}}\right]^2=\frac{2It_{\text{rise}}}{T}\left[\frac{\mathrm{sin}\left(x\right)}{x}\right]^2,\ x=\frac{n\pi t_{\text{rise}}}{T}$$
上式中：
- $n$是正整数，取值范围1，2，3，4……
- 第$n$次谐波的频率为：$$f=\frac{n}{T}$$
- 谐波的滚降特性：
	- 在$f=\frac{1}{\pi t_{\text{rise}}}$之前，谐波幅度基本是平的
	- 在$f=\frac{1}{\pi t_{\text{rise}}}$之后，谐波的幅度以$-40\mathrm{dB/decade}$的速度滚降

## Exercise 2

A repetitive current waveform is shown below. Compute the fundamental, second and third harmonics of the current waveform. Plot the approximate current spectrum of the waveform.

![[Pasted image 20241125174530.png#pic_center|]]
$$t_{r}=1\text{ns},T=20\text{ns},I=500\text{mA}$$

### 解

$$\left|I_n\right|=\frac{2It_{\text{rise}}}{T}\left[\frac{\mathrm{sin}\left(\frac{n\pi t_{\text{rise}}}{T}\right)}{\frac{n\pi t_{\text{rise}}}{T}}\right]^2$$
开始滚降的频率：$$f=\frac{1}{\pi t_r}=318.3\mathrm{MHz}$$所以会在第6个谐波之后衰减
$$I_1=49.59\mathrm{mA}=93.91\mathrm{dB\mu A}$$
$$I_5=40.53\mathrm{mA}=92.16\mathrm{dB\mu A}$$
$$I_6=36.84\mathrm{mA}=91.33\mathrm{dB\mu A}$$
$$I_7=90.33\mathrm{dB\mu A}$$
$$I_8=89.14\mathrm{dB\mu A}$$
$$I_9=87.75\mathrm{dB\mu A}$$
# Radiated Emission

## 差模电流
$$E_{\text{DM,max}}=2.632\times10^{-14}\left(\frac{f^2AI_{\text{DM}}}{r}\right)\mathrm{V/m}$$

### 差模电流和频率的关系

将$E_{\text{DM,max}}$写成对数的形式：$$E_{\text{DM,max}}=20\mathrm{log}C+40\mathrm{log}f+20\mathrm{log}I_{\text{DM}}$$
可以发现电场与频率的对应关系是一直以$40\mathrm{dB/decade}$上升。可以直接感性理解，在$f_c$后，$I_{\text{DM}}$以$40\mathrm{dB/decade}$的速率下降，所以综合的关系是：在$f_c$之前，电场以$40\mathrm{dB/decade}$的速度上升，而之后不变，最大的电场就是$f_c$频率带入时的值。
需要注意的是这是电场的包络，实际的电场由于存在$\text{sin}$函数的关系会非常复杂。

## 共模电流

**需要注意的是，共模电流是L线与N线二者共模电流之和（2021年）。但如果题目说明了使用的是clamp on电流探头的话，由于是直接测量L+N两根线的，所以不需要乘2。**

$$E_{\text{CM,max}}1.26\times10^{-6}\left(\frac{fI_{\text{CM}}l}{r}\right)\mathrm{V/m}$$
# Board Resonances

$$f_{mn}=\frac{150\sqrt{\left(\frac{m}{L}\right)^2+\left(\frac{n}{W}\right)^2}}{\sqrt{\epsilon_r \mu_r}}\mathrm{MHz}$$

# Exercise 6

A voltage regulator (VR) provides DC power to an integrated circuit (IC) through the power and ground planes of the PCB. When the IC is in operation, it draws the current from the capacitor and the current waveform is given below. If the capacitor is ideal and its capacitance is large enough to supply the current to the IC, will the PCB comply with CISPR 22 Class B limit? If the connection from the capacitor to the IC is open-circuited, will the PCB still comply with the same limit?

![[Pasted image 20241125181839.png#pic_75center|]]
![[Pasted image 20241125182138.png#pic_center|]]

先考虑有电容的情况，使用小学数学题计算出回路的面积
![[Pasted image 20241125181948.png#pic_75center|]]
$$A=(1.2+1.5)(3+5+3)-1.2\times 5=23.7\mathrm{mm^2}=23.7\times 10^{-6}\mathrm{m^2}$$
谐波的电流：$$\left|I_n\right|=\frac{2It_r}{T}\left(\frac{\mathrm{sin}\left(\pi t_r nf_{\text{fund}}\right)}{\pi t_r nf_{\text{fund}}}\right)^2=0.162114\frac{\mathrm{sin}(0.392699 n)^2}{n^2}$$
带入那个什么差模的电场公式：$$E_{\text{DM}}=2.632\times10^{-14}\left(\frac{nf_{\text{fund}}AI_{\text{DM}}}{r}\right)$$
综合两个式子，可以得到$$E_{\text{DM}}=0.000025281 \times\mathrm{sin}(0.392699n)^2$$
接下来的就是，自己代数字算……我懒。计算器要打爆了。
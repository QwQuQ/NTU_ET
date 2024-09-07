# EMI接收机

EMI接收机用于测量EUT的辐射

检波器：QP、PK、RMS、AV

<div align="center">
<img src="image.png" width=70%>
<br>
<div>CISPR 16-1-1提供了关于EMI接收机的数据</div>
<br>
</div>

<div align="center">
<img src="image-1.png" width=70%>
<br>
<div>EMI接收机的框图</div>
<br>
</div>

根据EMI接收机的框图可以看出，这是一台二次变频类型的接收机

## 窄带信号

3dB带宽小于接收机3dB带宽的信号（要求信号的载波与接收机的接收频率相同）

一般是CW连续波、调制后且带宽小于接收机带宽的CW连续波信号

## 宽带信号

带宽大于接收机3dB带宽的信号

窄脉冲（冲激函数）、时钟信号（谐波分量大，频谱图为sinc函数的包络）、UWB脉冲（超宽带脉冲）

（这后面的图我没看懂，也不知道他在讲什么。好像也不是卷积效应）

# 检波器

接收机的检波器一般用来测量目标信号的功率或者电压

对于没有调制的信号（CW连续波），所有检波器必须输出相同的RMS值

$$V_{RMS}=\sqrt{\frac{1}{T}\int_{0}^T A^2 cos^2\left(\omega t\right)\mathrm{d}t}=\frac{A}{\sqrt{2}}$$

**类型**

Peak Detector(PK)

Quasi Peak Detector(QP)

Root Mean Square Detector(RMS)

Average Detector(AV)

## Peak Detector

充电的时间常数极小

放电的时间常数非常长

显示的是与脉冲重复无关的峰值

显示出的最大幅度：PK>QP,RMS

<div align="center">
<img src="image-2.png" width=70%>
<br>
<div><font size=2><B>峰值检波器电路</B></font></div>
<br>
</div>

$R_d$ 用来提供极大的放电时间常数

### 充电特性

<br>
<div align="center">
<img src="image-3.png" width=70%>
<br>
<div><font size=2><B>输出电压曲线</B></font></div>
<br>
</div>

对于理想二极管，它没有内阻，所以电容两端的电压会瞬间充电到 $V_{in}$

对于真实的二极管，它有内阻 $r$ ，充电时会有一段上升时间（忽略二极管压降）

<br>
<div align="center">
<img src="image-6.png" width=70%>
<br>
<div><font size=2><B>真实的电路图</B></font></div>
<br>
</div>

电容两端的电压（ $0\leq t \leq \tau_{\mathrm{Pulse\ Width}}$ ）：

$$v_C=V^\prime\frac{R}{R_r}\left(1-e^{-\frac{t}{\tau_{C}}}\right)$$

 $V^\prime$ 在第一个脉冲时等于 $V_{in}$

其中 $$\tau_C=\frac{rRC}{R+r} \approx rC$$

当 $R \gg r$ 时约等于成立

### 放电特性

$$
\begin{cases}
    v_D=V^{\prime\prime}e^{-\frac{t}{\tau_D}} \\
    \tau_D=RC \\
    V^{\prime\prime}=v_C\left(t=\tau_{PW}\right) \\
\end{cases}
$$

对于 CISPR 16-1-1标准
<br>
<div align="center">
<img src="image-9.png" width=70%>
<br>
<div><font size=2><B>比值</B></font></div>
<br>
</div>

## Quasi Peak Detector

准峰值检波器一般用于 $1GHz$ 以上的频率

充电速度快和相对长的放电时间常数

读数受到脉冲重复频率的影响

<br>
<div align="center">
<img src="image-4.png" width=70%>
<br>
<div><font size=2><B>峰值检波器电路</B></font></div>
<br>
</div>

<br>
<div align="center">
<img src="image-5.png" width=70%>
<br>
<div><font size=2><B>输出电压的时域特征</B></font></div>
<br>
</div>

其中 

$$\mathrm{Pulse\ Repetition\ Frequency}=\frac{1}{\tau_{PRI}}$$

（I大概是Interval的意思？）

输出电压的方程（与峰值检波器类似，只是充电电阻相比非常大）：

<br>
<div align="center">
<img src="image-7.png" width=70%>
<br>
<div><font size=2><B>电路图</B></font></div>
<br>
</div>

以脉冲开始为原点算充电特性： $0 \leq t \leq \tau_{PW}$

$$
\begin{cases}
    v_C=V^\prime\frac{R_2}{R_1+R_2}\left(1-e^{-\frac{t}{\tau_C}}\right) \\
    \tau_C=\frac{R_1 R_2 C}{R_1+R_2} \\
    V^\prime=v_{in}
\end{cases}
$$

以脉冲结束为原点算放电特性： $0 \leq t \leq \tau_{PRI}-\tau_{PW}$ 

$$
\begin{cases}
    v_D=V^{\prime\prime}\frac{R_2}{R_1+R_2}\left(1-e^{-\frac{t}{\tau_D}}\right) \\
    \tau_D=R_2 C \\
    V^{\prime\prime}=v_C\left(\tau_{PW}\right)
\end{cases}
$$

QP检波器的输出收到脉冲宽度和脉冲间隔的影响（PPT上的图还挺详细的，不写了）

## Example

（哼，哼，哼，啊啊啊啊啊啊啊啊啊啊啊啊，啊啊啊啊啊啊啊啊啊啊）


# 测试装备

## 天线

天线的增益一般描述的是远场特性

<br>

但是EMI的测量一般在近场进行：

空间限制

设备发出的辐射信号较弱

辐射抗扰度测试需要强电磁场

<br>

对于EMI测试，我们一般在电场或者磁场测量接收到的电压，而不是发射和接收功率：

所以有一套全新的描述天线特性的参数：

Antenna Factor (AF)

Transmit Antenna Factor (TAF)

<br>

### Antenna Factor

$$AF=\frac{E}{V_L} m^{-1}= 20log_{10}\frac{E}{V_L}\mathrm{dB}/m$$

这个描述的是电场在**接收**天线的**负载**上产生单位电压的情况。很明显这边假设的是极化与天线是匹配的，并没有考虑极化损耗。天线系数越小，相同电场强度的情况下接收到的电压越高。

#### Rod Antenna

$$AF\mathrm{@20kHz}=75\mathrm{dB}/m$$

$$AF\mathrm{@20MHz}=25\mathrm{dB}/m$$

如果电场强度为 $1V/m$ 的话，天线接收到的电压为：

20kHz:

$$V=\frac{E}{AF}=E\left(\mathrm{dB}\right)-AF\left(\mathrm{dB/m}\right)=\frac{1}{10^{75/20}}=0-75=-75\left(\mathrm{dBV}\right)=0.17mV$$

20MHz:

$$V=\frac{E}{AF}=E\left(\mathrm{dB}\right)-AF\left(\mathrm{dB/m}\right)=\frac{1}{10^{75/20}}=0-25=-25\left(\mathrm{dBV}\right)=56.23mV$$

### Transmit Antenna Factor

$$TAF=\frac{E_{1m}}{V_t} m^{-1}=20log_{10}E_{1m}-20log_{10}V_t \left(\mathrm{dB}/m\right)$$

其中 $E_{1m}$ 是发射天线在1m处测量到的场强， $V_t$ 是发射电压。TAF越大，产生的电场强度越大。

对于同一个天线，AF和TAF不一样

### 对数周期天线

对数周期天线可以在很宽的频率上产生强电场。

ATR 26M6G from ATR worldwide covers from 26MHz to 6GHz.（某种广告）

如果输入功率为10W，频率22MHz，1m处产生的场强为10V/m，可以计算得到：

假设是50欧负载，输入天线的电压为：

$$V=\sqrt{P\times Z_0}=22.360V$$

所以

$$TAF=\frac{10}{22.360}=0.45m^-1$$

用dB做法也可以：

$$22.360V=26.989\mathrm{dB}V=146.989\mathrm{dB}\mu V$$

$$10V/m=20\mathrm{dB}V\cdot m^{-1}=140\mathrm{dB}\mu V\cdot m^{-1}$$

$$TAF=-6.989\mathrm{dB}/m$$

### 环形天线（磁场天线）

感应电压(Induced Voltage)：

$$V_i=-n\frac{\mathrm{d}\Phi}{\mathrm{d}t}=2\pi f n A B$$

$n$ 为线圈匝数， $f$为频率， $A$ 为线圈的截面积， $B$ 为磁感应强度。

### $AF_H$ 和 $AF_B$

$$AF_H=\frac{H}{V_L}S/m=\frac{1}{2\pi f n A \mu_0}$$

$$AF_B=\frac{B}{V_L}=\frac{\mu H}{V_L} Tesla/V$$

$$AF=AF_H\times \eta_0=\frac{H}{V_L}\times \frac{E}{H}=\frac{E}{V_L}$$

$$AF\left(\mathrm{dB}/m\right)=AF_H\left(\mathrm{dB}S/m\right)+20log_{10}\left(\eta_0\right)$$

## Antenna Example 1 作业形式

$$V_{in}=\sqrt{P\times Z_0}=50V=33.9794\left(\mathrm{dB}V\right)$$

$$E_{1m}=TAF\left(\mathrm{dB}/m\right)+V_{in}\left(\mathrm{dB}V\right)\\
=33.9794-4=29.9794\left(\mathrm{dB}V/m\right)
$$

$$E_{3m}=E_{1m}\left(\mathrm{dB}V/m\right)-20log_{10}(3m)+20log_{10}(1m)=20.436975\left(\mathrm{dB}V/m\right)
$$

$$V_L=E_{3m}\left(\mathrm{dB}V/m\right)-AF\left(\mathrm{dB}/m\right)=20.436975-23=-2.5630\left(\mathrm{dB}V\right)=0.74V$$


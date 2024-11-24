---
aliases: 
tags:
  - MOSFET
---
# MOS Capacitors

## 前置知识

- [[Vacuum Level]]
- [[Electron Affinity]]
- [[Work Function]]
- Ionization energy
	- energy required to raise an electron from the valence band edge, $E_V$ to Vacuum Level $E_0$

[[MOS Capacitors]]的四种情况

## Poisson Equation

Used for finding potentials within semiconductor devices. Based on **Gauss's Law**

$$\begin{cases}
\nabla\cdot\mathbf{D}&=\rho \\
\mathbf{D}&=\epsilon \mathbf{E} \\
\mathbf{E}&=\nabla\psi
\end{cases} \\
\implies \nabla^2\psi=-\frac{\rho}{\epsilon}$$

将上述方程转换到1维的笛卡尔坐标系。$$\frac{\mathrm{d}^2\psi}{\mathrm{d}x^2}=-\frac{\rho}{\epsilon}$$

### 硅的表面电势

硅的静电势经常被表示为$$\psi_i=-\frac{E_i}{q}$$
在一维分析中，能带弯曲可以表示为$$\psi(x)=\psi_i(x)-\psi_i(x=\infty)$$
$\psi(0)$自然是表面电势
- 说了好像没说

### 解Poisson Equation

由于同时有移动的电荷和静止的电荷，所以Poisson Equation需要写成：$$\frac{\mathrm{d}^2\psi}{\mathrm{d}x^2}=-\frac{q}{\epsilon}\left[p(x)-n(x)+N_d^+(x)-N_a^-(x)\right]$$
使用Law of mass action：$$N_d^+(x)-N_a^-(x)=\frac{n_i^2}{N_a}-N_a$$
[[Boltzmann Distribution|玻尔兹曼分布]]：$$\begin{cases}p(x)=n_i \text{exp}\left(\frac{q(\psi_f-\psi_i)}{kT}\right)=N_a \text{exp}\left(\frac{-q\psi}{kT}\right)\\n(x)=n_i \text{exp}\left(\frac{q(\psi_i-\psi_f)}{kT}\right)=\frac{n_i^2}{N_a}\text{exp}\left(\frac{q\psi}{kT}\right)\end{cases}$$
带进去之后式子变成：$$\frac{\mathrm{d}^2\psi}{\mathrm{d}x^2}=\frac{-q}{\epsilon_{\text{Si}}}\left[N_a\left(\text{exp}\left(-\frac{q\psi}{kT}\right)-1\right)-\frac{n_i^2}{N_a}\left(\text{exp}\left(\frac{q\psi}{kT}\right)-1\right)\right]$$

## Silicon Charge

- Flat-band $\psi_s=0$, $Q_s=0$
- Accumulation, $\psi_s<0$, $exp\left(-\frac{q\psi_s}{kT}\right)$ term dominates and $Q_s$ increases as $exp\left(-\frac{q\psi_s}{2kT}\right)$
- Depletion, $\psi_s>0$, $\frac{q\psi_s}{kT}$ dominates. $Q_s$
- $\psi_s$进一步增大，

## Strong Inversion

$$\frac{\mathrm{d}\psi}{\mathrm{d}x}=-\sqrt{\frac{2kTN_a}{\epsilon_{\text{Si}}}\left(\frac{q\psi}{kT}+\frac{n_i^2}{N_a^2}\mathrm{exp}\left(\frac{q\psi}{kT}\right)\right)}$$

### Common criterion for strong inversion

$$\frac{n_i^2}{N_a^2}\mathrm{exp}\left(\frac{q\psi_s}{kT}\right)=1$$
$$\psi_s(\text{inv})=2\psi_B=2\frac{kT}{q}\mathrm{ln}\left(\frac{N_a}{n_i}\right)$$
$\psi_B$是体的电势

## MOS Gate Voltage Equation

硅表面的电势$\psi_S$不容易测量，但是栅极电压$V_g$可以测，所以$$V_g=V_{ox}+\psi_s$=\frac{\left|Q_s\right|}{C_{ox}}+\psi_s$$
$C_{ox}$是栅氧单位面积的电容

## MOS Small Signal Capacitances

定义：$$C=\frac{\mathrm{d}|Q_s|}{\mathrm{d}V_s}$$
通过对Gate Voltage Equation取微分，可以得到硅的电容表达式$$C_{\text{Si}}=\frac{\mathrm{d}|Q_s|}{\mathrm{d}\psi_s}$$
$$\frac{\mathrm{d}V_g}{\mathrm{d}|Q_s|}=\frac{\mathrm{d}V_{ox}}{\mathrm{d}|Q_s|}+\frac{\mathrm{d}\psi_s}{\mathrm{d}|Q_s|}$$
$$\implies \frac{1}{C}=\frac{1}{C_{ox}}+\frac{1}{C_{\text{Si}}}$$

## 测量MOS Capacitance

- Apply a dc ramped bias across the MOS capacitor (step increase).
- Superpose a small ac signal (<100mV)
- Sense the out-of-phase (reactive) component current or $C=\frac{\mathrm{Im}(Y)}{2\pi f}$, Y是电导$Y=G+j2\pi fC$
- Repeating the above across a range of dc bias and/or frequencies will yield a C-V curve.

## Surface States and Interface Trapped Charge

### Surface States（表面态）

- 表面态是指位于**Si-SiO₂界面**处的局部电子态，由于硅晶格在界面处的周期性终止而产生。
- 这些态的能量位于硅的带隙内，成为电子和空穴的捕获中心。
- 影响：
	- 降低导电电流
	- 降低载流子迁移率

- 控制表面态：
	- 不同晶向的表面态密度不同，例如：  (100)<(110)<(111)，  **(100)**方向的晶圆优先用于CMOS制造。
	- 后金属化退火，在**400°C**的氢气（H2H_2H2​）或重氢（D2D_2D2​）环境中退火。氢与硅的悬挂键（dangling bonds）结合，生成稳定的氢化硅（Si-H）键，从而钝化表面态。

## Fixed Oxide Charge

- 由氧化过程中或氧化后退火过程中引入的过量Si生成。
- 位于Si-SiO2界面附近并停留不动。
- 固定氧化物电荷的密度也与方向有关，(100) < (110) < (111)。

## Mobile Ionic Charge

- 由于晶圆处理过程中的离子污染（$Na^+$，$K^+$）
- 在电场和高温下，这些离子能够在二氧化硅中漂移
- 硅-二氧化硅界面附近的移动离子能够导致漏电流和库仑散射
- 控制污染对于减少这玩意很重要，所以晶圆处理要超净间

## Oxide Trapped Charge

- 通过带电粒子或高能光子的轰击，可以很容易地在SiO2内部生成局部态（陷阱）。
- 通过隧道效应或热载流子效应注入SiO2的电子或空穴随后可以被陷阱捕获。
- 通过热退火可以相对容易地去除陷阱。

上面这些玩意，会导致 MOS 电容器的 C-V 曲线相对于理论（理想）C-V 曲线被拉伸或移动。

# Long channel MOSFET

沟道长度大于10微米，长沟道器件表现出理想的特性

- 用于推导C-V特性的两种近似：
	- Gradual channel approximation (GCA)
	  假设沟道电位沿着沟道长度方向的变化是缓慢的。
	- Charge sheet approximation (CSA)
	  假设沟道内的电荷分布是沿着沟道方向均匀的，即假设沟道内的电子或空穴形成一个薄薄的电荷片。


## Gradual Channel Approximation (GCA)

沿着沟道（y方向）的电场变化远小于垂直于沟道（x方向）的电场变化。
- Use of GCA will reduce the Poisson’s equation from 2-D to just 1-D and simplifies the analysis.
- Applicable to most of the channel except the **pinch-off point** and **beyond**.

$$J_n(x,y)=-q\mu_nn(x,y)\frac{\mathrm{d}V(y)}{\mathrm{d}y}$$

沟道中的电子迁移率$\mu_n$比体中的载流子迁移率小很多。$n(x,y)$是在$(x,y)$点的电子浓度。
$J_n(x,y)$包含了漂移和扩散电流，因为$V(y)$被假设为电子的准费米能级。

整个反型层的高度为$x_i$，所以从$x=0$积分到$x=xi$，定义电流方向是$-y$，可以得到$I_{ds}$电流：$$I_{ds}(y)=W\int_0^{x_i}q\mu_nn(x,y)\frac{\mathrm{d}V(y)}{\mathrm{d}y}\mathrm{d}x$$
假设沟道中的电子迁移率是恒定的，等效为$\mu_{\text{eff}}$。使用GCA等效，可以认为$\frac{\mathrm{d}V(y)}{\mathrm{d}y}$在x轴是参数，所以也可以提出来。这样可以得到$$I_{ds}(y)=qW\mu_{\text{eff}}\frac{\mathrm{d}V(y)}{\mathrm{d}y}\int_0^{x_i}n(x,y)\mathrm{d}x$$
令$$Q_i(y)=-q\int_0^{x_i}n(x,y)\mathrm{d}x$$
这样可以得到$$I_{ds}=-\mu_{\text{eff}}WQ_i(y)\frac{\mathrm{d}V(y)}{\mathrm{d}y}$$
因为$V$是一个$y$的函数，所以可以写成$$I_{ds}=-\mu_{\text{eff}}WQ_i(V)\frac{\mathrm{d}V(y)}{\mathrm{d}y}$$
把$\mathrm{d}y$乘到左边，同时积分：$$\int_0^{L}I_{ds}(y)\mathrm{d}y=\int_0^{V_{ds}}-\mu_{\text{eff}}WQ_i(V)\mathrm{d}V$$
因为沟道中电流处处相等，所以$$\int_0^{L}I_{ds}(y)\mathrm{d}y=LI_{ds}$$
从而得到$$I_{ds}=\mu_{\text{eff}}\frac{W}{L}\int_0^{V_{ds}}-Q_i(V)\mathrm{d}V$$

## Charge Sheet Approximation

- 反型电荷正好位于硅表面，并形成一个零厚度的电荷片。
- 反型层上没有电位降。
- 在电荷片下方是耗尽区。在这一区域，由于强反型的开始，表面电位（或能带弯曲）为 $\psi_s = 2\psi_B + V(y)$。

使用耗尽近似，体的耗尽层电荷密度为：$$Q_{\text{depletion}}=-qN_aW_{dm}=-\sqrt{2\epsilon_{\text{Si}}qN_a(2\psi_B+V)}$$
硅中的总电荷为：$$Q_{\text{Si}}=-C_{ox}(V_g-V_{fb}-2\psi_B-V)$$
对他们做差可以得出反型层的电荷：$$Q_i=\sqrt{2\epsilon_{\text{Si}}qN_a(2\psi_B+V)}-C_{ox}(V_g-V_{fb}-2\psi_B-V)$$
最终得到的电流表达式为：$$I_{ds}=\mu_{\text{eff}}C_{ox}\frac{W}{L}\left[\left(V_g-V_{fb}-2\psi_B-\frac{V_{ds}}{2}\right)-\frac{2\sqrt{2\epsilon_{\text{Si}}qN_a}}{3C_{ox}}\left[(2\psi_B+V_{ds})^2-(2\psi_B)^{3/2}\right]\right]$$

## Linear Region

$$V_{ds}<V_g-V_t$$
对那个很复杂的$I_{ds}$式子级数展开，只保留线性项，可以得到：$$I_{ds}=\mu_{\text{eff}}C_{ox}\frac{W}{L}\left(V_g-V_{fb}-2\psi_B-\frac{\sqrt{4\epsilon_{\text{Si}}N_a\psi_B}}{C_{ox}}\right)V_{ds}$$
定义阈值电压为：$$V_t=V_{fb}+2\psi_B+\frac{\sqrt{4\epsilon_{\text{Si}}N_a\psi_B}}{C_{ox}}$$
所以$I_{ds}$可以写为：$$I_{ds}=\mu_{\text{eff}}C_{ox}\frac{W}{L}\left(V_g-V_t\right)V_{ds}$$
此时的MOS管像一个电阻，电阻率受到$V_g$控制：$$\rho_{\text{sheet}}=\frac{1}{\mu_{\text{eff}}C_{ox}(V_g-V_t)}$$
### 通过实验确定MOS管阈值电压的办法



## Saturation Region

$$V_{ds}>V_g-V_t=V_{\text{d,sat}}$$
但$V_{ds}$足够大的时候，二阶项不能忽略，所以表达式为：$$I_{ds}=\mu_{\text{eff}}C_{ox}\frac{W}{L}\left((V_g-V_t)V_{ds}-\frac{m}{2}V_{ds}^2\right)$$
上式中的$m$为体效应参数。

当$V_{ds}=V_{\text{d,sat}}=\frac{V_g-V_t}{m}$时，$I_{ds}$达到最大：$$I_{ds}=I_{sat}=\mu_{\text{eff}}C_{ox}\frac{W}{L}\frac{(V_g-V_t)^2}{2m}$$
当晶圆掺杂浓度很低时，$m=1$，式子变成了熟悉的形式：$$I_{sat}=\mu_{\text{eff}}C_{ox}\frac{W}{L}\frac{(V_g-V_t)^2}{2}$$

## Pinch off and Current Saturation

沟道夹断和电流饱和

反型层的电荷约为：$$Q_i\sim C_{ox}(V_g-V_t-mV(y))$$
当$V_g=V_{\text{d,sat}}$时，$Q_i=0$，所以当饱和时，漏极附近的反型层电荷开始消失。
这种情况叫做沟道夹断。当$V_{ds}>V_{\text{d,sat}}$时，夹断点轻微向源极移动，并且夹断点的电压维持在$V_{\text{d,sat}}$

## Charge Transport in Saturation Region

- **对于小**$V_{ds}$，$V(y)$ 随$y$平滑增加。
- 随着$V_{ds}$增加，漏极附近的反型层电荷减少，为了维持电流连续性，$\frac{\mathrm{d}V}{\mathrm{d}y}$必须加大，所以$V_(y)$的曲线向上弯曲。
- 在$V_{\text{d,sat}}$时$V(y)$在$y=L$处有一个奇点（$\frac{\mathrm{d}V}{\mathrm{d}y}=\infty$）
- y方向场的变化无法忽略，所以GCA近似失效
- 在pinch-off点后，必须解2D的泊松方程
- 在pinch-off点后，载流子不再局限于表面的沟道
- 载流子从夹断点注入耗尽层

## Subthreshold Characteristics

- 栅极电压略低于阈值电压时，$I_{ds}$并不为0，这为亚阈值电流，因为硅上方的弱反型层仍然存在。
- 亚阈值电流对于数字CMOS（互补金属氧化物半导体）应用极为重要。在CMOS逻辑门电路中，无论输出状态如何，一半的MOSFET是导通的，而另一半则关闭。亚阈值导电性限制了这些关闭的MOSFET的关断行为，并增加了**待机功耗**，这是一个主要问题。

- 亚阈值区的电流不仅包括扩散电流，还包括漂移电流，而在饱和区中主要是漂移电流。这使得亚阈值电流的分析变得更加复杂，因此该分析通常集中在低漏极偏压（low drain bias）情况下。$$I_{ds}=\mu_{\text{eff}}C_{ox}\frac{W}{L}(m-1)\left(\frac{kT}{q}\right)^2e^{q(V_g-V_t)/mkT}(1-e^{-qV_{ds}/kT})$$
- 亚阈值电流取决$于V_g$、 $V_{ds}$和体效应系数。
- 如果$V_{ds}$大于几个kT，亚阈值电流主要由$V_g$控制

### Subthreshold Slope

$$S=2.3\frac{mkT}{q}=\left(\frac{\mathrm{d}\mathrm{lg}I_{ds}}{\mathrm{d}V_g}\right)^{-1}$$
$$S = 70\sim 100mV/\text{decade}$$
在VLSI应用中，S需要小以适应高速开关。但不是很容易达到，因为S主要由温度T决定。衬底掺杂浓度$N_a$和栅氧厚度能够通过调整体效应参数的方式有限地调整S

### Importance of the Subthreshold Slope

- 亚阈值斜率在**低功耗微电子学**中非常重要。通常，电源电压会降低以节省待机和开关功率。
- 由于S的有限值和有限的下降幅度，电源电压不能随意降低。
- 降低$V_{CC}$将会在逻辑0时导致巨大的漏电流，因为此时低电平与阈值电压非常接近

# Submicron MOSFETs

- 到目前为止所概述的理论只能准确描述早期MOSFET的行为。
- 随着光刻技术的进步和MOSFET的沟道长度减少到1微米以下，可以很容易地观察到与长沟道行为的显著偏差。
- 这些偏差通常对电路应用是不利的。需要仔细的器件设计和越来越复杂的工艺集成来减轻这些影响。

## Origin of Secondary Effects in Submicron MOSFETs

- 一维模型的假设不再适用，开始使用二维模型
- 缩小MOS器件的规则并没有很好地遵守

## Short Channel Effect

- 沟道长度减小导致MOSFET的阈值电压$V_t$减小
- 施加$V_{ds}$能够加剧短沟道效应
- SCE的结果：
	- 漏电流和电源消耗增加
	- 需要对最小尺寸的器件进行优化以抵消SCE

### Physical Origin of Short Channel Effect
长沟道器件的仿真图
![[Pasted image 20241120213629.png#pic_center|simulation]]
等电位线基本沿着y轴，y轴的变化很小，电场只在x轴变化。

短沟道器件的仿真图
![[Pasted image 20241120213854.png#pic_center|]]
在相同的$V_{ds}$和$V_g$下，等电位线更加弯曲，电场是2维的。硅表面的能带更加弯曲，耗尽层更宽，器件的阈值电压更低。

- 由于漏极和源极非常接近，所以会产生二维的电场
- 两侧都形成了一个pn结并且和耗尽层相关
- 对于长沟道器件，这两个耗尽层离得足够远，所以不会影响到器件里的电场
- 对于短沟道器件，源极和漏极的距离相比耗尽层宽度并不大，所以电场的形状受到漏源电压的强烈影响。

### Threshold Voltage Lowering by SCE

- Charge Sharing Model
- Drain induced barrier lowering (DIBL)

#### Drain Induced Barrier Lowering

![[Pasted image 20241120214428.png]]
- 该图显示了表面电势（电子）与归一化距离$y/L$的函数关系。
- 在源极（$y/L=0$）处，当器件关闭时，表面势垒防止电子进入沟道区。
- 对于长通道情况（曲线A），势垒在大部分通道上是平坦均匀的。对于短通道情况（曲线B、C），势垒更低，更圆。
- 如果漏极偏压增加，势垒会进一步降低（DIBL）。降低的势垒增加了电子进入沟道的可能性，并导致阈值电压降低。

## 2-D Poisson’s Equation and Lateral Field Penetration

$$\frac{\partial E_x}{\partial x}+\frac{\partial E_y}{\partial y}=-\frac{qN_a}{\epsilon_{\text{Si}}}$$

带x的可以视为由栅极控制的场，带y的可以视为由$V_{ds}$控制的场

![[Pasted image 20241120220219.png#pic_center|Simulated lateral field vs distance y]]

- 横向电场随着距离增大呈指数型减小
- 这种指数衰减的特征长度不随通道长度而变化
- 所以短沟道器件中心的横向电场比长沟道器件大
- 施加漏极偏压会使零场点向源极移动。场的零点对应于DIBL中的电位最大点

## Source Drain Extensions

- 在源极、漏极与沟道之间插入浅结
- 自对准离子注入形成S-D延伸（低剂量）
- 沉积上间隔电介质（SiN），然后进行一次高剂量自对准注入
- 让源极和漏极对比沟道是凹陷的，代价是源极漏极的串联寄生电阻增加
## Source-Drain Series Resistance

- 寄生电阻与源极和漏极区域的有限薄层的电阻率和欧姆接触有关。
- 这种外在效应在长沟道器件中并不重要，因为沟道电阻很大，可以忽略不计。
- 然而，在亚微米器件中，沟道电阻与源极-漏极电阻相当。因此，这种外在效应现在很重要。

## Source-Drain Resistance

源极的电阻非常不理想，因为会降低gate的驱动能力

### Accumulation layer resistance

- 栅极边缘通常与源极和漏极重叠。在栅极-源极（或漏极）重叠区域，载流子被限制在一个累积层内，该累积层具有电阻$R_{ac}$

### Spreading resistance

这是与注入电流从薄的累积层扩展到源极或漏极相关的电阻分量。对于均匀掺杂的源-漏极$$R_{sp}=\frac{\rho_j}{\pi W}\mathrm{ln}\left(\frac{3x_j}{4x_c}\right)$$
其中：
- $\rho_j$是电阻率
- $x_j$是结的深度
- $x_c$是accumulation layer thickness
- $W$为器件宽度

### Sheet Resistance

这是源-漏扩散区域的电阻，简单表示为：$$R_{\text{sheet}}=\rho_{sd}\frac{S}{W}$$
$S$是栅极边缘和金属接触边缘之间的间距，$\rho_{sd}$是源-漏电荷片的电阻率。由于$\rho_{sd}$很小，这个电阻经常能够被忽略。

### Contact Resistance

$$R_{\text{contact}}=\frac{\sqrt{\rho_{sd}\rho_c}}{W}\mathrm{coth}\left(l_c\sqrt{\frac{\rho_{sd}}{\rho_c}}\right)$$
- $l_c$是接触窗口的宽度
- $\rho_c$是金属和硅之间欧姆接触的界面接触电阻率，单位是$\Omega/cm^2$。
在欧姆接触中，电流主要由隧穿或场发射主导。因此，$\rho_c$强烈依赖于势垒高度和表面掺杂浓度。

## Self-aligned Silicide Contacts

在先进的CMOS器件中，通过使用自对准硅化物或硅化物，$R_{\text{contact}}$和$R_{\text{sheet}}$被最小化。

低电阻率的硅化物层（例如$\mathrm{TiSi_2}$）形成在整个源漏扩散区域上。通过介电间隔物将该层与栅极隔离。硅化物有效地分流了来自扩散区域的电流。

$R_{\text{sheet}}$被限制在间隔物下方的非硅区域。

$R_{\text{contact}}$因为接触窗口的宽度减少，$l_c$是硅化物扩散区域的宽度。
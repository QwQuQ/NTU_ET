# 前置知识

## 传输线

- 特征阻抗：由于传输线的分布参数，将传输线激励为TEM模需要一定的能量（转化为电磁场的能量），那么这部分就可以用一个特征阻抗$Z_0$来表示
- 特征阻抗的微观理解就是这跟线单位长度上的电抗、电阻值共同形成的一个值
- 对于一个理想的无损耗传输线，电磁波在上面不发生衰减

![[Pasted image 20250225000731.png#pic_75center|]]

- 传输线都是有两部分导体的，电磁波分布在两个导体之间而不是导体内部（波导guide）

## 阻抗匹配与传输线的等效（后面会经常用到）

![[Pasted image 20250224233510.png#pic_75center|传输线的等效]]
- 在瞬态与交流分析时
	- 传输线当作负载时，可以当作一个阻抗为$Z_0$的电阻
	- 传输线当作源时，可以当作一个内阻为$Z_0$的电压源，其开路电压为**这一特定点**传输线的电压值
	- 这种等效无论传输线有多长均成立，甚至无限长也是成立的。
- 在稳态直流时，理想的无损耗传输线就是导线

# 传输线参数的的推导

![[Pasted image 20250224234352.png#pic_33center|传输线的单位长度集总参数模型]]
- 对于单位长度的传输线，我们几乎总能够将其建模为一个集总参数模型。上图中的$R$、$L$、$C$、$G$都是单位长度下的参数，例如电阻$R$的单位就应该为$\mathrm{\Omega\cdot m^{-1}}$
- 我们假设传输线是理想无损耗的，那么电阻$R$与电导$G$都能够被忽略。对于一段微元$\mathrm{d}x$情况下的传输线，可以得到其电感与电容值为：$$\displaylines{\text{Inductance}=L\mathrm{d}x \\ \text{Capacitance}=C\mathrm{d}x}$$
- 接下来使用瞬态分析，对于一对瞬态的电压与电流：$\mathrm{d}v$和$\mathrm{d}i$，我们可以列出：$$\displaylines{\mathrm{d}v=\mathrm{d}i\cdot L\mathrm{d}x\cdot \frac{1}{\mathrm{dt}} \\ \mathrm{d}i=\mathrm{d}v\cdot C\mathrm{d}x\cdot \frac{1}{\mathrm{dt}}}$$联立可以解得：$$\frac{\mathrm{d}v}{\mathrm{d}i}=\sqrt{\frac{L}{C}}$$
- 回忆一下关于电阻的拓展定义：$I-V$曲线中的斜率是电阻，那么我们就知道**特征阻抗**$Z_0$的表达式为：$$Z_0=\sqrt{\frac{L}{C}}$$
- 同样可以得到介质（电磁波存在于PCB基板中，而不是铜箔）中的电磁波速度为：$$V_{\text{propagation velocity}}=\frac{\mathrm{d}x}{\mathrm{d}t}=\sqrt{\frac{1}{LC}}$$
- 单位长度传输线的延迟为：$$\text{delay}=\frac{1}{V_{\text{propagation velocity}}}=\sqrt{LC}$$
- 至此可以根据传输线单位长度上的电感和电容来推导其参数了

### 微带线（一种传输线）的参数

*看起来好像有点重要，但我也不知道*

- 电磁波速度：$$V_{\text{propagation velocity}}=\sqrt{\frac{1}{LC}}=\frac{c}{\sqrt{\epsilon_r}}$$其中：
	- $c$为真空光速，是真空
	- $\epsilon_r$为PCB基板的介电常数（不是铜，不是空气）

# 反射

- 反射的电压信号会让传输的数据收到先前数据的影响
	- 超过噪声容限（Noise Margin）造成错误
- 对于反射，使用反射系数$\Gamma$（Tony用了$\rho$）进行描述。它表示入射波与反射波电场强度的比值（是复数）。
- 在这个课件中，电场强度就是电压值，$\Gamma$（Tony用了$\rho$）的符号表示反射电压是与入射电压**相加**还是**相减**

## 反射系数的推导

![[Pasted image 20250225004102.png#pic_50center|针对的电路图]]

- 规定入射电压电流为：$$\displaylines{v_{\text{forward}}\\ i_{\text{forward}}}$$反射电压电流为：$$\displaylines{v_{\text{reflect}} \\ i_{\text{reflect}}}$$终端叠加后的电压电流为：$$\displaylines{v_{\text{terminal}} \\ i_{\text{terminal}}}$$

![[Pasted image 20250225005259.png#pic_33center|反射波方向的等效电路]]

- 我们先对反射波进行分析，假设这个传输线是理想无损耗的，那么我们可以将前面的传输线直接等效为一个阻值为$Z_0$的电阻（在反射波传输的方向上），那么有：$$i_{\text{reflection}}=\frac{v_{\text{reflection}}}{Z_0}$$

![[Pasted image 20250225010038.png#pic_33center|入射波方向的等效电路]]

- 对于入射波进行分析，传输线又可以等效成一个阻值为$Z_0$的电阻：$$i_{\text{forward}}=\frac{v_{\text{reflection}}}{Z_0}$$

![[Pasted image 20250225005700.png#pic_50center|新的电路图]]

- 再对终端电阻进行分析，假设这个传输线是理想无损耗的，那么**最终的电压值没有衰减**，仍然为$V_{\text{forward}}$. 由于叠加定理，可以直接在反射波等效电路的基础上添加新的元件。在此基础上我们可以得到：$$\displaylines{v_{\text{terminal}}=v_{\text{forward}}+v_{\text{reflect}} \\ i_{\text{terminal}}=i_{\text{forward}}+i_{\text{reflect}} \\ i_{\text{terminal}}=\frac{v_{\text{terminal}}}{Z_{\text{terminal}}}}$$
- 联立上述三个例子，我们可以计算得到：$$v_{\text{reflection}}=\frac{Z_t-Z_0}{Z_t+Z_0}v_{\text{forward}}$$从而我们将那一大坨规定为反射系数，从而有：$$\Gamma=\frac{Z_t-Z_0}{Z_t+Z_0}$$Tony在这里使用$\rho$来表示反射系数，大概是什么另外的教材来的。
- 有了这玩意反正$v_{t}$也很好求了，就是课件上那两个式子。

## 实际情况

*在有反射系数推导的基础上理解这个是比较容易的*

- 极端值
	- 短路$\rho=-1$，终端电压为0
	- 匹配$\rho=0$，终端电压为$v_{\text{forward}}$
	- 开路$\rho=1$，终端电压为$2v_{\text{forward}}$

![[Pasted image 20250225010910.png#pic_33center|终端电阻大于特征阻抗]]![[Pasted image 20250225010923.png#pic_33center|终端电阻小于特征阻抗]]

- 一般情况：最终电压的情况根据**反射系数的正负**来判断。

## 信号的反射

*一大堆概念性知识，不写了*

![[Pasted image 20250225011156.png#pic_75center|]]

- 振铃比较重要

## Lattice Diagram

*暴力计算反射的一种手段*
*我会使用LTSPICE进行辅助分析*

- 画Lattice图需要知道的参数有：
	- 传输线的特征阻抗$Z_0$和传播延迟$t_{\text{pd}}$
	- 源的电压和源的串联等效阻抗
	- 负载的阻抗
- Lattice最下面的箭头代表最初发射的波前，想象一下一条很长的贪吃蛇盘踞在这短短的传输线里。要计算源与负载的电压只需要把每一段的电压加起来就可以了

## 例子

### 手撕的过程

![[Pasted image 20250225012526.png#pic_50center|就是PPT的第一个例子]]

- 首先计算两边看进去的反射系数：$$\displaylines{\rho_{\text{source}}=\frac{75-50}{75+50}=0.2  \\ \rho_{\text{terminal}}=\frac{\infty-50}{\infty+50}=1}$$

![[Pasted image 20250225013040.png#pic_33center|对源端的电路进行等效]]

- 使用等效电路计算驱动传输线的电压$$V_{\text{source}}=\frac{Z_0}{Z_0+Z_s}\cdot V_{S}=0.8V$$
- 画出Lattice图，每一次反射都使用对应的反射系数进行计算
![[Pasted image 20250225014111.png#pic_75center|]]
### SPICE科技

![[Pasted image 20250225012243.png#pic_50center|LTSPICE仿真电路]]
![[Pasted image 20250225014303.png#pic_75center|LTSPICE说我们是对的]]

## 减少反射的技术

*PPT上写了一堆，总结一下就是：阻抗一定要匹配*
- 输出阻抗：上拉电阻一般是300欧（P管没力气），下拉电阻30欧。
- 输入阻抗：1.5V以内低于100欧，1.5V以上大于10k欧

### Series Matching

*串电阻*
- To increase the output impedance artificially in order to match the line characteristic impedance
- To prevent negative overshoot ( ‘1’→‘0’ transition )
- Using external resistor in series with typical values of $\approx 47\Omega$

![[Pasted image 20250225022046.png#pic_50center|没什么好说的]]

- All reflections propagate back and are damped at the transmitter.
- Received voltage > transmitted voltage
- Slower rise time
- Smaller residual reflections than end terminators
- At low-pulse repetition rates, source terminators dissipate little power
- The same peak drive power as an end-terminated line

#### 功率消耗

- 源端电阻在一次上升下降周期中的能量消耗，*我觉得得具体问题具体分析*：
- 直到信号反射回来之前，串联匹配（假设完美匹配）电阻的能量消耗是：$$E=2t_{\text{propagation delay}}\frac{\left(\Delta V/2\right)^2}{R}$$

### Line Termination

- All reflections are damped at the receiver
- Received voltage = transmitted voltage
- Faster rise time
- Larger power dissipation
- The same peak drive power as an source-terminated line

![[Pasted image 20250225022328.png#pic_50center|]]

#### 功率消耗

- 这屁股电阻的消耗功率是（注意不是能量）$$P=\frac{\left(V_{\text{logic high}}-V_{SS}\right)^2+\left(V_{\text{logic low}}-V_{SS}\right)^2}{2R_D}+\frac{\left(V_{\text{CC}}-V_{logic high}\right)^2+\left(V_{\text{CC}}-V_{logic low}\right)^2}{2R_U}$$

### 其他的办法

- Clamping钳位
- Middle Terminators

# 透射

- 如果我们有两端传输线，在界面不连续的特征阻抗处就会**既有反射又有透射**
- 透射波的电场强度（电压）为：$$V_{\text{透射}}=V_{\text{入射}}\cdot \left(\rho+1\right)$$
- 这在能量守恒上是很好证明的，但是很烦。相位上透射波的相位与入射波的相位是相同的。
- 于是我们就能够得到这个超级加倍的Lattice图
![[Pasted image 20250225021516.png#pic_75center|]]

# 串扰

![[Pasted image 20250225023439.png#pic_33center|]]

- 如果一根线是悬浮的（floating），那么它的串扰用耦合系数衡量：Agressor的总电容/Victim的总电容（注意还有其他平面）$$k_{\text{couple}}=\frac{2C_c}{2C_c+C_o}$$

![[Pasted image 20250225023459.png#pic_33center|]]

- 如果一根线接在源上，那么Victim的时间常数就很好计算：$$\tau=R\cdot\left(C_c+C_o\right)$$很好理解的一点就是：Aggressor线上的上升时间大于Victim时间常数的话串扰就会减少

## 耦合

![[Pasted image 20250225023642.png#pic_33center|这是耦合器]]
![[Pasted image 20250225023711.png#pic_50center|这是芯片中的耦合]]
- 必须知道的是：如果在AB线中产生了一个从A到B的信号，那么在CD线中耦合到的信号是从D到C的，也就是耦合信号与原信号的方向相反，并且耦合信号的持续时间与原信号的持续时间相同。

![[Pasted image 20250225024018.png#pic_50center|]]

- 如果使用分布参数来描述这一耦合，极其困难。上图展示了一种分布参数描述耦合的情况。在这种情况中，同时存在**互感**和**互容**两种耦合方法

![[Pasted image 20250225024211.png#pic_50center|]]

- 直接把上面那一堆乱七八糟的等效成一个$Z_m$. 要注意的是这个互阻抗$Z_m$是一个虚拟的阻抗，它并不在传输线中产生端口（也就意味着没有反射）
---
*这里是分析过程*
- 首先将电路图画成传输线的形式：
  ![[Pasted image 20250225024211.png#pic_50center|]]
  ![[Pasted image 20250225025509.png#pic_50center|等效电路图]]
  要注意的是，如蓝色箭头指示两边的电流各只有一个波前（单向的），这也就是等效电路中不将上部的传输线等效为并联两个$Z_0$的原因
  再一次强调$Z_m$是一个假想的电阻，接入电路不会产生反射，耦合波与入射波同时产生，所以老师说$Z_m$等效接入电路中点和$V_2$是电路中点的电压都是有点问题的。$V_2$真正的位置是与入射波的波前平行的位置（很绕，可以不用管）
- 将$V_x$左侧的传输线等效为电压为$V_1$的电压源（无耗传输线没有压降）与$Z_0$阻抗串联，$V_x$右侧等效为对地电阻$Z_0$，$V_2$左侧等效为对地电阻$Z_0$. 我们就得到了等效电路图：
  ![[Pasted image 20250225025408.png#pic_50center|]]
  直接应用基尔霍夫定律就能够求得：$$V_2=\frac{Z_m}{3\cdot Z_0+2\cdot Z_m}V_x$$$V_x$很好求，直接应用一下等效就能求得$$V_x=\frac{Z_0}{Z_0+Z_S}$$
- *并不严谨的分析，实际上根据HFSS的仿真结果，逻辑门D的位置会产生一个巨大的脉冲（再次体会我说的$V_2$的位置是与入射波波前平行的位置，这是不断叠加的结果）。但在这里我们假设耦合线中仅存在一条耦合波，并不计算这个叠加效应*
  那么如果我们要求得耦合线中逻辑门D的输入电压，就得等耦合波传播到逻辑门C的输入端后**反射**，再反向传播到逻辑门D，这一步比较好理解，最终的电压就是$$V_D=V_2\cdot \rho_C=V_2\cdot \frac{R_t-Z_0}{R_t+Z_0}$$其中$R_t$是逻辑门C的输出阻抗。
- 至此串扰分析完成。

# 去耦电容

![[Pasted image 20250225030759.png#pic_75center|]]
- 看这个图，在输出跳变时会产生额外的电流（Total Supply），去耦电容就是为了及时提供这个电流。
- 电容的电流表达式为：$$i=C\frac{\mathrm{d}v}{\mathrm{d}t}$$移项：$$C=i\frac{\mathrm{d}t}{\mathrm{d}v}\approx i\frac{\Delta t}{\Delta v}$$其中：
	- $\Delta t$是需要提供大电流的时间（e.g., $20\mathrm{nS}$）
	- $\Delta v$是电源允许的波动值（e.g., $0.1\mathrm{V}$）
	- $i$是转换期间需要的电流（e.g., $50\mathrm{mA}$）
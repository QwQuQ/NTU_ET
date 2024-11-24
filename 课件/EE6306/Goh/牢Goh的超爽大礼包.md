# Review of Integrated Circuit Fundamentals

## Characteristics of Digital Integrated Circuits

### Introduction（略）

### pn Junction & Diode Equation

[[Diode I-V Relation|Diode Equation]]

### The MOSFET Transistor

#### nMOS Operation

- Body一般接地
- 在Gate接低电压的时候
	- p型衬底的电压一般很低
	- Source-Body和Drain-Body形成的pn结一般都截止
	- 没有电流流过，晶体管截止
- 在Gate接高电压的时候
	- [[MOS Capacitors]]栅极上有正电荷
	- Body上积累负电荷
	- 栅极下方反型，成为n型半导体
	- 现在电流能够通过反型的n型半导体，从源极经过沟道流到漏极，晶体管导通

#### pMOS Operation

- 和nMOS类似但是掺杂和电压都反过来
- Body连接到高电压（$V_{DD}$）
- Gate低电压：导通
- Gate高电压：截止
- 器件符号中的泡泡表示这一反转的行为

#### MOS管的符号（略）

#### MOS(FET) Transistor As Switch

- nMOS可以等效成一个开关
- $V_{GS}>V_T$时，沟道在Source和Drain之间产生
- Source和Drain之间的电压差会让电流从这两个区域中流过
- $V_{GS}$调节沟道的电导率
- $V_{GS}<V_T$时，没有沟道存在，这个开关被视为开路

#### Threshold Voltage Concept

- [[Threshold Voltage]]

### Body-Bias Effects

- 到目前为止，我们忽略了 p 型衬底的存在。实际上，MOSFET 是一个四端器件，基板是器件的体（B）端。
- 当源极与体之间存在电压$V_{SBn}$时，nFET会产生体效应
- 增加任何类型器件的阈值电压（$V_T$）
- 在 MOS 集成电路中，有时将每个源极连接到基板是不切实际的。在这些情况下，由于体效应引起的可能的$V_T$偏移必须在电路设计中考虑。
- 负偏置会让$V_T$从0.45V上升到0.85V
- 由于这是反转沟道所需的栅极电压，如果源极电压增加，则连接到沟道的源极电压也会增加。
- 源极电压提高导致阈值电压升高也被称为体效应

- [[Body-Bias Effect]] Model

### I-V Relations – Linear & Saturation Modes

#### Transistor in Linear Mode

- $V_{GS}>V_T$
- $V_{DS}<V_{GS}-V_T$

- Channel Charge:$$Q_i(x)=-C_{ox}\left[V_{GS}-V(x)-V_T\right]$$
- 电流是漂移速度与电荷量的乘积，记得乘上沟道宽度W：$$I_D=v_{\text{n,drift}}(x)Q_i(x)W$$
- 电子漂移速度和电场强度和载流子迁移率有关：$$v_{\text{n,drift}}=-\mu_{n}\xi(x)=\mu_n\frac{\mathrm{d}V}{\mathrm{d}x}$$
- 结合上述式子，把分母移项：$$I_D\mathrm{d}x=\mu_nC_{ox}\left[V_{GS}-V(x)-V_T\right] \mathrm{d}V$$
  两边积分，根据顺子的说法还要级数展开。可以得到长沟道器件在线性区的表达式：$$I_D=k_n^\prime\frac{W}{L}\left[(V_{GS}-V_T)V_{DS}-\frac{V_{DS}^2}{2}\right]^2$$
  上式中：
	- $k_n^\prime$是[[Process Transconductance Parameter|工艺跨导参数]]
	- $k_n=k_n^\prime\frac{W}{L}$是[[Gain Factor]]

#### Transistor in Saturation Mode

- $V_{GS}>V_T$
- $V_{DS}>V_{GS}-V_T$

对于长沟道器件，沟道在：$$I_D^\prime=\frac{1}{2}k_n^\prime\frac{W}{L}(V_{GS}-V_T)^2$$
$$I_D=I_D^\prime(1+\lambda V_{DS})$$
上式中$\lambda$是沟道调制系数。

#### Current Determinates

- 源极到漏极的距离$L$
- 沟道宽度$W$
- 阈值电压$V_T$
- 栅氧厚度$t_{ox}$
- 栅氧的介电常数$\epsilon_{ox}$
- 载流子迁移率：
	- pMOS$\mu_p\approx180cm^2/V-\mathrm{sec}$
	- nMOS$\mu_n\approx500cm^2/V-\mathrm{sec}$
# MOS Transistor Theory

## MOS Capacitor

- 栅极和体形成了MOS电容
- 三种工作状态（比顺子少了Flatband）：
	- Accumulation
	  pMOSC情况下栅极施加负电压
	- Depletion
	  pMOSC情况下栅极施加正电压，但是界面附近的本征费米能级并未低于费米能级
	- Inversion
	  pMOSC栅极电压超过阈值电压，形成反型层


### Terminal Voltages

- $V_D$，$V_S$，$V_G$
- 一般来说$V_S<V_D$
- nMOS的body是接地的，所以第一步假设Source也接地


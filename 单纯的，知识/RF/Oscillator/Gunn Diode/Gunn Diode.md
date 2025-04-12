---
aliases:
  - Transferred Electron Device
  - 耿氏管
  - TED
tags:
  - rf
  - oscillator
---
参考：*半导体物理与器件，尼曼*

# 耿氏效应

在强电场作用下，半导体中的自由电子会从高迁移率的能带跃迁至低迁移率的能带中，这种现象为转移电子现象。

- 在低电场下，导带中的电子位于[[E-k Diagram|k空间图]]的低能谷区，电子的[[Density of States|态密度]]和[[Effective Mass|有效质量]]小导致电子**迁移率大**。
- 高能谷的能级比低能谷高，当电场强度高于阈值电场强度$E_{\text{th}}$时，电子获得能量从低能谷谷底转移到高能谷谷底。
- 高能谷的电子**态密度**和**有效质量**大，**迁移率小**。
- 电子的谷间转移导致随着电场强度的增加，电子的迁移率反而下降，导致了微分负迁移率。

- 条件：
	- $\Delta E>kT=0.026eV$，不然的话[[Thermal Voltage|热电压]]就会让电子跃迁到高能谷
	- $E_g>\Delta E$，不然的话加的电场会让半导体击穿

![[Pasted image 20250409224221.png#pic_75center|]]

# 耿氏二极管

![[Pasted image 20250409230340.png#pic_75center|]]

![[Pasted image 20250409230511.png#pic_75center|]]

- 工作在微分负电阻区的耿氏二极管会在**阴极Cathode**产生一个空间电荷区，由于微分电导此时是负的，所以这个空间电荷区并不会消失，而会向**阳极Anode**移动。（漂移速度相同时能够对应两个电场强度）
- 至此，耿氏二极管能够产生周期脉冲电流。
- 耿氏二极管的效率一般小于10%

- 振荡频率为：$$f=\frac{v_\text{s}}{L}$$
  其中：
	- $v_{\text{s}}$是载流子饱和漂移速度（Saturated Drift Velocity），对于GaAs器件来说$v_{\text{s}}\approx 10^7 \text{cm/s}$
	- $L$是器件长度


- 根据电场公式能够得出偏置电压为：$$V_{\text{Bias}}=E_{\text{th}} L$$
- 根据[[Current Density Equations|电流密度方程]]，只考虑漂移项，能够得到耿氏管截面积与偏置电流的关系为：$$I_{\text{Bias}}=A\times J=An_0 q v_{\text{s}}$$
	- 知道了截面积就能算半径了（耿氏管是圆的！不是方的！）

# 其他耿氏效应振荡器

-  Quenched domain mode
- Limited Space-Charge Accumulation mode，效率可达20%

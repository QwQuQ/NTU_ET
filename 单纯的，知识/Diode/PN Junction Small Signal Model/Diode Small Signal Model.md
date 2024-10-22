---
aliases:
  - 二极管小信号模型
tags:
  - analog
  - diode
  - pn_junction
---
![[Diode Small Signal Model.png|200]]

其中 $r_s$ 是实际存在的电阻，它会产生[[Thermal Noise|热噪声]]。 $r_d$ 是二极管的动态电阻，不会产生热噪声。二极管中电子的运动会产生[[Shot Noise|散粒噪声]]和[[Flicker Noise|粉红噪声]]，[[Burst Noise|突发噪声]]与他俩相比可以忽略。

二极管中，电流的表达式为：
$$I_D=I_s\left(e^{\frac{V_D}{\phi_T}}-1\right)$$
$V_D$是二极管两端的电压。正向偏置的电压降低势垒使二极管导通，反向电压使二极管势垒抬高截止

$\phi_T$为[[Thermal Voltage|热电压]]，$300K$时为$26mV$.

$I_S$是二极管的饱和电流
---
aliases:
  - PN结噪声模型
tags:
  - analog
  - semi_conductor
  - diode
  - pn_junction
---
根据[[Diode Small Signal Model|二极管小信号模型]]，$r_s$存在[[Thermal Noise|热噪声]]，PN结部分存在[[Shot Noise|散粒噪声]]、[[Flicker Noise|粉红噪声]]和[[Burst Noise|突发噪声]]. 其中散粒噪声和粉红噪声占主导作用。

$$\overline{v_s^2}=4kTr_s(\mathrm{V^2/Hz})$$

$$\overline{i^2}=2qI_D+k_1\left(\frac{I_D^a}{f}\right)+k_2\left(\frac{I_D^b}{1+\left(\frac{f}{f_c}\right)^2}\right)(\mathrm{A^2/Hz})$$
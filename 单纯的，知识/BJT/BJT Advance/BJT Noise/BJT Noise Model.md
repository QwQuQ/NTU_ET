---
aliases:
  - BJT噪声模型
---
![[BJT Small Signal Model.png|500]]

根据[[BJT Small Signal Model|BJT小信号模型]]，由于三极管内有两个PN结，所以存在两处[[Diode Noise Model|PN结噪声模型]]。但是CE结的[[Flicker Noise|粉红噪声]]被忽略了。 $r_{\pi}$ 和 $r_o$ 为PN结的动态电阻， $r_b$ 为输入电阻，物理意义上存在。所以可以得到三极管的噪声模型为：

$$\overline{v_b^2}=4kTr_b(\mathrm{V^2/Hz})$$

$$\overline{i_b^2}=2qI_B+k_1\left(\frac{I_B^a}{f}\right)+k_2\left(\frac{I_B^c}{1+\left(\frac{f}{f_c}\right)^2}\right)(\mathrm{A^2/Hz})$$

BE结中，仍然是[[Shot Noise|散粒噪声]]和[[Flicker Noise|粉红噪声]]占据主导地位，[[Burst Noise|突发噪声]]可以忽略。

$$\overline{i_c^2}=2qI_c(\mathrm{A^2/Hz})$$

CE结中，省略[[Flicker Noise|粉红噪声]]，仅保留[[Shot Noise|散粒噪声]]。
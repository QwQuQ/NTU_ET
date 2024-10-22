---
aliases:
  - MOSFET Saturation Region
  - MOSFET饱和区
  - 饱和区
---
对于场沟道器件，当$V_{GS}>$[[Threshold Voltage|阈值电压]]$V_T$且$V_{DS}>V_{GS}-V_T$时，MOS管在漏极处沟道夹断，进入饱和区。饱和区的电流计算公式为：

$$I_D^\prime=\frac{k_n^\prime}{2}\times\frac{W}{L}\times\left(V_{GS}-V_T\right)^2$$
$k_n^\prime$：[[Process Transconductance Parameter|工艺跨导参数]]

考虑$V_{DS}$引起的[[Channel-Length Modulation|沟道长度调制效应]]的电流为：

$$I_D=I_D^\prime\left(1+\lambda V_{DS}\right)$$

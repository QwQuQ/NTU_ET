---
aliases:
  - MOSFET线性区
  - 线性区
  - MOSFET Linear Region
---

![[MOSFET Linear Mode.png|400]]

# 推导
假设$V_{GS}$>[[Threshold Voltage|阈值电压]]$V_T$，$V_{DS}\leq V_{GS}-V_T$. 沿沟道的电压为$V(x)$，所以该点栅极到沟道的电压为$V_{GS}-V(x)$，假设这一电压一直大于$V_T$. 

[[Channel Charge|沟道电荷]]：

$$Q_i\left(x\right)=-C_{ox}\cdot\left[V_{GS}-V\left(x\right)-V_T\right]$$

电流等于[[Carrier Velocity|载流子漂移速度]]$\nu_n(x)$乘沟道电荷，根据电荷守恒，在整个沟道中这是一个常数。$W$为与沟道垂直的宽度。可以得到：

$$I_D=\frac{Q_{channel}}{t}=-\nu_n(x)Q_i(x)W$$

电子速度取决于电场和迁移率：

$$\nu_n=-\mu_n\xi(x)=\mu_n\frac{\mathrm{d}V}{\mathrm{d}x}$$

结合上述所有等式：

$$I_D\mathrm{d}x=\mu_nC_{ox}W\left(V_{GS}-V-V_T\right)\mathrm{d}V$$

对上式在沟道长度$L$上积分，可以得到MOS管的I-V关系。

# 线性区公式

当长沟道器件（L > 0.25 micron）$V_{DS}\leq V_{GS}-V_T$时，器件位于线性区，电流计算公式为：

$$I_D=k_n^\prime\left(\frac{W}{L}\right)\left[\left(V_{GS}-V_T\right)V_{DS}-\frac{V_{DS}^2}{2}\right]$$
$k_n^\prime$是[[Process Transconductance Parameter|工艺跨导参数]]。
$\mu_n$为[[Carrier Mobility|载流子迁移率]]
$k_n$是MOSFET的[[Gain Factor|增益系数]]

当$V_{DS}$比较小的时候，$V_{DS}$与$I_D$之间呈现线性关系，此时称为电阻区或者线性区
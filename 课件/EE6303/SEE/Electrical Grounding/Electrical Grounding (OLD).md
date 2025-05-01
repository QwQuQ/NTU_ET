---
aliases:
  - 接地
tags:
  - emi
  - 这个ppt做得真棒
  - 弃坑
---
# Exercise 1

An AC signal source of 5 V is connected to a $100\Omega$ resistive load through two parallel conductors separated by air as shown. The copper conductors have diameter of 5 mm and length of $2m$. The centre-to-centre spacing between conductors is 20 mm. Electrical properties of copper: $\sigma=5.8\times 10^7S/m$ and $\mu=4\pi\times10^{-7}H/m$, respectively. Determine the voltage across the load at 50Hz and 5MHz.

## Solution

### 计算趋肤深度
根据[[Skin Effect]]的表达式：

$$\delta=\frac{1}{\sqrt{\pi f \sigma\mu}}$$
根据给定的数据，可以计算得到：

| f    | d                   |
| ---- | ------------------- |
| 50Hz | 9.35mm              |
| 5Mhz | $29.55\mu \text{m}$ |

### 计算导线电阻

由于导线的直径为5mm，所以50Hz时趋肤深度大于半径2.5mm。带入电阻的计算公式：$$R=\frac{l}{\sigma \pi r^2}=$$ 
在5MHz时需要考虑趋肤效应：$$R=\frac{1}{2\pi r \sigma \delta}=$$

### 计算导线电感

50Hz时需要考虑导线的自感：$$L=4\times 10^{-7}ln\left(\frac{D-r}{0.7788r}\right)$$

5MHz时不需要考虑线材的自感：$$L=4\times 10^{-7}ln\left(\frac{D-r}{r}\right)$$

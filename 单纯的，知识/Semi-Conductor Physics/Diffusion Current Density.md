---
aliases:
  - 扩散电流密度
---
在有载流子浓度梯度的情况下，载流子会自发地从高浓度向低浓度扩散，直到恢复平衡。
对于电子$$J_{n,Diffusion}=qD_n\frac{\mathrm{d}n}{\mathrm{d}x}$$
对于空穴$$J_{p,Diffusion}=-qD_p\frac{\mathrm{d}p}{\mathrm{d}x}$$
上式中$D_n$和$D_p$为电子和空穴的扩散常数，并且$J_n$和$J_p$的符号不同。

# 推导：
在$t-\tau$时刻，位于$x-l$的电子经过时间$\tau$后，于$t$时刻到达了位于$x$的平面。所以可以得到$$J_-=qn\left(x-l\right)\frac{v_{th}}{2}$$
同理可以得到$$J_+=qn\left(x+l\right)\frac{v_{th}}{2}$$
其中$v_{th}$为载流子热运动的平均速度。
经过泰勒展开，可以得到$$J_{Diffusion}=q v_{th}l\frac{\mathrm{d}n}{\mathrm{d}x}$$
可以得出扩散电流密度与浓度梯度成正比。
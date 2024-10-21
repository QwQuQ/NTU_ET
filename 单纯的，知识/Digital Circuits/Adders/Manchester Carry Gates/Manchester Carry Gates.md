---
aliases:
  - 曼彻斯特进位链加法器
tags:
  - Adder
---
# 静态逻辑实现

![[Pasted image 20241021214522.png]]

[[Transmission–Gate-Based Adder|传输门型加法器]]中的进位传播电路可以通过增加进位产生和进位消除信号来简化。
- 进位传播路径不充电，如果进位传播信号$P=(A_i\oplus B_i)=1$，则$C_i$被传送至输出$C_o$
- 如果传播条件不满足，则输出由信号$D_i$下拉或$\overline{G_i}$上拉。

# 动态逻辑实现

![[Pasted image 20241021214211.png]]

使用动态实现可以让电路更加简洁。由于动态电路中的晶体管是单方向工作的，所以可以只用NMOS传输管来代替传输门。预充电输出使电路不再需要进位取消信号（对于进位链，传播的是进位信号的反信号时的情景）。



# 表达式

carry delete:
$$D=\overline{A}\cdot\overline{B}$$

carry propagate:
$$P=A\oplus B$$

carry generate:
$$G=A\cdot B$$

$$C_o=G_i+P_iC_i$$

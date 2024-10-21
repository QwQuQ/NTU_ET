---
aliases:
  - 曼彻斯特进位链加法器
tags:
  - adder
  - digital_circuits
---
[[Transmission–Gate-Based Adder|传输门型加法器]]中的进位传播电路（进位链）可以通过增加进位产生和进位消除信号来简化。需要添加产生中间信号的电路。

# 静态逻辑实现

![[Static Manchester Carry Gates.png]]

- 进位传播路径不充电，如果进位传播信号$P=(A_i\oplus B_i)=1$，则$C_i$被传送至输出$C_o$
- 如果传播条件不满足，则输出由信号$D_i$下拉或$\overline{G_i}$上拉。

# 动态逻辑实现

![[Dynamic Manchester Carry Gates.png]]

使用动态实现可以让电路更加简洁。由于动态电路中的晶体管是单方向工作的，所以可以只用NMOS传输管来代替传输门。预充电输出使电路不再需要进位取消信号（对于进位链，传播的是进位信号的反信号时的情景）。

# 表达式

[[Full Adder|全加器]]的中间信号：
carry delete:
$$D=\overline{A}\cdot\overline{B}$$

carry propagate:
$$P=A\oplus B$$

carry generate:
$$G=A\cdot B$$

$$C_o=G_i+P_iC_i$$

# 动态逻辑中间信号产生电路

![[Dynamic Implementation of P and G.png]]
上图的电路中使用一个[[Bleeder]]来补偿[[Dynamic Logic|动态逻辑]]中由于[[Charge Leakage|电荷泄露]]导致的电荷损失。
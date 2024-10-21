---
aliases:
  - 曼彻斯特进位链加法器
tags:
  - Adder
---
# 动态逻辑实现

[[Transmission–Gate-Based Adder|传输门型加法器]]中的进位传播电路可以通过增加进位产生和进位消除信号来简化。使用动态实现可以让电路更加简洁。由于动态电路中的晶体管是单方向工作的，所以可以只用NMOS传输管来代替传输门。预充电输出使电路不再需要进位取消信号（对于进位链，传播的是进位信号的反信号时的情景）。


# 表达式

carry delete:
$$D=\overline{A}\cdot\overline{B}$$

carry propagate:
$$P=A\oplus B$$

carry generate:
$$G=A\cdot B$$

$$C_o=G_i+P_iC_i$$

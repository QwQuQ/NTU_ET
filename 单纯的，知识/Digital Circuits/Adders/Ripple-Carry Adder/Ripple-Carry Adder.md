---
aliases:
  - 行波进位加法器
  - 逐位进位加法器
tags:
  - adder
  - digital_circuits
---
![[Ripple-Carry Adder.png]]

N位加法器可以把N个1位的[[Full Adder|全加器]]串联起来。进位必须从最低有效位LSB一直波动到最高有效位MSB

- Ripple-Carry Adder is simple but suffer from long delay, specially when n is large.

# 延时

最坏情况：在LSB上产生了一个进位，其他位不产生进位而是传播这一进位。所以延时为：$$t_{adder}=(n-1)\times t_{carry}+t_{sum}$$
上式中：
$t_{carry}$为$c_i$到$c_o$的传播延时
$t_{sum}$为$c_i$到$s$的传播延时
## 例子

8bit逐位进位加法器的最差情况：
$$a+b=01111111b+00000001b=10000000b$$

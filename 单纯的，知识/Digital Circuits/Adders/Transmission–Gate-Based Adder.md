---
aliases:
  - 传输门型加法器
tags:
  - Adder
---
全加器可以用多路开关和XOR门设计，
# 表达式
中间值：
$$P=A \oplus B$$
结果：
$$S=P\oplus C_i=\overline{\overline{P}\ \overline{C_i}+PC_i}$$
$$C_o=AB+PC_i=\overline{\overline{P}\ \overline{A}+P\overline{C_i}}$$
# 特点
- 和与进位输出有近似的延时
---
aliases:
  - 互补CMOS全加器
tags:
  - adder
  - digital_circuits
---
由[[Full Adder|全加器]]改进而来。
# 表达式
$$c_o=ab+bc_i+ac_i$$
$$s=a\oplus b \oplus c_i=abc_i+\overline{c_o}(a+b+c_i)$$
# 缺点
- The Complementary Static CMOS full adder cell has 28 transistors.
- It is large and slow.
- PMOS stacks are in carry and sum part.
- Intrinsic capacitance of co is large: 6 [[Gate Capacitance]] + 2 [[Diffusion Capacitance]] + Interconnect Capacitance.
- Carry propagates through 2 inverting stages.
- Sum output requires extra logic (although not critical).

# 改进
利用加法器的反向特性，我们可以隔一个移除进位链中的反相器。
![[Pasted image 20241021201112.png|400]]
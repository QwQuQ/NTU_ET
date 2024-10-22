---
aliases:
  - 有符号乘法
tags:
  - multiplier
  - digital_circuits
---
# 取反与负号之间的联系

对1个1位2进制数$a$取反后，可以得到：
$$\overline{a}=1-a\implies -a=\overline{a}-1$$
由此建立了取反与负数之间的关系

# 竖式计算

与无符号的[[Binary Multiplication|二进制乘法]]类似，有符号的二进制乘法主要区别为：在部分积相加时，在对应的位需要取反并减1.

![[Signed Multiplication_1.png]]
将减1项合并，随后取补码转化为加法
![[Signed Multiplication_2.png]]
将含有0的项舍去，只保留含有1的项
![[Signed Multiplication_3.png]]
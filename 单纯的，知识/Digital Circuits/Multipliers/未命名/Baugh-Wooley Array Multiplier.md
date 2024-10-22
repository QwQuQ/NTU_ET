---
aliases: 
tags:
  - multiplier
  - digital_circuits
---
# Baugh-Wooley算法

Baugh-Wooley算法是由Baugh和Wooley于1973年提出的二进制补码并行阵列相乘算法。该算法转化为等效并行阵列相加，其中每个部分和为乘数和被乘数比特相与，并且所有的部分和符号位为“+”。将n比特X，Y，乘法结果2n比特的P表示如下：
$$X=-x_{n-1}2^{n-1}+\left(\sum_{i=0}^{n-2}x_i\times 2^i\right)$$
$$Y=-y_{n-1}2^{n-1}+\left(\sum_{i=0}^{n-2}y_i\times 2^i\right)$$
$$\displaylines{
P=XY=x_{n-1}2^{n-1}\times y_{n-1}2^{n-1}+\left(\sum_{i=0}^{n-2}\sum_{j=0}^{n-2}x_iy_j\times 2^{i+j}\right)
\\
-2^{n-1}\left(\sum_{i=0}^{n-2}y_{n-1}x_i\times2^i\right)-2^{n-1}\left(\sum_{j=0}^{n-2}x_{n-1}y_j\times 2^j\right)
}$$

可以发现$P$能够分为4项，令：
- $C=x_{n-1}2^{n-1}\times y_{n-1}2^{n-1}$
- $D=\left(\sum_{i=0}^{n-2}\sum_{j=0}^{n-2}x_iy_j\times 2^{i+j}\right)$
- $A=2^{n-1}\left(\sum_{i=0}^{n-2}y_{n-1}x_i\times2^i\right)$
- $B=2^{n-1}\left(\sum_{j=0}^{n-2}x_{n-1}y_j\times 2^j\right)$

对$A$、$B$进行操作，由于二者操作相同，所以以$A$为例：

将A补零至2n位，方便在阵列中相加

| $2n-1$ | $2n-2$ |  $2n-3$   |  $2n-4$   | $\cdots$ |   $n$   |  $n-1$  | $n-2$ | $n-3$ | $\cdots$ | $0$ |
| :----: | :----: | :-------: | :-------: | :------: | :-----: | :-----: | :---: | :---: | :------: | :---: |
|  $0$   |  $0$   | $a_{i-2}$ | $a_{i-3}$ | $\cdots$ | $a_{1}$ | $a_{0}$ |  $0$  |  $0$  | $\cdots$ | $0$ |

对A取补码（取反加1）

| $2n-1$ | $2n-2$ |        $2n-3$        |        $2n-4$        | $\cdots$ |        $n$         |        $n-1$         | $n-2$ | $n-3$ | $\cdots$ | $0$ |
| :----: | :----: | :------------------: | :------------------: | :------: | :----------------: | :------------------: | :---: | :---: | :------: | :-: |
|  $1$   |  $1$   | $\overline{a_{i-2}}$ | $\overline{a_{i-3}}$ | $\cdots$ | $\overline{a_{1}}$ | $\overline{a_{0}}+1$ |  $0$  |  $0$  | $\cdots$ | $0$ |

同理可得$B$

所以$-(A+B)$的表达式为：
$$\displaylines{
-(A+B)=2^{2n-1}+2^{2n-2}+2^{n-1}\left(\sum_{i=0}^{n-2}\overline{a_i}\times 2^i\right) \\
+2^{2n-1}+
}$$
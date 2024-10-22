---
aliases:
  - 二进制乘法
tags:
  - digital_circuits
  - multiplier
---
![[Binary Multiplication.png]]
考虑$M$位二进制数$X$和$N$位二进制数$Y$：
$$X=\sum_{i=0}^{M-1}X_i2^i$$
$$Y=\sum_{j=0}^{N-1}Y_j2^j$$
它们的积可以表示为：
$$\displaylines{
Z=X\times Y=\sum_{k=0}^{M+N-1}Z_k2^k=\left(\sum_{i=0}^{M-1}X_i2^i\right)\left(\sum_{j=0}^{N-1}Y_j2^j\right) \\
=\sum_{i=0}^{M-1}\left(\sum_{j=0}^{N-1}X_iY_j2^{i+j}\right)
}
$$
上式中的：$\sum_{j=0}^{N-1}X_iY_j2^{i+j}$被称为[[Partial Products|部分积]]（Partial Products，PP）
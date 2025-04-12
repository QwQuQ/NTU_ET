---
aliases:
  - 单端口负阻抗振荡器
tags:
  - rf
  - oscillator
---
*参考文献：Foundations of Oscillator Circuit Design, Guillermo Gonzalez*

![[Pasted image 20250409214258.png#pic_50center|单端口负阻振荡器的电路]]

- 规定上图中：
	- $X_{\text{L}}\left(\omega\right)$：负载阻抗的虚部
	- $R_{\text{L}}\left(\omega\right)$：负载阻抗的实部
	- $Z_{\text{L}}$：负载复阻抗
	- $X_{\text{IN}}\left(\omega\right)$：源阻抗的虚部
	- $R_{\text{IN}}\left(\omega\right)$：源阻抗的实部
	- $Z_{\text{IN}}$：源复阻抗
	- $i\left(t\right)$：振荡电流的瞬时值
	- $v\left(t\right)$：振荡电压的瞬时值
	- $A$：振荡电流的幅度
	- $A_0$：稳定振荡时电流的幅度
	- $\omega$：振荡电流的角频率
	- $\omega_0$：稳定振荡时电流的角频率

# 振荡条件

- 阻抗的实部表示能量的增多或者减少，所以可以得到：
	- 起振条件：环路阻抗的实部小于0，输入能量$$R_{\text{IN}}\left(A,\omega\right)+R_{\text{L}}\left(\omega\right)<0$$
	- 稳定条件：环路阻抗的实部等于0，没有能量交换$$R_{\text{IN}}\left(A_0,\omega_0\right)+R_{\text{L}}\left(\omega_0\right)=0$$
- 阻抗的虚部表示电流与电压的相位差，在这里用于控制频率，在稳定振荡时：$$X_{\text{L}}\left(\omega_0\right)+X_{\text{IN}}\left(A_0,\omega_0\right)=0$$

# 负载阻抗的选择

- 做出近似，源阻抗的实部不随频率变化，并且与振荡电流的幅度$A$呈线性关系：$$R_{\text{IN}}\left(A,\omega\right)\approx R_{\text{IN}}\left(A\right)\approx-R_0\left(1-\frac{A}{A_M}\right)$$
  其中：
	- $A_M$：能够达到的最大振荡电流幅度
	- $R_0$：幅度为0时源阻抗的实部

- 交流电复功率的平均值：$$P=\frac{1}{2}\mathrm{Re}\left(V\cdot I^*\right)$$
  其中：
	- $I^*$是复电流的共轭复数
	- $V$是复电压
	- $1/2$将峰值电压电流转化为平均值
- 带入$$V=I\cdot R_{\text{IN}}\left(A\right)$$得到：$$\displaylines{P=\frac{1}{2}\mathrm{Re}\left(V\cdot I^*\right)=\frac{1}{2}\mathrm{Re}\left(I\cdot I^* \cdot R_{\text{IN}}\left(A\right)\right)=\frac{1}{2}\left|I\right|^2\left|R_{\text{IN}}\left(A\right)\right| \\ =\frac{1}{2}A^2 R_0\left(1-\frac{A}{A_M}\right)}$$
- 高中导数题，求导然后找极值点：$$\displaylines{\frac{\mathrm{d} P}{\mathrm{d} A}=\frac{1}{2}R_0\left(2A-\frac{3A^2}{A_M}\right)=0\implies A=\frac{2}{3}A_M \\ \implies \left\{\begin{eqnarray} R_{\text{IN}} =&-\frac{1}{3}R_0\\R_{\text{L}} =&\frac{1}{3}R_0\end{eqnarray}\right .}$$

# 反射系数

*用来找稳定性圆*

假设这个单端口网络与负载之间传输线的特征阻抗为$Z_o$

- 源的反射系数$$\Gamma_{\text{IN}}=\frac{Z_{\text{IN}}-Z_o}{Z_{\text{IN}}+Z_o}$$

- 负载的反射系数：$$\Gamma_{\text{L}}=\frac{Z_{\text{L}}-Z_o}{Z_{\text{L}}+Z_o}$$

- 在稳定振荡时有：$$Z_{\text{IN}}+Z_{\text{L}}=0$$所以有：$$\Gamma_{\text{IN}}\cdot\Gamma_{\text{L}}=1$$
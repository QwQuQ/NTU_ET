---
aliases:
  - 平衡载流子浓度
  - 热平衡载流子浓度
---

In silicon and other semiconductors,

conduction band:
	$$n_0=N_c\times exp\left(-\frac{E_c-E_F}{kT}\right)$$

valence band:
$$p_0=N_v\times exp\left(-\frac{E_F-E_v}{kT}\right)$$
$n_0$:[[Thermal Equilibrium|热平衡]]电子浓度
$p_0$:[[Thermal Equilibrium|热平衡]]空穴浓度
$N_c$:导带[[Effective Density of States|有效态密度]]
$N_v$:价带[[Effective Density of States|有效态密度]]
$E_F$:[[Fermi Level|费米能级]]
$k$:玻尔兹曼常数
$T$:开尔文温度

推导：
导带电子的浓度：[[Density of States|态密度]]乘状态被一个电子占据的几率（[[Fermi-Dirac Distribution|费米-狄拉克分布]]），单位体积内的表达式可以写成：
$$n=\int_{E_c}^{\infty}g\left(E\right)f_n\left(E\right)\mathrm{d}E$$
对[[Fermi-Dirac Distribution|费米-狄拉克分布]]使用玻尔兹曼近似变为[[Boltzmann Distribution|玻尔兹曼分布]]：
$$n=\int_{E_c}^{\infty}g\left(E\right)e^{-\frac{E_c-E_F}{kT}}$$
代入[[Density of States|态密度函数]]求解积分：
$$n=2\left(\frac{2\pi m_n^* kT}{h^2}\right)^{3/2}e^{-\frac{E_c-E_F}{kT}}$$
定义[[Effective Density of States|有效态密度]]为：$N_c=2\left(\frac{2\pi m_n^* kT}{h^2}\right)$，可以得到：
$$n=N_c\times e^{-\frac{E_c-E_F}{kT}}$$
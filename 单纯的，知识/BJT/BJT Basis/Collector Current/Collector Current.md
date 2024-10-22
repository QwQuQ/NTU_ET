---
aliases:
  - 集电极电流
tags:
  - BJT
  - analog
  - TODO
---

$$I_C=I_S e^{(V_{BE}/V_T)}$$
上式中的$V_T$为[[Thermal Voltage|热电压]]，$I_S$是二极管的饱和电流，在BJT中是一个晶体管常数。这个公式与[[Diode I-V Relation|PN结I-V关系]]很类似，因为BE结确实是一个PN结类似物。

# 推导

Since recombination can be ignored, we can integrate with respect to $x$ as
$$
\displaylines{
J_n\int_{0}^{W_B}\frac{p_p}{qD_nn_{ie}^2}\mathrm{d}x=\frac{n_pp_p}{n_{ie}^2}\Big|_{x=W_B}-\frac{n_pp_p}{n_{ie}^2}\Big|_{x=0} \\
n_p(0)=n_{p0}(0)exp\left(\frac{qV_{BE}}{kT}\right)\ , \\
n_p(W_B)=n_{p0}(W_B)\ll n_p(0) \\
\implies J_n\int_{0}^{W_B}\frac{p_p}{qD_nn_{ie}^2}\mathrm{d}x=-\frac{n_{p0}(0)p_p(0)}{n_{ie}^2(0)}exp\left(\frac{qV_{BE}}{kT}\right) \\
}$$

For a modern bipolar transistor, $p_p(0) \approx p_{p0}(0)$. Noting that $n_{p0}(0)p_{p0}(0) = n_{ie}^2(0)$, we can reduce the above to:
$$J_n=-\frac{q\cdot exp\left(\frac{qV_{BE}}{kT}\right)}{\int_0^{W_B}\frac{p_p}{D_n n_{ie}^2}\mathrm{d}x}$$
This electron current density is the source of the collector current.

From emitter area $A_E$, 
$$I_C=A_E\left|J_n\right|=A_E\left|J_C\right|$$
The collector current can be written as:
$$I_C=A_EJ_{C0}\cdot exp\left(\frac{qV_{BE}}{kT}\right)$$
where $J_{C0}$ is the saturated collector current density defined as $J_{C0} = \frac{qn_i^2}{G_B}$ and $G_B$ is the base Gummel number.
$$G_B=\int_0^{W_B}\frac{n_i^2}{n_{ieB}^2}\frac{p_p}{D_{nB}}\mathrm{d}x$$

- This definition of the Gummel number takes into account the effect of heavy doping in the base.
- Collector current is a function of base parameters only.
- Collector current does not depend on the properties of the emitter.
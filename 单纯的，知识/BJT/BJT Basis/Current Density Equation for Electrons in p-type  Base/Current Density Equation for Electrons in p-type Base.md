---
aliases: 
tags:
  - analog
  - BJT
---
From [[Current Density Equations]] and [[Einstein's Relation]]:
$$J_n(x)=-qn_p\mu_n\frac{\mathrm{d}\phi_n}{\mathrm{d}x}$$
Since the hole [[Quasi-Fermi Potential]] is approximately constant in the base, $\frac{\mathrm{d}\phi_p}{\mathrm{d}x}\approx0$
$$\implies J_n(x)\approx q n_p\mu_n\frac{\mathrm{d}(\phi_p-\phi_n)}{\mathrm{d}x}$$
From [[Heavy Doping Effect]], we have:
$$\phi_p-\phi_n=\frac{kT}{q}ln\left(\frac{p_pn_p}{n_{ie^2}}\right)$$
Substitute,
$$J_n(x)=qD_n\frac{n_{ie}^2}{p_p}\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{n_pp_p}{n_{ie}^2}\right)$$
for the electron current density in the base. $J_n$ is given in terms of the electron and hole concentrations in the base.
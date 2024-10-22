---
aliases:
  - 基极电流
tags:
  - BJT
  - analog
  - TODO
---
Base current have 3 components:
- the holes injected from the base into the emitter
- the holes that recombine in the quasineutral base region with the minority electrons injected from the emitter
- the holes that recombine with electrons within the base-emitter space-charge region

Since there is no electron [[Carrier Recombination]], the base current is just the hole injection current from base to emitter.
Due to [[Heavy Doping Effect]] in the emitter, $n_n\approx n_{n0}=N_E$, $N_E$: emitter doping density
$$J_p(x)=-qD_p\frac{n_{ie}^2}{n_{n0}}\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{n_{n0}p_n}{n_{ie}^2}\right)$$
Base current is a function of emitter parameters only. Base current is independent of the properties of the base region.


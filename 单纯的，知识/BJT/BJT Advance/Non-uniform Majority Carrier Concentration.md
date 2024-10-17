---
aliases:
---
对于NPN管，基区的多子是空穴，少子是电子。空穴不均匀分布的原因：
1. non-uniform doping profile during implant or diffusion
2. high level of minority injection from emitter (upset equilibrium)

考虑基区空穴的[[Quasi-Fermi Potential|准费米电势]]
$$\phi_p=\psi_i+\frac{kT}{q}ln\left(\frac{p_p}{n_i}\right)$$
移项：$$\psi_i=\phi_p-\frac{kT}{q}ln\left(\frac{p_p}{n_i}\right)$$
电场强度：$$
\displaylines{
E=\frac{\mathrm{d}\psi_i}{\mathrm{d}x} \\
\implies
E=\frac{kT}{q}\frac{1}{p_p}\frac{\mathrm{d}p_p}{\mathrm{d}x}-\frac{\mathrm{d}\phi_p}{\mathrm{d}x}
}
$$
可以证明$\frac{\mathrm{d}\phi_p}{\mathrm{d}x}$可以被忽略，所以$$E\approx\frac{kT}{q}\frac{1}{p_p}\frac{\mathrm{d}p_p}{\mathrm{d}x}$$
所以除非基区的掺杂是均匀的$\frac{\mathrm{p_p}}{\mathrm{d}x}=0$，否则基区内部将会存在一个电场。
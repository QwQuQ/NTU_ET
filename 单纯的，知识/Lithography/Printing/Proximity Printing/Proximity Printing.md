---
aliases: 
tags:
  - lithography
  - lithography_printing
  - single_exposure
---
# Proximity Aligner

![[Pasted image 20250211001745.png|Contact / Proximity Aligner]]

# Proximity Printing

![[Pasted image 20250210234036.png#pic_25center|Proximity Printing]]

- mask and wafer in close proximity (a small gap of $10-50\mathrm{\mu m}$ between mask and wafer), less damage by dust particles, the low resolution of the order of $2-5\mathrm{\mu m}$ due to the fringe.

## Diffraction in Proximity Printing

![[Pasted image 20250218154537.png#pic_75center|]]

- limited by Near Field (Fresnel) Diffraction
受到菲涅耳衍射的限制
- 产生条件：$$\lambda<g<\frac{W^2}{\lambda}$$
- Resolution is the minimum linewidth $W_{\text{min}}$ achievable by the lithography equipment. $$W_{\text{min}}\approx\sqrt{k_1\lambda g}$$ 其中： ^b617ab
	- $k_1$是一个常数，没有明确的物理学定义，为一个实验参数。其大小取决于光学系统和光刻胶的性质，一般是1
	- $\lambda$是曝光光源的波长
	- $g$是mask到wafer表面的间距，单位为$\mathrm{\mu m}$

- Mask and wafer are separated by a small gap of $2-20\mathrm{\mu m}$
掩模和晶圆之间分隔了一小段$2-20\mathrm{\mu m}$的间隙。
- The resulting diffraction pattern has several features
由此产生的衍射图样具有几个特征
	- Intensity rises gradually near the edges producing some resist exposure outside the mask edge
	  强度在边缘附近逐渐增加，导致掩模边缘外的一些光刻胶暴露。
	- Ringing in intensity distribution within the aperture
	  在光圈内的强度分布中出现振铃现象（有波动）。

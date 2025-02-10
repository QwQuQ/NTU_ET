# UV Light Spectrum and Resolution

## 大概是前置知识

### 波长和频率的关系（高中物理）

$$\lambda=\frac{c}{f}$$
- $v$是光速$3\times 10^8 \mathrm{m\cdot s^{-1}}$，$f$的单位是赫兹，$\lambda$的单位是$\mathrm{m}$

### 光谱

- Most resists react with visible UV
  大多数光刻胶与可见紫外光发生反应。

- Common UV wavelengths used in optical lithography
	- DUV: Deep Ultraviolet ($\lambda=248\mathrm{nm}$)
	- VUV: Vacuum Ultraviolet
	- EUV: Extreme Ultraviolet

### Resolution

- 更高的Resolution总是更好的
- Resolution是在晶圆上区分两个紧邻特征的能力
- Feature Size是形成了的图案的实际尺寸
- 最小的Feature Size是Critical Dimension (CD)
- Resolution is important for critical dimension

（怎么感觉都是废话）

### Light Intensity

- Higher intensity = Shorter exposure time
- Lower intensity = Longer exposure time
- KrF laser is preferred over Hg lamp DUV. 看图，KrF激光的Light Intensity在DUV上对比水银灯更强

（又都是废话）

## Excimer Laser （准分子激光）

- Deep UV by excimer lasers
  图上说准分子激光能够覆盖EUV到DUV
- $Kr+NF_3+(\text{energy})\rightarrow KrF+(\text{photon emission})$
- KrF（氟化氪）: $\lambda=248\mathrm{nm}$, (CD: $\leq 0.25 \mathrm{\mu m}$)
- ArF（氟化氩）: $\lambda=193\mathrm{nm}$, (CD: $\leq 0.18\mathrm{\mu m}$)
- $F_2$ （氟）： $\lambda=157\mathrm{nm}$, (CD: $\leq0.15\mathrm{\mu m}$)

## Mercury Arc Lamp（汞弧灯；水银灯！）

- 汞蒸气灯：玻璃灯中有汞的等离子体
- 产生许多不同波长的光
- 光强比较有限
- 图上说能够覆盖DUV、Mid-UV和紫光

- "g" line: $\lambda=436\mathrm{nm}$ (used to mid 1980s); Critical Dimension Resolution (µm): $0.5\mathrm{\mu m}$
- "h" line: $\lambda=405\mathrm{nm}$; Critical Dimension Resolution (µm): $0.4\mathrm{\mu m}$
- "i" line: $\lambda=365\mathrm{nm}$ (early 1990s, $>0.3\mathrm{\mu m}$); Critical Dimension Resolution (µm): $0.35\mathrm{\mu m}$
- DUV(Deep Ultraviolet): ($\lambda=248\mathrm{nm}$); Critical Dimension Resolution (µm): $0.25\mathrm{\mu m}$

# Negative and Positive Lithography

## Resist

- Resist是一种对光敏感的聚合物

- Positive Resist
  被光照射后可以溶解
- Negative Resist
  没被光照的可以溶解

- 主要功能
	- 保护下方的薄片（ie. $\mathrm{SiO_2}$、$\mathrm{Al}$、polysilicon、$\mathrm{Si_3 N_4}$）免受蚀刻
	- 描出金属接触和薄膜沉积的窗口
	- 在选择性离子注入中防止离子进入穿透进下方的硅
	- 利用剥离工艺在衬底上形成金属图案

### Lift-off Process

![[Pasted image 20250203144059.png#pic_center|Lift-off Process]]

1. 基板被涂覆上光刻胶，然后通过带有所需图案的掩模使光刻胶曝光
2. 显影光刻胶以在基板上获得所需图案
3. 金属薄膜被沉积到带有光刻胶图案的基板上
4. 沉积在光刻胶上的金属被移除（通常使用丙酮），金属图案将被保留在衬底上

- 在Microstructuring Technology中，Lift-off Process是一种在衬底上使用可被牺牲的材料创建目标材料图案的技术
- Lift-off Process是对更传统的减材技术如蚀刻而言的补充。

## Negative Lithography

![[Pasted image 20250203145109.png|Negative Lithography]]

## Positive Lithography

![[Pasted image 20250203145046.png|Positive Lithography]]

# Eight Basic Steps of the Lithography Process

0. Vapour Prime Pre-Step-[[Dehydration Bake]]
1. [[Vapour Prime]]
2. [[Spin Coat]]
3. [[Soft Bake]]
4. [[Alignment and Exposure]]
5. [[Post-Exposure Bake]]
6. [[Developing]]
7. [[Hard Bake]]
8. [[Develop Inspect]]

# Lithography Equipment

## Aligners

- Single Exposure:
	- Contact Aligner
	- Proximity Aligner

![[Pasted image 20250211001745.png|Contact / Proximity Aligner]]

- Multiple Exposure
	- Step-and-Repeat Aligner (Stepper)

![[345678.png|Step-and-Repeat Projection Aligner]]

## UV Exposure / Printing

- UV exposure is sometimes known as “printing” because it “prints” the desired pattern onto the substrate using UV source.
- Single Exposure:
	- Contact Printing: mask and wafer in direct contact, high resolution of the order of 1µm, the problem with dust particles.
	- Proximity Printing: mask and wafer in close proximity (a small gap of $10-50\mathrm{\mu m}$ between mask and wafer), less damage by dust particles, the low resolution of the order of $2-5\mathrm{\mu m}$ due to the fringe.
![[Pasted image 20250210233638.png#pic_center|Contact Printing]]
![[Pasted image 20250210234036.png#pic_25center|Proximity Printing]]
- Multiple Exposures:
	- Projection Printing: 
		- **Reticle**: May contain the pattern of one or more die.
		- **Projection Lens**: Reduces the size of reticle field to be printed onto the wafer surface
		- **Single Field Exposure**: Includes focus, align, expose, step, and repeat process
		- Wafer stage controls the position of the wafer in $\mathrm{X}$, $\mathrm{Y}$, $\mathrm{Z}$, and $\mathrm{\theta}$
![[1t6437851415.png#pic_75center|Projection Printing]]

# Resolution and its Critical Parameters

## Minimum Linewidth / Resolution for Proximity Aligner

![[1274608581.png#pic_center|Proximity Aligner]]

- Resolution is the minimum linewidth achievable by the lithography equipment.
- Minimum linewidth (Resolution) for the proximity printer: $$W_{\text{min}}\approx \sqrt{k_1\lambda g}$$ 其中：
	- $k_1$是一个常数，没有明确的物理学定义，为一个实验参数。其大小取决于光学系统和光刻胶的性质，一般是1
	- $\lambda$是曝光光源的波长
	- $g$是mask到wafer表面的间距，单位为$\mathrm{\mu m}$

## Minimum Linewidth / Resolution for Projection Aligner

![[Pasted image 20250211004807.png#pic_75center|Projection Printing]]
- In projection aligner (also called step-and-repeat aligners), the gap between mask and wafer is very large (in the range of cm).
- Minimum linewidth (resolution) for the projection printer can be calculated using: $$W_{\text{min}}\approx k_1\frac{\lambda}{NA}$$
	- 其中$NA$为numerical aperture

### Numerical Aperture

![[Pasted image 20250211004807.png#pic_75center|Projection Printing]]

- The numerical aperture (NA) of an optical system is a measure of the ability to collect light, which is a measure of the light gathering power.
- Numerical Aperture, (NA) can be defined as: $$NA=n\mathrm{sin}\theta$$其中：
	- $n$为系统所浸没的介质的折射率，如果是空气的话$n=1$
	- $\theta$为物镜的接受角的一半
- 当$n=1$的时候，$NA$可以被定义为：$$NA=\mathrm{sin}\theta\approx\mathrm{tan}\theta=\frac{d/2}{f}=\frac{d}{2f}$$
	- 当$\theta < 12\degree$时$\mathrm{tan}\theta\approx\mathrm{sin}\theta$
	- 所以投影物镜的数值孔径也是孔径和焦距之间的几何比。

# Mask and Reticle
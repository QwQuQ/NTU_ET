# UV Light Spectrum and Resolution

## 大概是前置知识（废话们）

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

### Light Intensity

- Higher intensity = Shorter exposure time
- Lower intensity = Longer exposure time
- KrF laser is preferred over Hg lamp DUV. 看图，KrF激光的Light Intensity在DUV上对比水银灯更强

## Excimer Laser （准分子激光）

- Deep UV by excimer lasers
  图上说准分子激光能够覆盖EUV到DUV
- $Kr+NF_3+(\text{energy})\rightarrow KrF+(\text{photon emission})$
- KrF（氟化氪）: $\lambda=248\mathrm{nm}$, (CD: $\leq 0.25 \mathrm{\mu m}$)
- ArF（氟化氩）: $\lambda=193\mathrm{nm}$, (CD: $\leq 0.18\mathrm{\mu m}$)
- $F_2$ （氟）： $\lambda=157\mathrm{nm}$, (CD: $\leq0.15\mathrm{\mu m}$)

## Mercury Arc Lamp（汞弧灯；水银灯）

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
	- Protect underlying films such as $\mathrm{SiO_2}$, $\mathrm{Al}$, polysilicon, $\mathrm{Si_3N_4}$ etc. from etching
	  保护下方的薄片（ie. $\mathrm{SiO_2}$、$\mathrm{Al}$、polysilicon、$\mathrm{Si_3 N_4}$）免受蚀刻
	- Define windows for metal-contact and thin film deposition
	  描出金属接触和薄膜沉积的窗口
	- Prevent ions from penetrating the underlying $\mathrm{Si}$ during selective ion implantation
	  在选择性离子注入中防止离子进入穿透进下方的硅
	- Lift-off process used to create metal patterns on the substrate
	  利用剥离工艺在衬底上形成金属图案

### Lift-off Process

- Lift-off process used to create metal patterns on the substrate
  利用剥离工艺在衬底上形成金属图案
![[Pasted image 20250203144059.png#pic_center|Lift-off Process]]

1. The substrate is coated with resist. Then the resist is exposed through a mask with the desired pattern
   衬底被涂覆上光刻胶，然后通过带有所需图案的掩模使光刻胶曝光
2. The resist is developed to obtain the desired pattern on the substrate
   显影光刻胶以在衬底上获得所需图案
3. The metal film is deposited onto the resist-patterned substrate
   金属薄膜被沉积到带有光刻胶图案的衬底上
4. The metal-deposited resist is removed (acetone is usually used). The metal pattern will remain on the substrate.
   沉积在光刻胶上的金属被移除（通常使用丙酮），金属图案将被保留在衬底上

- 在Microstructuring Technology中，Lift-off Process是一种在衬底上使用可被牺牲的材料创建目标材料图案的技术
- Lift-off Process是对更传统的减材技术如蚀刻而言的补充。

## Negative Lithography

![[Pasted image 20250203145109.png|Negative Lithography]]
- 没曝光的地方被溶解

## Positive Lithography

![[Pasted image 20250203145046.png|Positive Lithography]]
- 曝光的地方被溶解

# Eight Basic Steps of the Lithography Process

[[Lithography Process]]

# Lithography Equipment

## Aligners

- Single Exposure:
	- [[Contact Printing#Contact Aligner|Contact Aligner]]
	- [[Proximity Printing#Proximity Aligner|Proximity Aligner]]

- Multiple Exposure
	- [[Projection Printing#Step-and-Repeat Aligner (Stepper)|Step-and-Repeat Aligner (Stepper)]]

## UV Exposure / Printing

- UV exposure is sometimes known as “printing” because it “prints” the desired pattern onto the substrate using UV source.
- Single Exposure:
	- [[Contact Printing]]
	- [[Proximity Printing]]

- Multiple Exposures:
	- [[Projection Printing]]

# Resolution and its Critical Parameters

- [[Proximity Printing#^b617ab|Resulution for Proximity Aligner]]
- [[Projection Printing#^d1580e|Resolution for Projection Aligner]]

# Lithography on Uneven Surface

[[Projection Printing#Depth of Focus|Depth of Focus]]

# Mask and Reticle

- Mask
	- Single Exposure; 1:1 Mask
	  单次曝光，1:1的图案
	- Pattern for a Complete Wafer
	  覆盖整一个wafer
- Reticle
	- Multiple Exposure: Reticle (Typically 4:1)
	  多次曝光，一般比例是4:1
	- Pattern for Only Part of the Wafer
	  只覆盖wafer的一部分
	- Reduced Size Pattern
	  将图案尺寸缩小
	- Achieve Higher resolution
	  能够获得更高的精度
- Mask和Reticle的需求
	- Flat, highly polished
	- One surface of glass is patterned with opaque chromium
	  玻璃的表面镀有不透光的铬
	- High degree of transparency for optimal usage, better exposure, higher transmitted power to PR
	  光学级的透明度，更适用于曝光，能把更多的能量传递给光刻胶（PR）

# Diffraction in Optical Lithography

- Diffraction occurs when light passes through a narrow opening or past a sharp edge.
  当光穿过狭窄的开口或经过锐利的边缘时，会发生衍射。
- Diffraction is the spread of light radiation light propagates in waves.
  衍射是光辐射在波动中传播的扩散现象
- Modern lithography tools are limited by the spreading of light (and not their optical elements)
  现代光刻工具受限于光的扩散（而不是其光学元件）
- Aperture will create a diffraction pattern that will divert some of the light from its desired path, thereby decreasing the quality of the image
  孔会产生衍射图样，使部分光线偏离其预定路径，从而降低图像质量。
- Interference patterns occur along the edge of the opening, causing a fuzzy image rather than the expected sharp edge that occurs between light and shadow.
  干涉图样沿着边缘的开口出现，导致图像出现模糊，并不会产生预期中光与影之间的锐利边缘。
- Diffraction patterns rob exposure energy and scatters it, leading to exposure of unwanted areas of the resist
  衍射图案损耗并散射曝光的能量，导致在光刻胶的非预期位置曝光
- Light diffraction is a concern in photolithography because of the extremely small patterns of sharp edges and narrow spaces on reticles.
  在光刻中，光的衍射是一个问题，因为掩模上的极小图样包含锐利边缘和狭窄间隙。

- Limited cases
	- [[Fresnel Diffraction|Near Field]]
	- [[Fraunhofer Diffraction|Far Field]]

![[Pasted image 20250218153835.png#pic_75center|衍射的形式]]![[Pasted image 20250221042019.png#pic_75center|衍射的形式]]

- Type of spreading depends on mask wafer separation:
	- Hard contact: (Almost) no diffraction
	- Proximity: [[Fresnel Diffraction|菲涅耳衍射]]
	- Projection:[[Fraunhofer Diffraction|夫琅和费衍射]]

- [[Contact Printing#Diffraction in Contact Printing|Diffraction in Contact Printing]]
- [[Proximity Printing#Diffraction in Proximity Printing|Diffraction in Proximity Printing]]
- [[Projection Printing#Rayleigh Criterion for Resolution|Diffraction in Projection Pringing]]

# Modulation Transfer Function (MTF) of the system

[[Modulation Transfer Function|MTF]]

# Resist critical modulation transfer function (CMTF)

[[Resist#Critical Resist Modulation Transfer Function (CMTF)|CMTF]]


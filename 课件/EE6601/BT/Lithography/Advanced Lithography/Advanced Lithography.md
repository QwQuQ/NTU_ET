# Optical Enhancement Techniques

## Improvement in Resolution

- 改善分辨率：$$W_{\text{min}}=k_1 \frac{\lambda}{NA}$$
	- 减小波长$\lambda$
	- 加大[[Projection Printing#Numerical Aperture|NA]]
	- 减小$k_1$，这是个经验参数
		- 改进mask，Critical Dimension (CD) control and phase shift masks
		- Resolution Enhancement Techniques (RET)
- 改善分辨率中带来的[[Projection Printing#Depth of Focus (DOF)]]问题：$$\text{DOF}=k_2 \frac{\lambda}{NA^2}$$
	- 数值孔径提升，DOF下降
	- 波长缩短，DOF下降
	- $k_2$下降（$k_2$与$k_1$有关系），DOF下降
- Nevertheless, wafers are made of PLANAR (very flat surface) with Chemical Mechanical Polishing (CMP) which allow the lithography systems to work with smaller DOF, resolving DOF issue
  然而，通过化学机械抛光（CMP）处理，使晶圆的表面非常平坦（PLANAR），从而使光刻系统能够在更小的景深（DOF）条件下工作，解决了景深问题。

## Diffraction in Lithography

你可真是个废话大王，不是吗？
- [[Lithography Technology#Diffraction in Optical Lithography|Diffraction in Optical Lithography]]
- [[Fresnel Diffraction]]
- [[Fraunhofer Diffraction]]
- [[Proximity Printing#Diffraction in Proximity Printing|Diffraction in Proximity Printing]]
- [[Projection Printing#Rayleigh Criterion for Resolution|Diffraction in Projection Printing]]
- We can adopt optical enhancement techniques such as Optical Proximity Correction (OPC), Phase-Shift Masks (PSM) and Off-Axis Illumination (OAI)
  我们可以采用光学增强技术，例如光学邻近校正（OPC）、移相掩模（PSM）和离轴照明（OAI）

## Phase Shift Mask (PSM)

![[Pasted image 20250221042204.png#pic_75center|]]
- Phase-Shift Mask (PSM) is a method used to overcome problems associated with light diffraction through small openings patterned on the reticle.
  PSM是一种用于解决光通过在掩模上印制的小孔时产生的衍射问题的方法
- With PSM, the reticle is modified with an additional transparent layer so that alternating clear regions cause the light to be phase-shifted 180°. This causes destructive interference, where light diffracted into the nominally dark area on the left will encounter destructive interference with light diffracted from the right clear area.
  使用PSM时，掩模会被修改添加一个额外的透明层，使交替的透明区域使光的相位发生180°的变化。这会导致相消干涉，即左侧灰色区域中的光遇到与从右侧区域衍射的光发生相消干涉。
---
- 减小了最小线宽，所以系统的$k$值减小了

## Optical Proximity Correction (OPC)

![[Pasted image 20250221042818.png#pic_75center|一些特征的位置]]
![[Pasted image 20250221042924.png#pic_50center|]]
- High-frequency components of the diffracted light are lost for finite NA of lenses. **Ends and bows of narrow lines are not ideal**
  由于透镜有限的数值孔径（NA），衍射光的高频成分会丢失。**窄线条的端部和弯曲部分并不理想**
- Use of optical proximity correction (OPC) in the mask design. This is another approach to design a better mask (e.g. clever mask engineering based on software algorithms) can also improve resolution significantly
  在掩模设计中使用OPC。这是优化掩模的另一种方法（例如基于软件算法的精巧掩模工程），也可以显著提高分辨率
- The approach involves adding extra features to the mask, usually at corners where features are sharp, to compensate for the high-frequency information lost due to diffraction effects
  这种方法在掩模上引入额外的特征，位置一般在角落这种尖锐处，以补偿由于衍射导致的高频细节丢失

## Off-Axis Illumination (OAI)

![[Pasted image 20250221043131.png#pic_75center|]]
- If the incident light source is illuminated at an angle with respect to the lens system (off-axis), higher order diffracted rays can be collected using the lens of the same size.
  如果入射光源以一定角度角度照射（离轴），则可以使用相同尺寸的透镜收集更高阶的衍射光线

- This allows the optical system to capture some of the higher order diffracted light, and hence can improve resolution
  这使得光学系统能够捕捉到一些高阶衍射光，从而可以提高分辨率
- OAI has the incident exposure light that strikes the mask at an angle in order to align diffraction fringes with the lens
  OAI使入射曝光光以一定角度打在掩模上，以便将衍射条纹与透镜对齐。

# Immersion Lithography

![[Pasted image 20250221164806.png#pic_75center|Immersion Lithography]]

## 第一种

- Same lens column design
  相同的透镜设计：保持NA不变$$NA=n^\uparrow \mathrm{sin}\theta^{\downarrow}$$
- Maintain resolution
  由于NA不变，所以分辨率也不变

![[Pasted image 20250221165055.png#pic_75center|Improvement in DOF]]

- Improve [[Projection Printing#Depth of Focus (DOF)|DOF]]
  $$\sigma^\uparrow=\frac{n^\uparrow}{2}k_1\frac{\lambda}{NA^2}$$所以DOF改善了

## 第二种

- Modified lens column: Hyper-NA ($> 1.0$), Exit angle $\theta$ of the lens for exposure does not change
  NA变大：$$NA^\uparrow=n^\uparrow\mathrm{sin}\theta$$
- Higher resolution$${W_{\text{min}}}^\downarrow=\frac{k_1\lambda}{n^\uparrow\mathrm{sin}\theta}$$

- Lower DOF$$\sigma^\downarrow=\frac{\cancel{n}}{2}k_1\frac{\lambda}{n^{\cancel 2}\mathrm{sin}^2\theta}=\frac{\lambda k_1}{2n^\uparrow\mathrm{sin}^2\theta}$$

# X-ray Lithography

![[Pasted image 20250221171519.png#pic_75center|]]

- $\lambda\sim 1\mathrm{\mu m}$ (extremely short wavelength for high resolution)
  极短波长实现高分辨率
- X-rays are produced by synchrotron radiation in a high energy electron storage ring.
  X射线通过高能电子储存环中的同步辐射产生
- Contamination becomes less of a concern because X-rays will penetrate most dust particles (low atomic number)
  污染变得不那么重要，因为X射线会穿透大多数尘埃颗粒（低原子序数）
- No need for vacuum (little absorption of X-ray by air)
  不需要真空（空气极少吸收X射线）
- No lens (transmission or reflection), because for Xray, refractive index $n=1$; thus only [[Proximity Printing]]
  没有透镜（传输或反射），因为对于X射线，折射率$n=1$；因此只能进行[[Proximity Printing]]
- Proximity printing can still achieve high resolution ($< 30\mathrm{nm}$) due to small $\lambda$.

- 优点：
	- High resolution
	- Reduced diffraction effect
- 缺点：
	- Expensive X-ray source
	- Absorption problem (mask)
	- Shadowing errors
	- Non-monochromatic X-ray source
	  X射线源并不单色
	- Low throughput
	  产率低

# EUV Lithography


| Immersion (ArFi)       | EUV                                |
| ---------------------- | ---------------------------------- |
| Water in scanner       | High vacuum                        |
| Materials Interactions | New wavelength ($13.5\mathrm{nm}$) |
| Hyper-NA ($>1$)        | Reflective optics                  |
| Same wavelength        | New mask                           |
| Same masks             | No pellicle<br>掩模保护膜               |
| Same resists           | New resists                        |
> Mask Pellicle是一种透明的薄膜，在生产中覆盖在掩膜版的表面。顾名思义，主要对掩膜版起物理与化学保护作用

![[Pasted image 20250221175506.png#pic_75center|]]
![[Pasted image 20250221175651.png#pic_75center|]]
![[Pasted image 20250221175716.png#pic_75center|]]

- Immersion presented many challenges, but many elements ported for dry ArF
  浸没式曝光带来了许多挑战，但许多元素已移植到干式ArF光刻中
- EUV is a significantly more challenging endeavour, requiring more innovative comprehensive solutions
  极紫外光刻（EUV）是一项更具挑战性的工作，需要更多创新和综合性的解决方案
- Shorter EUV wavelength has better resolution than conventional DUV
  较短的EUV波长具有比传统DUV更好的分辨率
- Features down to 35nm can be printed
  小于$35\mathrm{nm}$的特征能够印制出来
- 挑战：
	- source power
	- optics lifetime
	- resist sensitivity
	- mask defectivity

- uses a laser-generated plasma source to produce wavelengths of 13 nm. The source operates in a vacuum environment to produce the EUV radiation, which is collected by condenser optics and formed into a beam, The beam is reflected off a reflective reticle and onto the wafer
  使用激光产生的等离子体源产生13nm的波长。该源在真空环境中工作以产生EUV辐射，该辐射被聚光光学器件收集并形成光束。光束被反射掩模版反射到晶片上
	- Principle of High Harmonic Generation (HHG)
	  高次谐波产生原理
	- focuses a conventional laser into a gas to produce high harmonics of the fundamental laser frequency
	  将传统激光聚焦到气体中，以产生基波激光频率的高次谐波

- Light source with $\lambda=13.5\mathrm{nm}$, $13.5\mathrm{nm}$ light is absorbed by all materials
  $\lambda=13.5\mathrm{nm}$的光源，$13.5\mathrm{nm}$光被所有材料吸收
- Purely reflecting optics system including mask
  包括掩模在内的纯反射光学系统
- Each mirror consists of multilayers of $\text{Mo}$ and $\text{Si}$ and can both be used for reduction (usually $4\times$) and as mask
  每个镜子由许多层$\text{Mo}$和$\text{Si}$组成，既可以用于缩小（通常为$4\times$），也可以用作掩模
	- Mirrors are used in place of lenses due to high absorption at short wavelengths
	  由于透镜在短波长下吸收率高，因此使用镜子代替透镜

# E-beam and SCALPEL Lithography

![[Pasted image 20250221182636.png#pic_50center|]]

- System
	- Electron gun (or e-source)
	- Focusing lens
	- Beam blanking plates
	  是一种用于电子束光刻系统中的装置。它们的主要功能是在电子束曝光时快速切断（或“空白”）电子束，以防止不必要的曝光。这些板通过在电子束路径上切换开关来实现快速切换，从而确保只有在需要的时候才有电子束通过
	- Beam deflectors (scan coils that direct beam horizontally and vertically)
	  偏转线圈

- The electron beam has a wavelength so small that diffraction is insignificant
  电子束的波长非常小，以至于衍射可以忽略不计
- The tool is just like an SEM with on-off capability controlled by a “beam blanker”
  该设备就像一台扫描电子显微镜（SEM），具有通过beam blanker控制的开关功能
- Accurate positioning (alignment): “see” the substrate first, then expose
  精确定位（对准）：先“看”基板，然后曝光
- Beam spot diameter of 2 nm can be achieved, at a typical acceleration voltage of $>20\mathrm{k} e \mathrm{V}$
  在典型的加速电压$>20\mathrm{k}e\mathrm{V}$下，可以实现$2\mathrm{nm}$的束斑直径
- However, typical resolution ∼15 nm (>> beam diameter), limited by proximity effect and lateral diffusion of secondary electrons
  然而，典型的分辨率约为$15\mathrm{nm}$（$>>$电子束直径），受到邻近效应和二次电子横向扩散的限制
- 电子的德布罗意波长：$$\lambda=\frac{h}{\sqrt{2meV}}$$其中：
	- $m$为电子质量
	- $e$为元电荷
	- $h$为普朗克常数

## Nanofabrication by E-Beam Lithography

### Advantages

- Precise control of energy and dose
  对能量和剂量的控制很精准
- Critical Dimension $\sim 10\mathrm{nm}$
- Beam focusing achieved using large electrostatic and magnetic field lenses
  使用大静电和磁场透镜聚焦
- Ability to register accurately over small areas
  能够在小区域实现高精准度的套印
- Low defect densities
  缺陷密度低

### Disadvantages

- Requires ultra-high vacuum system to drive electrons effectively
  高真空度
- Very sensitive to electronic and mechanical noise
  对电和机械噪声敏感
- Proximity effect: resolution degrades due to backscattering of electrons within the resist surface
  由于光刻胶表面内电子的反向散射，分辨率会降低

## SCALPEL

![[Pasted image 20250221184529.png#pic_50center|]]

- **SC**attering with **A**ngular **L**imitation **P**rojection **E**lectron beam **L**ithography
  具有角度限制投影的散射电子束光刻
	- Combine all the benefits of step-and-repeat imaging, size reduction, and the narrow beam resolution of e-beam lithography
	  结合步进重复成像、尺寸缩小和电子束光刻的窄束分辨率的所有优点
		- Mask: SiN membrane ($100 \mathrm{nm}$) patterned with $25 \mathrm{nm}$ of W/Cr
		   $100 \mathrm{nm}$ 的氮化硅膜，线宽$25\mathrm{nm}$的钨
		- Thickness coupled with the atomic mass of W/Cr provides sufficient scattering contrast
		  厚度与钨的原子质量匹配，提供了足够的散射对比度
		- Step-and-scan with $4\times$ reduction
		  步进扫描，4倍缩小
		- Decrease exposure time
		  减小曝光时间
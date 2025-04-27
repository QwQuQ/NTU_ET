---
aliases: 
tags: []
---
*表征分析与测量技术*
# Optical Characterization

- 光学表征方法是非损伤的，不会损伤样品的表面
- 但可能效果不如其他表征方法

## Optical Microscopy

- Light cannot be focused to an infinitesimally small spot due to the wave nature of light
  光由于其波动性，无法聚焦到无限小的点。
- There is no lower limit to the size of an isolated object that can be detected
  对于可检测的孤立物体的尺寸，没有下限
![[Pasted image 20250427175404.png#pic_25center|]]
- The minimum separation, $s$, of two point objects occurs when the first maximum of the diffraction pattern of one object falls on the first minimum of the second object 
  两个点状物体的最小分辨距离 ss 出现在一个物体的衍射图案的第一主极大值落在另一个物体的第一极小值上的情况：$$s=\frac{0.61\lambda}{n \mathrm{sin}\theta}=\frac{0.61\lambda}{NA}$$
	- $\lambda$: free space wavelength
	- $n$: refractive index of immersion medium
	- $\theta$: half the angle subtended by the lens at the object,
	- $NA$: numerical aperture
- Best resolution about $0.25 \mathrm{\mu m}$ for $\lambda \approx 0.4\mathrm{\mu m}$, $NA \approx 1$
![[Pasted image 20250427175543.png#pic_75center|]]
- Different approaches to optical microscopy bring out different features
  不同的光学显微镜方法能够突出不同的特征

## Ellipsometry

- Nondestructive technique
- Film thickness measurement; can measure film thicknesses down to $1\mathrm{nm}$
  薄膜厚度测量；可测量厚度低至$1\mathrm{nm}$的薄膜
- Refractive index determination; can measure refractive index of thin films of unknown thickness
  折射率测定；可测量未知厚度薄膜的折射率
- Azimuth angles can be measured with great accuracy
  方位角可以被极其精确地测量
- Measures a ratio of two values
	- Highly accurate and reproducible (even in low light levels)
	  在低光照条件下仍具有高精度和可重复性
	- No reference sample necessary
	  无需参考样品
	- Not as susceptible to scatter, lamp or purge fluctuations
	  对散射、光源或气体冲洗波动的影响较小
- Surface uniformity assessment
  表面一致性评估
- Composition determinations
  成分测定
- Can be used for in situ analysis
  可用于在位分析

![[Pasted image 20250427175645.png#pic_75center|]]
- Angles $P$, $C$, and $A$ lead to ellipsometer quantities $\rho$, $\Psi$ and $\Delta$
- The ellipsometry equation:$$\rho=\mathrm{tan}\Psi e^{j\Delta}$$
- Polarizer将入射光处理成线极化光
- 反射光遵循椭圆方程进行反射，从而能够测量出顶层（蓝色）的反射系数（材料特性）和厚度

## Transmission

![[Pasted image 20250427180306.png#pic_75center|]]
![[Pasted image 20250427180341.png#pic_75center|]]

- Definition
	- Absorption: the loss of a photon from an incident flux by the process of exciting an electron from a lower- to a higher-energy state
	  吸收：通过将电子从较低能态激发到较高能态，从而入射光通量损失光子的过程
- General Scheme
	- Light is incident on a thin sample part of the light is reflected and the remainder is absorbed or transmitted; a measurement is made of the transmitted intensity
	  光照射到一个薄样品上，部分光被反射，其余部分被吸收或透射；然后对透射强度进行测量。
	- The experiment can be carried out as a function of temperature, externally applied fields, sample thickness, etc.
	  该实验可以作为温度、外部施加的场、样品厚度等因素的函数进行研究。

- 吸收系数：$\alpha$
- $\Delta=I_i-I_t=\alpha\cdot d$

## Photoluminescence

- 产生新的光（基本原则）
- 这种方法灵敏度不高
- 因为光的转化率很低，因为不是所有的光都能激发，大部分的光能被转化为热能；所以我们需要照射非常强的光。
- Luminescence is the emission of light due to:
	- Incandescence: energy supplied by heat
	- **Photoluminescence: energy supplied by light**
	- Fluorescence: energy supplied by ultraviolet light
	- **Chemiluminescence: energy supplied by chemical reactions**
	- Bioluminescence: energy supplied by chemical reactions in living beings
	- Electroluminescence: energy supplied by electric current/voltage
	- Cathodoluminescence: energy supplied by electron beams.
	- Radioluminescence: energy supplied by nuclear radiation
	- Phosphorescence: delayed luminescence or "afterglow"
	- Triboluminescence: energy supplied by mechanical action
	- Thermoluminescence: energy supplied by heat

![[Pasted image 20250427180913.png#pic_75center|]]

- Incident laser creates electron-hole pairs (ehp)
  入射激光创造电子-空穴对
- When the ehp recombine, they emit light
  当电子-空穴对复合时，会发光

###  How Does Photoluminescence Work and How Can It Be Used?

- Carrier generation depth
	- Wavelength: depth information
	  波长：深度信息
- Recombination
	- Shockley-Read-Hall (impurities): impurity information
	  杂质
	- Auger (high carrier densities): doping density information
	  掺杂浓度（只能获得高掺杂的信息，低掺杂很难测出来）
	- Surface (surface states, impurities): surface information
	  表面
	- Radiative (light emission): detection mechanism

# Charge-Based Characterization

- Scanning Tunnelling Microscopy
- Atomic Force Microscopy

## Charge-Based Measurements

![[Pasted image 20250427182852.png#pic_25center|]]
- Traditional (I-V Curve)
  传统派需要创建金属电极，对样品存在破坏
	- Current – voltage
	- Capacitance – voltage
	- Current, voltage, capacitance – time
	- Usually need test structure with contacts
- New
  新的方法通过测量电荷，电容什么的非接触测量，不会破坏样品，需要与样品保持一定的距离
	- Deposit charge
	- Measure surface voltage, surface photovoltage
	- Use charge, light
	- Usually contactless

![[Pasted image 20250427183623.png#pic_75center|]]

- Charge is deposited on the wafer chemically or by corona charge
  通过化学方式或电晕电荷将电荷沉积在晶圆上
  > Corona Charge: ionization of a fluid流体的电荷
- Contactless surface voltage/surface photovoltage is measured
  非接触表面电压/表面光电压测量
- Measurement can be enhanced with light
  可以通过光照增强测量效果

## Probe Microscopy

- Probe microscopy was invented in 1980 By Binnig and Rohrer at IBM Labs. in Zürich, Switzerland
- They devised a clever way of bringing a sharp metal tip very close (within 1-2 nm) to a conducting sample, applied a voltage and measured the current
- This technique is known a scanning tunneling microscopy
- For this work they were awarded the Nobel prize in1986

## Scanning Tunneling Microscopy (STM)

![[Pasted image 20250427183146.png#pic_75center|]]
- 针尖和样品表面的电流通过隧道效应产生，非常微弱，所以需要一个放大器。
- 这是目前最精确的非接触测量方法，能够测量原子，速度很慢，要专门的地下室放
- 缺点：针尖的控制，
- For imaging surfaces at the atomic level The resulting tunneling current is a function of tip position, applied voltage, and the local density of states (LDOS) of the sample.
  用于以原子级别成像表面时，所产生的隧道电流是针尖位置、施加电压以及样品的局部态密度（LDOS）的函数
- It requires extremely clean and stable surfaces, sharp tips, excellent vibration control, and sophisticated electronics.
  该过程需要极其清洁且稳定的表面、尖锐的针尖、卓越的振动控制以及先进的电子设备

## Atomic Force Microscopy (AFM)

![[Pasted image 20250427183723.png#pic_75center|]]
- A sharp tip is scanned over a surface with feedback
  一个尖锐的探针在表面上扫描，并通过反馈进行调节QQ
- Piezo-electric scanners maintain the tip at
	- Constant force
		- Height information
	- Constant height
		- Force information
- Tips are typically made from $\mathrm{Si_3N_4}$ or $\mathrm{Si}$
  探针通常由 $\mathrm{Si_3N_4}$ 或 $\mathrm{Si}$ 制成
- The detector measures the difference in light intensities between the upper and lower photodetectors
  检测器测量上下光电探测器之间的光强度差异
- Feedback from the photodiode difference signal enables the tip to maintain either a constant force or constant height
  通过光电二极管的差分信号反馈，使探针保持恒定力或恒定高度

- Contact mode
	- Tip scans the sample in close contact with the surface
	  探针与样品表面紧密接触进行扫描
	- The repulsive force on the tip is around $\mathrm{10^{-8}N}$
	  探针上的排斥力约为 $\mathrm{10^{-8}N}$
	- This force is set by pushing the sample against the cantilever with a piezoelectric element
	  该力通过压电元件推动样品与悬臂梁接触来设定
	- The piezo voltage is proportional to sample height
	  压电电压与样品高度成比例
- Non-contact mode
	- Tip is 5-15 nm above the sample surface. Attractive Van der Waals forces acting between the tip and the sample are detected, and topographic images are constructed by scanning the tip above the surface
	  探针距离样品表面 5-15 nm. 检测探针与样品之间的范德华力，并通过扫描探针上方的表面构建拓扑图像
- Tapping mode
	- Cantilever oscillates at its resonant frequency (50-500 kHz)
	  悬臂梁以其共振频率（50-500 kHz）振荡
	- The cantilever oscillates with a high amplitude (around 20nm) when the tip is not in contact with the surface
	  当探针未接触表面时，悬臂梁以高振幅（约 20nm）振荡
	- The oscillating tip is then moved toward the surface until it begins to lightly touch, or tap the surface
	  振荡的探针向表面移动，直到开始轻微接触或轻敲表面
	- Oscillation amplitude is reduced
	  振荡振幅减少
	- The reduction in oscillation amplitude is used to measure surface features
	  振幅的降低用于测量表面特征

![[Pasted image 20250427184208.png#pic_75center|]]
- 圆球形的尖端能够测量垂直的倾斜
- Measured line width is probe shape dependent
  测量的线宽依赖于探针形状
	- Tip shape obtained from profiling standard samples
	  通过标准样品的轮廓测定探针形状
	- True profile is obtained from known probe tip shape
	  通过已知的探针形状获得真实轮廓
- Probe shape, flexing stability
  探针形状、弯曲稳定性
- Piezoelectric scan linearity
  压电扫描的线性度
- Low throughput

# Electron Beam Characterization

## Electron Yield

> **电子产额（Electron Yield）** 是指材料在受到入射电子或高能光子的激发后，所释放出的电子数量与入射电子数量的比值。它是表征材料电子发射能力的重要参数，在各种电子显微和光谱分析技术中具有重要应用。
> 
> - **二次电子产额（Secondary Electron Yield, SEY）**— 入射电子撞击样品后，会激发二次电子，这些电子的能量较低，通常用于材料表面分析。
    
- **背散射电子产额（Backscattered Electron Yield, BEY）**— 部分入射电子被样品散射并反弹回检测器，它们的能量较高，通常用于成分分析。
    
- **光电子产额（Photoelectron Yield）**— 材料吸收高能光子（如 X 射线或紫外光）后，释放出的光电子产额，常用于光电子能谱分析（XPS）。
![[Pasted image 20250427184832.png#pic_50center|]]

- Primary electrons (PE) incident on a solid give:
	- Absorbed electrons (AE)
	- Secondary electrons (SE)
	- Backscattered electrons (BSE)
- Secondary electron yield maximum at $E\approx 1-3\mathrm{eV}$
- SEs used in scanning electron microscopy (SEM) and voltage contrast

## Electrons in a Solid

![[Pasted image 20250427185014.png#pic_50center|]]

- 入射电子（PE）的能量越大，电子进入样品的深度也就越深。不同的入射电子能量会产生不同的东西。甚至能够产生X射线。
- Electrons accelerated to $1-30\mathrm{keV}$
  - 电子被加速到 $1-30\mathrm{keV}$
- Beam can be focused to a few Angstrom diameter
  光束可以聚焦到几埃的直径
- In the solid the beam “blooms” out to electron range $R_e$
  在固体中，光束会扩展至电子的运动范围 $R_e$
- Since secondary's come from liberated core electrons, their energies are low and thus, only near surface electrons escape.
  由于SE来自被释放的核心电子，其能量较低，因此只有靠近表面的电子能够逸出

## Scanning Electron Microscopy (SEM)

![[Pasted image 20250427185113.png#pic_50center|]]
- 内部是真空的，所以电子能够运动更长的距离。上层产生并聚焦电子，下层用来放样品，边上有电源和真空泵。
- SEM是基于电子的反射工作的
- The electrons interact with atoms in the sample, producing various signals that contain information about the sample's surface topography and composition
  电子与样品中的原子相互作用，产生包含样品表面形貌和成分信息的各种信号
- Routinely used for semiconductors
	- Line width
	- Topology
- Cathodoluminescence
  阴极射线
	- Light emission
- Electron microprobe
  电子探针
	- X-ray emission

## Transmission Electron Microscopy (TEM)

![[Pasted image 20250427185624.png#pic_75center|]]
- Gate是晶体结构，所以能够看到单个原子的晶体结构
- 但是栅氧看不到具体的晶体结构

- TEM的加速能量比SEM高，因为电子要穿过样品。同时样品的测量结果也更好
- Electrons accelerated to $\approx 100-300 \mathrm{keV}$
- Sample must be very thin so electron do not spread out
  样品必须非常薄，必须准备高质量的样品（最重要的部分）

### Sample Preparation: Focused Ion Beam

![[Pasted image 20250427185927.png#pic_50center|]]

- 可以认为是一种蚀刻过程
- 从样品的两边逐渐蚀刻样品，最终创建一个几个原子厚的薄片
- Focused ion beam (FIB)
	- Ga beam
	  生成离子束
	- Focused to 5-10 nm
	  聚焦到5-10nm
	- Cut holes in a sample
	  在样品表面切洞
	- Prepare TEM samples
	  准备TEM样品
	- Connect metal lines
	  用金属线连接

## Electron Microprobe (EMP)

![[Pasted image 20250427190623.png#pic_50center|]]
- Incident electron knocks electron out of K shell
  入射电子将 K 层的电子击出
  > **K层（K Shell）**是原子内部最靠近原子核的电子层，也被称为**1s电子层**。它由最多两个电子组成，并且由于离原子核最近，电子在该层中受到最强的库仑吸引力。
- L shell electron falls into vacancy (hole)
  L 层电子填补空缺（空穴）
- Energy is emitted as an X-ray
  能量以 X 射线的形式释放

![[Pasted image 20250427190133.png#pic_center|能够找到样品中不同的元素]]

- Advantages: Nondestructive technique; trace impurities and major components in a single analysis. Two-dimensional information by scanned beam.
  优点：非破坏性技术；可在单次分析中检测微量杂质和主要成分。通过扫描光束获取二维信息。
- Limitations: Poor sensitivity for elements with Z < 10.
  只能用于比较重的元素，不能检测序数小于10的元素
- X-ray resolution determined by the electron absorption volume not the e-beam size.
  X 射线的分辨率由电子的吸收体积决定，而不是电子束的尺寸。
- Sensitivity: $10^{18}-10^{19}\mathrm{cm^{-3}}$
- Volume sampled:$\approx 10\mathrm{\mu m} \times 10 \mathrm{\mu m} \times 10\mathrm{\mu m}=10^{-9}\mathrm{cm^3}$
- Applications: Rapid analysis of thin films and bulk samples. Two- dimensional elemental display.
  应用：快速分析薄膜和块体样品。二维元素显示。

- The X-rays can be detected by
  SEM中也会有，因为SEM过程中也会产生X射线
	- Energy-dispersive spectrometer (EDS)
	- Wavelength-dispersive spectrometer (WDS)

# Ion Beam Characterization

![[Pasted image 20250427191233.png#pic_75center|]]

- Emission
	- Photon Spectroscopy
	- Particle Induced X-Ray Emission
	- Electron Emission
- Reflection
	- Sputtering
	- Secondary Ion Mass Spectrometry
	- Rutherford Backscattering
- Absorption
	- Ion Implantation
- 由于离子的质量比电子大很多，所以这种方法会损伤样品，但也能够获得更加精准的测量。电子只能测高掺杂和高原子序数的样品

## Secondary Ion Mass Spectrometry

![[Pasted image 20250427191403.png#pic_75center|]]

- Secondary ion mass spectrometry (SIMS) is the most common doping profile method
  次级离子质谱（SIMS）是最常见的掺杂分布分析方法
- Principle: Atoms sputtered from the sample; mass of the ejected ions analyzed
  原理：从样品溅射出原子，并分析喷射出的离子质量
	- Ion mass: element identification; ion intensity: element density
	  离子质量：用于元素识别；离子强度：元素密度
- Advantages: Gives depth profiles. Can analyze all elements; most sensitive of all analytical techniques. Can measure several impurities simultaneously
  优势：提供深度分布信息。可分析所有元素；是所有分析技术中最灵敏的。能够同时测量多种杂质
- Limitations: Destructive method. Subject to matrix effect: ion yields influenced by a change in surface composition. Need standards for concentration determination, independent depth measurement
  限制：破坏性方法。受基质效应影响——离子产额受表面成分变化影响。需要标准样品以确定浓度，并需独立深度测量
- Sensitivity: Depends on impurity. Highest sensitivity is boron in $\mathrm{Si}$ at $\approx 10^{14}\mathrm{cm^{-3}}$; all other elements less sensitive. Sensitivity limited by interference from ions of similar mass/charge
  灵敏度：取决于杂质。对硅中的硼灵敏度最高，约为 $\approx 10^{14}\mathrm{cm{-3}}$；其他元素的灵敏度较低。灵敏度受相似质量/电荷离子的干扰限制

## Rutherford Backscattering

![[Pasted image 20250427191534.png#pic_75center|]]

- 这种玩意有点过时了，太复杂了，能量太高了，现在不咋用
- He ions with several $\mathrm{MeV}$ energy are scattered by the sample atoms
- The mass of the sample atom is determined from the energy of the scattered ions
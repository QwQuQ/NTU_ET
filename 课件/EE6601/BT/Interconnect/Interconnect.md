
# 术语

![[Pasted image 20250222232721.png#pic_75center|]]

- **Local Interconnects**: Wire up transistors within a circuit functional block. They are the shortest but most numerous
  在电路功能块内连接晶体管。它们是最短但数量最多的。
- **Intermediate Interconnects**: Wire up devices across functional circuit blocks
  在功能电路块之间连接设备
- **Global Interconnects**: Are the widest and thickest lines in a chip. They provide power and timing signals to the entire chip
  它们是芯片中最宽和最厚的线路。它们为整个芯片提供电力和时序信号
- **Via**: Refers to the short vertical conductors that connect different levels of wiring to each other
  这是指连接不同层级布线的短垂直导体

# Introduction

![[Pasted image 20250222231647.png#pic_75center|]]

- **Interconnects** connect the electronic circuits on a chip for proper functionality
- Interconnects can be **Local** (Connections within transistors) or Global (**Connections** between transistors including power, ground)

![[Pasted image 20250222234139.png#pic_75center|]]

- Silicides: Short local interconnections which have to be exposed to high temperatures and oxidizing ambients, e.g., polycide and salicide structures
  硅化物：必须暴露在高温和氧化环境中的短局部互连，例如多晶硅化物和自对齐硅化物结构。
- Refractory Metals: Via plugs, future gate electrodes, local interconnections which need very high [[Electromigration]] resistance
  难熔金属：通孔、预留的栅极电极、需要非常高抗电迁移的局部互连
- $\mathrm{TiN}$, $\mathrm{TiW}$: Barriers, glue layers, anti reflection coatings and short local interconnections
  $\mathrm{TiN}$ 和 $\mathrm{TiW}$：用于隔离、粘接层、抗反射涂层以及短局部互连。
- $\mathrm{Al}$, $\mathrm{Cu}$: 大部分互联

# Interconnect Delay

![[Pasted image 20250222232930.png#pic_75center|]]
- 一个公式：$$\tau_L=0.89RC=0.89K_IK_{OX}\epsilon_0\rho L^2\left(\frac{1}{Hx_{OX}}+\frac{1}{WL_S}\right)$$其中：
	- $K_{OX}$是氧化层的介电系数
	- $K_I$考虑了边缘的变化
	- $\rho$是互联线的电阻率

# Interconnect Scaling Scenarios

![[Pasted image 20250222233757.png#pic_33center|]]

- Scale Metal Pitch with Constant Height
  缩放金属间距时保持恒定高度
	- $R$, $C_S$ and $J$ increase by scaling factor
	  电阻，互联线之间的互容和电流密度都随缩放系数提升
	- Higher aspect ratio for gapfill / metal etch
	  宽高比更大
	- Need for lower resistivity metal, Low-$k$
	  需要低电阻率金属，低介电系数材料（参考第1点）
![[Pasted image 20250222233943.png#pic_33center|]]
- Scale Metal Pitch and Height
	- $R$ and $J$ increase by $\mathbf{scaling\ factor^2}$
	- Sidewall capacitance unchanged
	- Aspect ratio for gapfill/metal etch unchanged
	- Need for very low resistivity metal with significantly improved EM performance

# Al Interconnection

- 优点：
	- Low resistivity
	- Ease of deposition
	- Dry etching
	- Does not contaminate $\mathrm{Si}$
	- Ohmic contacts to $\mathrm{Si}$ (but problem with shallow junctions)
	  > Shallow Junction: 6604中出现过，结的长度比扩散长度小
	- Excellent adhesion to dielectrics
- 缺点：
	- [[Electromigration]]: Low life time
	- Hillocks: Shorts between levels
	- Higher resistivity: to $\mathrm{Cu}$

![[Pasted image 20250222234626.png#pic_75center|]]

## Electromigration

[[Electromigration|电迁移]]

## The problems of Al interconnection
![[Pasted image 20250223001720.png#pic_50center|]]
- One practical issue is that $\mathrm{Si}$ is soluble in $\mathrm{Al}$ ($\approx 0.5\% \text{ at 450}\degree C$). This can lead to "spiking" problems

- $1^{\text{st}}$ solution: add $1-2\% \mathrm{Si}$ in $\mathrm{Al}$ to satisfy solubility. Widely used, but $\mathrm{Si}$ can precipitate when cooling down and increase $\rho_C$
  在铝中加入1-2%硅，这被广泛使用。但是硅会参与冷却并且加大接触电阻$\rho_C$
![[Pasted image 20250223001802.png#pic_50center|]]
- Better solution: Use barrier layer(s). $\mathrm{Ti}$ or $\mathrm{TiSi_2}$ for good contact and adhesion, $\mathrm{TiN}$ for barrier
  使用隔离层。$\mathrm{Ti}$ 或 $\mathrm{TiSi_2}$ 用于良好的接触和粘附，$\mathrm{TiN}$ 用于隔离

# Cu interconnect

- $\mathrm{Cu}$ is slowly replacing $\mathrm{Al}$ because:
	- $\mathrm{Cu}$ has lower resistivity: Lower RC delay
	- $\mathrm{Cu}$ has lower [[Electromigration]]: Higher life time
	- $\mathrm{Cu}$ has fewer hillocks: Less shorts between levels
	- Higher electromigration resistance, reduced resistivity and dielectric constant results in reduction in number of metal layers as more wires can by placed in lower levels of metal layers.
	  更高的抗电迁移性、降低的电阻率和介电常数导致金属层数量减少，因为更多的导线可以放置在较低层级的金属层中

![[Pasted image 20250223002537.png#pic_33center|Typical Damascene Process]]

- 问题：
	- $\mathrm{Cu}$ **cannot be dry etched**: CMP
	- $\mathrm{Cu}$ contaminates $\mathrm{Si}$: Needs barriers
		- Copper **diffuses quickly** in $\mathrm{Si}$ and $\mathrm{SiO_2}$
			- increased junction and leakage
			- decreased carrier lifetime and junction break down voltage
		- Solutions:
			- Pattern using **Damascene** (inlaid) scheme
			  使用**大马士革**（镶嵌）方案进行图案化。
			- Encapsulate copper wires/vias with diffusion **barriers**

## Materials for Barriers / Liners

- **Transition Metals**: ($\mathrm{Pd}$, $\mathrm{Cr}$, $\mathrm{Ti}$, $\mathrm{Co}$, $\mathrm{Ni}$, $\mathrm{Pt}$) generally poor barriers, due to high reactivities to $\mathrm{Cu}$ $<450\degree C$, Exception: $\mathrm{Ta}$, $\mathrm{Mo}$, $\mathrm{W}$ etc. More thermally stable, but fail due to $\mathrm{Cu}$ diffusion through grain boundaries (polycrystalline films)
  过渡金属（$\mathrm{Pd}$、$\mathrm{Cr}$、$\mathrm{Ti}$、$\mathrm{Co}$、$\mathrm{Ni}$、$\mathrm{Pt}$）通常是较差的隔离
- ，因为它们在低于 $450\degree \mathrm{C}$ 时与铜（$\mathrm{Cu}$）的反应性较高。例外情况：$\mathrm{Ta}$、$\mathrm{Mo}$、$\mathrm{W}$ 等，这些金属具有更高的热稳定性，但由于铜通过晶界（多晶薄膜）扩散，它们最终也会失效
- **Transition Metal Alloys**: e.g., $\mathrm{TiW}$. Can be deposited as amorphous films (stable up to $500\degree C$)
  过渡金属合金：例如 $\mathrm{TiW}$。可以作为非晶薄膜沉积（稳定至 $500\degree \mathrm{C}$）
- **Transition Metal - Compounds**: Extensively used, e.g., $\mathrm{TiN}$, $\mathrm{TaN}$, $\mathrm{WN}$
  过渡金属化合物：广泛使用，例如 $\mathrm{TiN}$、$\mathrm{TaN}$、$\mathrm{WN}$
- **Amorphous Ternary Alloys**: Very stable due to high crystallization temperatures (i.e., $\mathrm{Ta_{36} S_{14}}$, $\mathrm{N_{50}}$, $\mathrm{Ti_{34}Si_{23}N_{43}}$)
  非晶态三元合金：由于具有较高的结晶温度，因此非常稳定（例如，$\mathrm{Ta_{36}S_{14}}$、$\mathrm{N_{50}}$、$\mathrm{Ti_{34}Si_{23}N_{43}}$）
- **Currently PVD**: Sputtering/evaporation is used primarily to deposit the barrier/liner, however, step coverage is a problem. **ALD** is being developed for barrier/liner application.
  主要使用溅射/蒸发法沉积屏障层/衬垫层，然而，阶梯覆盖是一个问题。**原子层沉积（ALD）** 正在开发用于隔离层/衬垫层应用

> ## Step Coverage
> 在沉积过程中，薄膜材料不仅需要覆盖水平表面，还需要覆盖垂直和倾斜的表面。阶梯覆盖是指薄膜材料在这些不同表面上的厚度一致性和覆盖效果。良好的阶梯覆盖意味着薄膜在所有表面上的厚度相对均匀，没有显著的薄弱点或缺陷
> 例如，在使用物理气相沉积（PVD）方法时，薄膜材料可能难以完全覆盖台阶和凹槽的侧壁和底部，导致阶梯覆盖不均匀。这可能会影响器件的性能和可靠性。相比之下，原子层沉积（ALD）方法可以通过分子级别的控制实现更均匀的阶梯覆盖，提供更好的薄膜质量

## Deposition Methods of Cu

### Physical Vapor Deposition (PVD)

![[Pasted image 20250223004613.png#pic_33center|]]
- **Physical Vapor Deposition (PVD)**
	- Conventional metal deposition technique: Widely used for $\mathrm{Al}$ interconnects
	  传统的金属沉积技术：广泛用于铝（$\mathrm{Al}$）互连。
	- Produce $\mathrm{Cu}$ films with **strong (111)**
	  生产具有**强（111）** 晶向的铜（$\mathrm{Cu}$）薄膜。
	- Poor step coverage: not tolerable for filling high-aspect ratio features: result **Pinching**
	  >在物理气相沉积（PVD）过程中，**pinching**（夹点）现象是指当沉积薄膜在填充高宽比特征（如深沟槽或高纵横比孔洞）时，由于覆盖不均匀而导致的薄膜断裂或狭窄现象。这个现象发生在薄膜在特征表面上沉积时，特别是在侧壁和底部的覆盖效果不佳，使得薄膜在这些区域形成空隙或狭窄部分

![[Pasted image 20250223004649.png#pic_75center|]]

### Chemical Vapor Deposition (CVD)

- **Chemical Vapor Deposition (CVD)**
	- Conformal deposition with ecellent step coverage in high-aspect ratio holes and vias: costly in processing and maintenance
	  在高宽比孔洞和通孔中具有优良阶梯覆盖的共形沉积：加工和维护成本较高
	  > **共形沉积（Conformal Deposition）** 是一种薄膜沉积技术，用于在复杂形状和高宽比特征（如深沟槽、孔洞和通孔）表面上形成均匀的薄膜。共形沉积的关键在于其在所有表面上的覆盖效果相同，无论是水平面、垂直面还是倾斜面
	- Generally produce $\mathrm{Cu}$ films with fine grain size, **weak (111)** texture and rough surface
	  通常会生产具有细晶粒尺寸、**弱（111）** 结构和粗糙表面的铜（$\mathrm{Cu}$）薄膜。

### Electroplating

![[Pasted image 20250223004705.png#pic_50center|]]
![[Pasted image 20250223005338.png#pic_75center|]]
- **Electroplating**
	- **Dissociation**: $\mathrm{CuSO_4}\rightarrow \mathrm{Cu}^{2+}+\mathrm{SO_4}^{2-} \text{ (solution)}$
	- **Oxidation**: $\mathrm{Cu}\rightarrow \mathrm{Cu}^{2+} + 2e^- \text{ (anode)}$
	- **Reduction**: $\mathrm{Cu}^{2+}+2e^-\rightarrow \mathrm{Cu}\text{ (cathode, i.e., wafer)}$
	- **Plating Bath**: Standard sulfuric acid copper sulfate bath ($\mathrm{H_2SO_4}$, $\mathrm{CuSO_4}$ solution)
	- Additives to improve the film quality

#### Why
![[Pasted image 20250223010912.png#pic_50center|]]
- Good step coverage and filling capability comparable to CVD process ($\mathrm{0.25\mu m}$)
- Compatible with Low-$k$ dielectrics
- Generally produce strong (111) texture of $\mathrm{Cu}$ film
- Produce much larger sized grain structure than any other deposition methods through self-annealing process

### Additives for Copper ECD

- **DEFINITION**: Mixture of organic molecules and chloride ion which are adsorbed at the copper surface during plating to
  在电镀过程中，混合的有机分子和氯离子吸附在铜表面上，以
	- enhance thickness distribution and feature fill
	  以增强厚度分布和特征填充
	- control copper grain structure and thus ductility, hardness, stress, and surface smoothness
	  控制铜的晶粒结构，从而影响其延展性、硬度、应力和表面光滑度
- Components: Most commercial mixtures use 3 or more organic components and chloride ion which adsorb at the cathode during plating:
  大多数商用混合物在电镀过程中使用 3 种或更多有机成分和氯离子，这些成分吸附在阴极上
	- Brighteners (Accelerators)
		- Adsorbs on copper metal during plating, participates in charge transfer reaction. Determines copper growth characteristics with major impact on metallurgy
		  吸附在电镀过程中的铜金属上，参与电荷转移反应。决定铜的生长特性，对冶金产生重大影响
	- Levelers
		- Reduce growth rate of copper at protrusions and edges to yield a smooth final deposit surface.
		  减少铜在突出部位和边缘的生长速率，以获得光滑的最终沉积表面。
		- Effectively increases polarization resistance at high growth areas by inhibiting growth to a degree。 proportional to mass transfer to localized sites
		  通过抑制高生长区域的生长速率，有效地增加极化电阻。其抑制程度与质量转移到局部位置的量成正比。
	- Carriers
		- Carriers adsorbed during copper plating to form a relatively thick monolayer film at the cathode (wafer). Moderately polarizes copper deposition by forming a barrier to diffusion of $\mathrm{Cu}^{2+}$ ions to the surface.
		  在铜电镀过程中，载体吸附在阴极（晶圆）上，形成相对较厚的单层膜。通过形成阻挡 $\mathrm{Cu}^{2+}$ 离子扩散到表面的屏障，适度极化铜沉积。
	- Chloride
		- Adsorbs at both cathode and anode.
		  在阴极和阳极上均有吸附。
		- Accumulates in anode film and increases anode dissolution kinetics.
		  积聚在阳极膜中，并增加阳极溶解动力学（速度？不懂）。
		- Modifies adsorption properties of carrier to influence thickness distribution.
		  改变载体的吸附性能以影响厚度分布。
	- Suppressors

### Effect of the seed layer on the properties of the final Cu

![[Pasted image 20250223013325.png#pic_75center|]]
- Electroplating needs a seed layer of $\mathrm{Cu}$ as it does not occur at a dielectric surface.
  电镀需要一层铜（$\mathrm{Cu}$）种子层，因为它不会在介电表面上进行。
- Properties of the final $\mathrm{Cu}$ layer critically depend upon the characteristics of the seed layer.
  最终铜（$\mathrm{Cu}$）层的特性在很大程度上取决于种子层的特性。
- The deposition of the seed layer can be done by PVD, CVD or ALD
  种子层的沉积可以通过物理气相沉积（PVD）、化学气相沉积（CVD）或原子层沉积（ALD）来完成。
- Currently PVD is preferred, CVD and ALD being investigated
  目前，物理气相沉积（PVD）是首选方法，而化学气相沉积（CVD）和原子层沉积（ALD）则正在研究中。

## Annealing

![[Pasted image 20250223013754.png#pic_75center|]]

## The effects of Cu Resistivity

**哎什么怪东西，压根不讲啊**

### Effect of Surface and Grain Boundary Scattering

#TODO 

### Effect of Line Width Scaling Due to Scattering

- Resistivity increases as grain size decreases due to increase in density of grain boundaries which act as carrier scattering sites
  随着晶粒尺寸的减小，电阻率增加，这是由于晶界密度的增加，这些晶界起到载流子散射点的作用（电阻的一大来源是晶格散射）
- Resistivity increases as main conductor size decreases due to increased surface scattering
  随着主导体尺寸的减小，由于表面散射的增加，电阻率增加

### Effect of Cu diffusion Barrier

![[Pasted image 20250223014956.png#pic_50center|]]
- Effect of Cu diffusion Barrier
	- Barriers have higher resistivity
	- Barriers can’t be scaled below a minimum thickness
	- Consumes larger area as dimensions decrease
- Resistivity of the composite wire is increased
- Resistivity of metal wires could be much higher than bulk value

导线缩了但是外面的皮没缩，所以相对的电阻率大了

### Effect of Chip Temperature

- Higher temperature ⇒ Lower mobility ⇒ Higher resistivity
- Realistic Values at 35nm node: P=0.5, temp=100 o C - local ~ 5 μΩ-cm - semi-global ~ 4.2 μΩ-cm - global ~ 3.2 μΩ-cm

# Future of Interconnect Technology

## Optical Interconnect

![[Pasted image 20250223015819.png]]

- In integrated circuits, optical interconnects refers to any system of transmitting signals from one part of an integrated circuit to another using light. Optical interconnects have been the topic of study due to the high latency and power consumption incurred by conventional metal interconnects in transmitting electrical signals over long distances, such as in interconnects classed as global interconnects.
  在集成电路中，光互连是指使用光从集成电路的一个部分传输信号到另一个部分的任何系统。由于传统金属互连在长距离传输电信号时会产生高延迟和高功耗，因此光互连成为研究的主题，特别是在被分类为全局互连的互连中。
  >在集成电路中，信号的传输是非常重要的。传统的金属互连，例如铜或铝线，用于在集成电路内部传输电信号。然而，当信号需要在较长距离上传输时，例如在大规模集成电路中，从一个芯片的一端传输到另一端，金属互连会导致信号延迟增加和功耗上升。这些问题会影响电路的性能和效率。
- In order to control the optical signals inside the small IC package properly, microelectromechanical system (MEMS) technology can be used to integrate the optical components (i.e. optical waveguides, optical fibers, lens, mirrors, optical actuators, optical sensors etc.) and the electronic parts together effectively.
  为了在小型集成电路封装内正确控制光信号，可以使用微机电系统（MEMS）技术将光学组件（如光波导、光纤、透镜、反射镜、光致动器、光传感器等）和电子元件有效地集成在一起。
  >微机电系统（MEMS）技术是一种将机械和电子部件集成在微小尺度上的技术。在控制集成电路（IC）封装内的光信号时，使用MEMS技术可以有效地将各种光学组件（如传输光信号的光波导、光纤、聚焦和调节光信号的透镜和反射镜，以及检测和调控光信号的光致动器和光传感器）与电子元件结合起来。这种集成不仅可以提高信号传输的精度和效率，还可以使整个系统更加紧凑和可靠。

## RF Interconnect

- RF or wireless interconnect technologies only recently are being considered as viable candidate for either on chip or off-chip interconnects replacing global wires
  射频（RF）或无线互连技术最近才被认为是替代全局导线的片上或片外互连的可行候选者。
- As optical interconnect, free-space transmission and guided-wave transmission
  作为光互连、自由空间传输和波导传输
- Free-space transmission is focused upon demonstration of a 24GHz wireless clock distribution system in CMOS technology
  自由空间传输侧重于演示采用CMOS技术的24GHz无线时钟分配系统
	- With both an on-chip clock transmitter and alternatively, with anoff-chip external clock transmitter
	  既有片上时钟发射器，也有片外外部时钟发射器
	- The 24GHz clock frequency will be divided down to obtain therequired clock data rate
	  24GHz时钟频率将被分频，以获得所需的时钟数据速率

（完全没懂有什么关系）

## 3D Interconnect

![[Pasted image 20250223020105.png#pic_50center|]]
- 3D interconnect is to reduce the number and the average lengths of the longest global wires
  3D互连旨在减少最长全局线的数量和平均长度
- 3D integration of active transistor layers or, placement of the clock/signal and power/ground wires on opposite sides of a chip has been shown to reduce the number and average length of 2D global wires by providing shorter vertical paths for connection
  有源晶体管层的3D集成，或者将时钟/信号和电源/地线放置在芯片的相对侧，已被证明可以通过提供更短的垂直连接路径来减少2D全局线的数量和平均长度
- A 3D approach has also been shown to reduce overall chip area when designs are interconnect-limited
  当设计受到互连限制时，3D方法也被证明可以减少整体芯片面积
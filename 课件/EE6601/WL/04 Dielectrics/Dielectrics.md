---
aliases: 
tags: []
---
# Most Important Passivating Material: SiO2

- Passivate (protect) high field regions on semiconductor surface
- Masking for selective ion implantation
- Very good etching selectivity
- As an insulating layer in the gate region of a MOS transistor
- Stable and reproducible Si/SiO2 interface, final circuit protection, etc
- Easily to form by thermal oxidation

# Metal-Oxide Semiconductor Structure

- Heart of MOSFETs
- Heart of DRAM, Flash memories
- MOS structure for metal line running over a dielectric- coated semiconductor
- Degenerated-doped polysilicon is used as the metal in MOS structure for CMOS devices

# MOSFET

![[Pasted image 20250428201048.png#pic_50center|]]
- In the MOSFET, the current is controlled by an electric field applied perpendicular to both the semiconductor surface and to the direction of current.
- The phenomenon is called the **field effect**.
- The basic transistor principle is that the voltage between two terminals, provides the electric field, and controls the current through the third terminal.
  晶体管的基本原理是，两个端子之间的电压提供电场，并控制通过第三个端子的电流。

# Scaling Issues

- MOSFET的source drain都是高掺杂的

## Limits

- Thermodynamics : doping concentration in source and drain
  热力学：源极和漏极的掺杂浓度。当我们施加电流时，器件会发热，所以杂质会更加活泼，导致杂质粒子可能会穿透绝缘层。当器件缩小是，绝缘能力就会下降。
- Physics : tunneling through thin gate oxide
  物理学：通过薄栅氧化层的隧道效应。器件变小后隧道效应变强。有些地方会产生弱点，导致器件击穿
- Statistics: statistical fluctuation of body doping
  统计学：掺杂浓度的统计波动。由于掺杂不均匀，所以掺杂可能会重新分布，从而导致器件性能下降。（掺杂可以当成墨水，半导体可以当成水）
- Economics : factory cost
  经济学：工厂成本

## Problems in Scaling of Gate Oxide

![[Pasted image 20250428202122.png#pic_50center|]]
- 电子会找最薄的地方穿透，所以最薄的地方会成为弱点。

- Below 20A problems with SiO2
  低于 20A 时 SiO₂ 的问题（2nm是一个合适的栅氧厚度）
- Gate leakage: circuit instability, power dissipation
  栅极漏电：电路不稳定、功耗增加
- Performance degradation due to $t_{ox}\text{(electrical)}>t_{ox}\text{physical}$
  由于 $t_{ox}\text{(electrical)}>t_{ox}\text{(physical)}$ 导致性能下降
	- Carrier quantization in the channel and depletion in poly-Si gate
	  载流子在通道中的量子化以及多晶硅栅极的耗尽
	- Degradation and breakdown
	  退化和击穿
	- Dopant penetration through gate oxide
	  掺杂剂穿透栅氧化层
	- Defects
	  缺陷

# Technology SiO2

- Thermal oxidation
- Chemical Vapor deposition (CVD)

## Important Properties SiO2

- Excellent dielectric:
  优良的介电材料
	- Resistivity $\rho_e>10^{16}\mathrm{\Omega\cdot cm}$. Bandgap $\mathrm{EG}\approx 9eV$
	- High breakdown field $E_c\approx 1V/\mathrm{nm}$
	- Interface passivation. $D_{\mathrm{it}}>10^9/eV\mathrm{cm^2}$
	- Stable & reproducible bulk properties
	- Stable & reproducible Si/$\mathrm{SiO_2}$ interface
	- Perfect adhesion & low pinhole density < $1/\mathrm{cm^2}$
- Good masking properties
  良好的遮盖特性
	- Low diffusivity for dopants
	  掺杂低扩散
	- Easily etched selective to Silicon
	  比硅的蚀刻选择性高

## Grown Oxide vs. CVD Oxide

![[Pasted image 20250429022058.png#pic_75center|]]
- Grown Film:
	- Oxygen is from gas phase
	- Silicon from substrate
	- Oxide grow into silicon
	- Higher quality
- Deposited Film:
	- Both oxygen and silicon are from gas phase
	- Deposit on substrate surface
	- Lower temperature
	- Higher growth rate

# Thermal Oxidation

## Kinetics of Oxide growth(Deal-Grove Model)

![[Pasted image 20250429011912.png#pic_50center|]]
- Oxidation of silicon occurs when either the oxidizer, $\mathrm{O_2}$ or $\mathrm{H_2O}$ , reacts with Si to form $\mathrm{SiO_2}$ . The possible way for the oxidation process is for the oxidizing species $\mathrm{O_2}$ or $\mathrm{H_2O}$ to diffuse through the growing oxide layer and then can react with $Si$ surface.
  硅的氧化发生在氧化剂（O₂或H₂O）与硅（Si）反应生成二氧化硅（SiO₂）时。氧化过程的可能机制是氧化物种（O₂或H₂O）通过正在生长的氧化层扩散，随后与硅表面发生反应
- Wet：水
- Dry：氧气

## Thermal Oxidation Basics

![[Pasted image 20250429012200.png#pic_50center|]]
- Silicon is consumed
- A 2.2 times volume expansion
- The oxidiser ($\mathrm{O_2}$ or $\mathrm{H_2O}$) diffuse
- Compressive grown-in stress
	- ~300MPa @ $T_G<950\degree C$
	- 300-700MPa @ $T_G<950\degree C$
- Oxidation& point defects:
- consumes vacancies
- generates interstitials
- Net reactions
	- Dry: $\mathrm{Si}+\mathrm{O}\rightarrow \mathrm{SiO_2}$
	- Wet: $\mathrm{Si}+2\mathrm{H_2O}\rightarrow \mathrm{SiO_2}+2\mathrm{H_2}$

## Thickness of Si consumed (planar oxidation)

![[Pasted image 20250429012502.png#pic_75center|]]
$$\displaylines{X_{\mathrm{Si}}=X_{\mathrm{ox}}\cdot \frac{N_{\mathrm{ox}}}{N_{\mathrm{Si}}} \\ =X_{\mathrm{ox}}\cdot\frac{2.3\times10^{22}\mathrm{\ molecules/cm^3}}{5\times 10^{22} \mathrm{\ atoms/cm^3}}=0.46X_{\mathrm{ox}}}$$

### Oxide Growth Rate

![[Pasted image 20250429012810.png#pic_75center|]]

$$t_{\mathrm{ox}}^2+At_{\mathrm{ox}}=B(t+\tau)$$

## Oxide Growth

- Initial Growth Phase:
  初始生长阶段
	- Kinetics of oxide formation(Deal-Grove Model) is very well applicable for wet oxidation.
	  氧化形成的动力学（Deal-Grove模型）非常适用于湿氧化
	- For dry oxidation, there is an extremely rapid oxidation occurring during the first 300Å of growth.Reasons: presence of pores, formation of space charge region (between oxygen ion and the hole).
	  对于干氧化，在最初300Å的生长过程中发生极快的氧化。原因包括：孔隙的存在，空间电荷区的形成（氧离子与空穴之间）
- Orientation Dependence of Oxidation Rate:
	- Growth rate depends on surface density of Si atoms.
	  氧化生长速率取决于硅原子的表面密度。
	- Surface density of atoms in Si(111)>Si(110>Si(100)
	  硅(111)的表面原子密度 > 硅(110) > 硅(100)。
	- Growth rate of oxide on Si(111)>Si(110)>Si(100).
	  硅(111)上的氧化生长速率 > 硅(110) > 硅(100)。
	- Growth rate depends on linear rate constant. Parabolic growth rate (associate with diffusivity) is independent of crystal orientation.
	  氧化生长速率取决于线性速率常数。抛物线生长速率（扩散性相关的）与晶体取向无关

## Thermal Oxidation Applications

![[Pasted image 20250429013136.png#pic_75center|]]

## Oxidation Furnaces

![[Pasted image 20250429013158.png#pic_75center|]]
- Dummy Wafers: 减弱turbulence（湍流）

## Silicon/Oxide Interface

![[Pasted image 20250429015734.png#pic_75center|]]
- 栅氧是多晶结构，硅衬底是单晶的，所以能够看到他们的分界面。

## Experimental SiO2 Growth

![[Pasted image 20250429015930.png#pic_75center|]]
- 想要长得快，用Wet
- 想要长得好，用Dry（薄片，小于1$\mathrm{\mu m}$）

## Oxidation Rate with Pre-oxidation Clean

![[Pasted image 20250429020044.png#pic_75center|]]
- 需要洗得很干净

## Thermal Nitridation

![[Pasted image 20250429020149.png#pic_75center|]]
> LOCOS：局部氧化硅隔离
> Kooi Effect：LOCOS中边缘产生白带

# Chemical Vapor Deposition

![[Pasted image 20250429020712.png#pic_75center|]]

- Chemical gases or vapors react on the surface of solid, produce solid byproduct on the surface in the form of thin film. Other byproducts are volatile and leave the surface.

### Deposition Process

![[Pasted image 20250429020856.png#pic_50center|]]

- Gas or vapor phase precursors are introduced into the reactor
  气相或蒸汽态前驱体被引入反应器
- Precursors across the boundary layer and reach the surface
  前驱体穿过边界层并到达表面
- Precursors adsorb on the substrate surface
  前驱体吸附在衬底表面
- Adsorbed precursors migrate on the substrate surface
  吸附的前驱体在衬底表面迁移
- Chemical reaction on the substrate surface
  衬底表面发生化学反应
- Solid byproducts form nuclei on the substrate surface
  固体副产物在衬底表面形成核
- Nuclei grow into islands
  核生长为岛状结构
- Islands merge into the continuous thin film
  岛状结构融合形成连续薄膜
- Other gaseous byproducts desorb from the substrate surface
  其他气态副产物从衬底表面脱附
- Gaseous byproducts diffuse across the boundary layer
  气态副产物穿过边界层扩散
- Gaseous byproducts flow out of the reactor.
  气态副产物流出反应器

- 岛的边界容易成为弱点，导致CVD沉积的质量下降。所以需要增加厚度来补偿缺陷

### Atmospheric Pressure CVD

![[Pasted image 20250429021224.png#pic_75center|]]

- CVD process taking place at atmospheric pressure
  在常压下进行的化学气相沉积 (CVD) 过程
- APCVD process has been used to deposit silicon oxide and silicon nitride
  常压化学气相沉积 (APCVD) 工艺已用于沉积氧化硅和氮化硅
- APCVD $\mathrm{O_3}$-TEOS oxide process is widely used in the semiconductor industry, especially in STI and PMD applications
  APCVD $\mathrm{O_3}$-TEOS 氧化工艺在半导体行业广泛应用，特别是在 STI（浅沟槽隔离）和 PMD（前金属介电层）应用中
- Conveyor belt system with in-situ belt clean
  具有在位清洁功能的传送带系统

### Low Pressure CVD

![[Pasted image 20250429021743.png#pic_75center|]]

- Longer MFP
  更长的平均自由程 (MFP)
- Good step coverage & uniformity
  良好的阶梯覆盖率和均匀性
- Vertical loading of wafer
  晶圆的垂直加载
- Fewer particles and increased productivity
  更少的颗粒，提高生产率
- Less dependence on gas flow
  对气体流动的依赖性降低
- Vertical and horizontal furnace
  垂直和水平炉
- Adaptation of horizontal tube furnace
  适用水平管式炉
	- Low pressure: from 0.25 to 2 Torr
	  低压：0.25 至 2 Torr
	- Used mainly for polysilicon, silicon dioxide and silicon nitride films
	  主要用于多晶硅、二氧化硅和氮化硅薄膜
	- an process 200 wafers per batch
	  每批可处理 200 片晶圆

> MFP（Mean Free Path，平均自由程）指的是气体分子在发生碰撞之前能够移动的平均距离。在半导体制造过程中，较长的 MFP 可以让气体分子充分接触晶圆的各个角落，从而提高CVD的质量。

### Plasma Enhanced CVD

![[Pasted image 20250429021834.png#pic_75center|]]

- Developed when silicon nitride replaced silicon dioxide for passivation layer
  发展于氮化硅取代二氧化硅作为钝化层时
- High deposition rate at relatively low temp.
  在相对较低的温度下具有较高的沉积速率
- RF induces plasma field in deposition gas
  射频 (RF) 在沉积气体中引发等离子场
- Stress control by RF
  通过射频控制力度
- Chamber plasma clean.
  反应腔等离子清洁

# Dielectric Thin Film Characteristics

## Refractive index

## Thickness

## Uniformity

# Reliability of SiO2

## Intrinsic Breakdown

- Damage initiates at anode and cathode interface causing degradation
- Eventually it spreads throughout the body of the dielectric causing breakdown
- Degradation can be minimized if damage at the interfaces is prevented

## Extrinsic Breakdown


![[Pasted image 20250430001028.png#pic_75center|]]
- Damage initiates at an extrinsic defect present in the oxide
- Eventually if spreads throughout the body of the dielectric causing breakdown
- Degradation is minimized by careful processing to reduce process induced defects

## Breakdown Statistics

![[Pasted image 20250430000600.png#pic_50center|]]
- Intrinsic breakdown has higher $Q_{bd}$
- Extrinsic breakdown results in early breakdown
- A good set of devices should not have early breakdown
- 早期故障都是由Extrinsic Breakdown引起的

## Transition (Strained) Layer at the Substrate Interface

![[Pasted image 20250430000909.png#pic_75center|]]
- 更薄的氧化层会导致更多的缺陷，所以我们希望氧化层越厚越好
- Structural inhomogenity (1-2 monolayers) due to transition from $\mathrm{Si}$ to $\mathrm{SiO_2}$
  硅到二氧化硅中间的几层
- Stress due to volume change during $\mathrm{SiO_2}$
- Strained bonds are easier to break resulting in lower $Q_{bd}$ for gate injection of electrons
- For thinner films the transition layer becomes a significant fraction of the total layer

# Nitrided $\mathbf{SiO_2}$

- Incorporating nitrogen or fluorine instead of hydrogen strengthens the Si/SiO2 interface and increases the gate dielectric lifetime because Si-F and Si-N bond are stronger than Si-H bonds

- Nitroxides
	- Nitridation os SiO2 by NH3, N2O, NO
	- Growth in N2O
	- Improvement in reliability
	- Barrier to dopant penetration from poly-Si gate
	- Used extensively
- Fluorination
	- Fluorination of SiO2 by F ion implantation
	- Improvement in reliability
	- Increases B penetration from P+ poly-Si gate
	- Not used intentionally
	- Can occur during processing (WF6, BF2)

# High k Dielectrics

## Dielectric Constant

- The dielectric constant, $k$, is a physical measure of the electric polarizability of a material
  介电常数 $k$ 是材料对电极化能力的物理度量。
- Electric polarizability is the tendency of a material to allow an externally applied electric field to induce electric dipoles (separated positive and negative charges) in the material. Polarization $\mathbf{P}$ is related to the electric field $\mathbf{E}$ and the displacement $\mathbf{D}$ by
  电极化能力是指材料允许外部施加的电场在其中诱导电偶极（分离的正负电荷）的倾向。极化 $\mathbf{P}$ 与电场 $\mathbf{E}$ 和位移 $\mathbf{D}$ 之间的关系为：$$\mathbf{D}=\varepsilon_0\mathbf{E}+\mathbf{P}$$
- $\mathbf{P}$ is related to $\mathbf{E}$ through $\chi_e$ the electric susceptibility of the dielectric 
  $\mathbf{P}$ 与 $\mathbf{E}$ 通过 $\chi_e$（介电的电敏感度）相关联 $$\mathbf{P}=\varepsilon_0\chi_e\mathbf{E}$$ therefore $$\mathbf{D}=\varepsilon_0\left(1+\chi_e\right)\mathbf{E}=\varepsilon_0 k \mathbf{E}$$where $\varepsilon_0$ is the permittivity of the free space
- Note that $\mathbf{P}$ also is the density of atomic electric dipole per unit volume 
  需要注意的是，$\mathbf{P}$ 也表示单位体积内的原子电偶极密度：$$\mathbf{P}=\Sigma\mathbf{p}/V=N\mathbf{p}$$where $\mathbf{p}$ is the dipole moment and $N$ is the density of dipoles
 $$\mathbf{D}=\varepsilon_0\mathbf{E}+\mathbf{P}$$

## Requirements for the MOS gate dielectrics

- High dielectric constant: higher charge induced in the channel
  高介电常数：在通道中诱导更高的电荷
- Wide band gap: higher barriers: lower leakage
  宽禁带：更高的势垒，降低泄漏
- Ability to grow high purity films on Si with a clean interface
  在硅（Si）上生长高纯度薄膜并保持洁净界面
	- High resistivity and breakdown voltage
	  高电阻率和击穿电压
	- Low bulk and interfacial trap densities
	  低体阱和界面阱密度
- Compatibility with the substrate and top electrode
  与衬底和顶电极的兼容性
	- Minimal interdiffusion and reaction
	  最小的互扩散和反应
	- Minimal silicon reoxidation during growth and device processing
	  在生长和器件加工过程中尽量减少硅的再氧化
		- Even a thin $\mathrm{SiO_2}$ layer would deteriorate the $C_{\text{gate}}$ significantly
		  即使是薄薄的一层 $\mathrm{SiO_2}$ 也会显著降低栅电容 $C_{\text{gate}}$
- Thermal stresses: most oxides have larger thermal expansion coefficients than $\mathrm{Si}$
  热应力：大多数氧化物的热膨胀系数大于硅 $\mathrm{Si}$
- Good Si fabrication processing compatibility
  良好的硅制造工艺兼容性
	- Stability at higher processing temperatures and environments
	  在较高的加工温度和环境下保持稳定
	- Ability to be cleaned, etched, etc.
	  具备清洁、蚀刻等工艺能力

# High-k Dielectrics

- Why do we need high-K dielectrics? $$I_D=\mu_{eff} C_{ox}\frac{W}{L}\left(V_G-V_T\right)^2=\frac{W\mu_{eff}k_{ox}\varepsilon_0}{Lt_{ox}}(V_G-V_T)^2$$
- With scaling
	- $W$ and $L$ decreases same amount
	- $\mu_{eff}$ remains about the same or decreases
	- $V_G-V_T$ decreases
- To keep drain current constant
	- $t_{ox}$ decreases: oxide leakage current increases
	- $k_{ox}$ increases: thicker insulator, reduced oxide leakage current

## High-k MOS Gate Dielectrics

$$I_{\text{channel}}\propto \text{charge}\times\text{source injection velocity}$$
$$I_{\text{channel}}\propto\left(\text{gate oxide cap} \times \text{gate overdrive}\right)V_{\text{inj}}$$
$$I_{\text{channel}}\propto C_{ox}\left(V_{GS}-V_T\right)E_{\text{source}}\mu_{\text{inj}}$$
$$I_{\text{channel}}\propto C_{ox}\propto\frac{k}{\text{thickness}}$$
- Historically $C_{ox}$ has been increased by decreasing gate oxide thickness. It can also be increased by using a higher $k$ dielectric

## Formation of High-k Dielectric for Advanced Technologies

- Formation of Silicon Oxynitride($\mathrm{SiON}$) in oxygen and $\mathrm{NH_3}$
- Nitridation of gate oxide in $\mathrm{NH_3}$ under high temperature to convert surface layer to silicon nitride
- Deposition of Silicon Nitride layer on top of underlying silicon oxide layer
- Deposition of truly high-k dielectrics

## Alternatives to SiO2 :Silicon Nitride


## Nitridation of Silicon

![[Pasted image 20250430003855.png#pic_75center|]]
- $\mathrm{Si}$ reacts with $\mathrm{NH_3}$ to grow $\mathrm{Si_3N_4}$
- Excellent gate dielectric properties
- Reaction needs very high temperatures
- $\mathrm{Si}$ reacts with atomic nitrogen
- Reaction temperature could be reduced using nitrogen plasma
- More research needed
- Several deposition methods under investigations, e.g., rapid thermal CVD, jet vapor deposition (JVD)

## Candidates for High K Gate Dielectrics

![[Pasted image 20250430003914.png#pic_75center|]]
- Higher $k$ materials have lower bandgap
- There are many performance, reliability and process integration issues yet to be solved
- More research is needed to make these materials manufacturable
- Wide band gap: higher barriers: lower leakage

## Thermodynamic Stability of High-K Dielectric Oxides

- Unstable oxides (e.g. $\mathrm{TiO_2}$, $\mathrm{TaO}$, $\mathrm{BST}$)
	- React with $\mathrm{Si}$ to form $\mathrm{SiO_2}$ and silicides upon thermal annealing
	- Barrier (e.g. $\mathrm{Si_3N_4}$) is required to prevent such a reaction
		- Dielectric stack: poly-Si/nitridelunstable oxide/nitride/Si substrate
		- A monolayer of nitride on both sides of gate dielectric already contributes 5A to the physical oxide thickness
- Stable oxides(e.g. $\mathrm{HfO_2}$,$\mathrm{ZrO_2}$,$\mathrm{Al_2O_3}$) and their silicates(e.g. $\mathrm{ZrSi_x O_y}$) and aluminates (e.g. $\mathrm{ZrAl_x O_y}$)
	- Do not react with Si upon thermal annealing(up to $\mathrm{1000\degree C}$)
	- May not require a barrier layer between $\mathrm{Si}$ and the metal oxide
		- simple structure: poly-Si/stable oxide/Si substrate

## High-k Gate Dielectric Can Also be Applied to Other Semiconductors

- Passivation of $\mathrm{Ge}$ with $\mathrm{GeO_x N_y}$, $\mathrm{ZrO}$ and $\mathrm{HfO_2}$
- $\mathrm{1^{st}}$ demo of $\mathrm{Ge}$ MOSFETs with hi-$k$
- *p*-MOSFET with $3\times \mathrm{mobility}$ vs. hi-$k$ $\mathrm{Si}$
- Passivation of many other materials being experimented, e.g., carbon nanotubes, GaAs, etc.

## Issues With High k Dielectrics

- Problems
	- Low band gap
	- Low barrier height
	- Low breakdown electric field
	- Poor insulator/Si interface
		- Thin intervening SiO layer
	- Oxide charge
	- Low electron/hole mobility
		- Strained Si
- MOS process compatible?

# High k or Low k?

- Low-k and copper for future interconnection
- High-k dielectric for gate or DRAM capacitor

- Parasitic capacitance is a significant problem in high-frequency circuits and is often the factor limiting the operating frequency and bandwidth of electronic components and circuits.
  寄生电容是高频电路中的一个重要问题，通常是限制电子元件和电路工作频率和带宽的因素。

- A low-k dielectric is an insulating material that exhibits weak polarization when subjected to an externally applied electric field. A few practical approaches to design low-k materials are:
  低介电常数 (low-k) 材料是一种在外加电场作用下表现出弱极化的绝缘材料。设计低介电常数材料的一些实用方法包括：
	- Choose a nonpolar dielectric system. For example, polarity is weak in materials with few polar chemical groups and with symmetry to cancel the dipoles of chemical bonds between dissimilar atoms.
	  选择非极性绝缘系统：例如，在化学结构中极性较弱的材料通常具有较少的极性化学基团，并且通过对称性可以抵消不同原子之间化学键的偶极。
	- Since $k_{\mathrm{air}}=1$, dielectrics can also have lower effective k with the incorporation of some porosity into the chemical structure.
	  由于空气的介电常数 $k_{\mathrm{air}}=1$，可以通过在化学结构中加入一定的孔隙来降低材料的有效介电常数，例如：
		- Materials where atoms are far apart (remember $\mathbf{P}=N\mathbf{p}$)
		  选用原子间距较大的材料
		- Add physical porosity
		  添加物理孔隙
	- Minimize the moisture content in the dielectric or alternatively design a dielectric with minimum hydrophilicity. Since $k_{\mathrm{water}}\approx 80$, a low-k dielectric needs to absorb only very small traces of water before losing its permittivity advantage.
	  减少材料的吸湿性：或者设计一种最小化亲水性的介电材料。由于水的介电常数 $k_{\mathrm{water}}\approx 80$，低介电常数材料必须避免吸收过多的水分，否则会失去其低介电常数的优势。

## Challenges for Low-K Materials

![[Pasted image 20250430005126.png#pic_75center|]]

- Weak Thermo-Mechanical Strength:$10\times$ worse than $\mathrm{SiO_2}$ in almost every category of thermo-mechanical properties.

## Dielectric Constant Reduction Methods

- Reduce polarization strength and density.
- Reduce Si-O density: $\mathrm{SiO_2}$ ($k=4$)
- Incorporate F: $\mathrm{SiOF}$ ($k=3.7$)
- Incorporate CH3-: SiOC(H) ($k=2.8$)
- Use low polarization polymer:![[Pasted image 20250430005250.png#pic_75center|]]

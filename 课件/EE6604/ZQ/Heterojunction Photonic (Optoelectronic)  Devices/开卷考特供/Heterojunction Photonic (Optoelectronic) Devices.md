# Semiconductor Lasers

## Photon-Electron Interaction

There are three processes for interaction between a photon and an electron in a solid

### Absorption

If an atom in state $E_1$ absorbs the photon, it goes to the excited state $E_2$. The change in the energy state is the **absorption process**. The requirement is $hf_{12}=E_2-E_1$.
如果处于状态$E_1$的原子吸收光子，它会进入激发态$E_2$。能级变化的过程称为**吸收**。要求是$hf_{12}=E_2-E_1$。

### Spontaneous Emission

The excited state of the atom is unstable. Without any external stimulus, the atom can make a transition to the ground state, giving off a photon of energy $hf_{12}$. This process is called **spontaneous emission**. Thus, $E_2-E_1=hf_{12}$.
原子的激发态是不稳定的。在没有任何外部刺激的情况下，原子可以跃迁到基态，并发出能量为$hf_{12}$的光子。这个过程称为**自发辐射**。因此，$E_2-E_1=hf_{12}$。

### Stimulates Emission

When a photon of energy $hf_{12}$ impinges on an atom while it is in the excited state, the atom can be stimulated to make a transition to the ground state and gives off a photon of energy $hf_{12}$. This process is called **stimulated emission**.
当能量为 $hf_{12}$ 的光子撞击处于激发态的原子时，原子可以被刺激到跃迁到基态，并发出一个能量为 $hf_{12}$ 的光子。这个过程被称为**受激发射**。
The radiation from stimualted emission if **coherent** because all photons emitted are in phase (the same energy and wave vector).
受激发射产生的辐射是**相干的**，因为所有发射的光子都是同相的（具有相同的能量和波矢）。

### Dominant Interaction Process In Devices

- LEDs: Spontaneous Emission
- Laser Diodes: Stimulated Emission
- Photodetectors and Solar Cells: Absorption

### Semiconductor Materials for Lasers

- All lasing semiconductors must have **direct bandgaps** because of the momentum conservation and high radiative-transition probability.
  所有激光半导体必须具有**直接带隙**，因为需要满足动量守恒和高辐射跃迁几率。
- The laser emission wavelengths range: $0.3$ to $30\mu\mathrm{m}$.
- GaAs was the first material to emit laser radiation and its related III-V compound alloys are extensively studied.
- Three most important III-V compound alloy systems for lasers are:
	- GaInAsP
	- GaInAsSb
	- AlGaAsSb

### Features of Semiconductor Lasers

- Similar to the solid-state ruby laser and helium-neon gas laser, semiconductor lasers are highly monochromatic and can produce a highly directional beam of light.
  与固态红宝石激光器和氦氖气体激光器相似，半导体激光器也是高度单色的，并且可以产生高度定向的光束。
- Differ from other lasers, semiconductor lasers are small (about 0.1 mm long) and can be easily modulated at high frequencies by simply modulating the biasing current.
  不同于其他激光器，半导体激光器体积小（约0.1毫米长），并且可以通过简单调节偏置电流高频调制。
- They are the important light source for optical communication, video recording, optical reading, high speeding printing.
  它们是光通信、视频录制、光学读取和高速打印的重要光源。

## Laser Operation

- Three conditions for laser operation:
	- Population Inversion
	  粒子数分布反转
	- Carrier and Optical Confinemen
	  载流子和光学限制
	- Optical Cavity
	  光学谐振腔

### Population Inversion 粒子数分布反转

![[Pasted image 20241103024933.png]]
- (a) Homojunction laser and double-heterojunction (DH) laser. ^103958
- (b) Energy band diagrams under forward bias for the two lasers.

To enhance stimulated emission for laser operation, population inversion is necessary. This can be done by very heavily doping both sides of the junction.

![[Pasted image 20241102224055.png#pic_center|]]
- When a large bias is applied, high concentrations of electron and holes are injected into the transition region. As a result, the region d contains a large concentration of elections in the conduction band and holes in the valance band.
  当施加大偏置电压时，高浓度的电子和空穴被注入到过渡区。因此，区域$d$包含大量导带电子和价带空穴。
- The condition necessary for population inversion is the difference of the **Quasi-Fermi Level**s of electron and holes $(E_{FC}-E_{FV})>E_g$.

>  ### Quasi-Fermi Levels 准费米能级
> 在电、光或热激发下，半导体并**不热平衡**时，在热平衡条件下的公式不适用。所以此时需要使用准费米能级$E_{FN}$和$E_{FP}$代替费米能级
$$n=n_i\times exp\left(\frac{E_{FN}-E_i}{kT}\right)$$
$$p=n_i\times exp\left(\frac{E_i-E_{FP}}{kT}\right)$$
式中的$n$和$p$代表非热平衡条件下的载流子浓度。
>> ### Thermal Equilibrium 热平衡
>> 在半导体中指材料中的载流子，产生数等于复合数。

### Carrier and Optical Confinements 载流子和光学限制

![[Pasted image 20241103025929.png#pic_center|Carrier Conffinement]]
- Take the double-heterojunction (DH) Laser as an example, the carriers are confined within the active region by the heterojunction energy barriers.
  以双异质结激光器为例，载流子通过异质结势垒被限制在有源区内。
  
  ![[Pasted image 20241103030345.png#pic_center|Optical Confinment]]
- The optical field is also confined within the active region by the abrupt reduction of the refractive index outside the active region.
  光场也通过有源区外折射率的急剧下降被限制在有源区内。
- AlGaAs has smaller refractive index than GaAs.
  AlGaAs的折射率比GaAs小。

![[Pasted image 20241103031217.png]]
- Consider that the three layer structure with layers 1,2,3 are n-AlGaAs, GaAs and p-AlGaAs, respectively. And $n_2>n_1,n_3$. The ray angle $\theta_{12}$ at the layer 1/2 intergace exceeds the critical angle given by Snell's law $$sin(\theta_c)=\frac{n_1}{n_2}$$ A similar situation occurs for $\theta_{23}$ at layer 2/3 interface. In this case, the propagation of optical radiation is confined in the direction parallel to the layer interface in the active region.
  考虑具有三层结构，其中层1、2、3分别是n-AlGaAs, GaAs和p-AlGaAs。而且 $n_2>n_1,n_3$。层1/2界面处的射线角度$\theta_{12}$超过了由**斯涅尔定律**给出的临界角$$sin(\theta_c)=\frac{n_1}{n_2}$$在层2/3界面处也会出现类似的情况。在这种情况下，光辐射的传播被限制在有源区内平行于层界面的方向。
- We can define a confinement factor $\Gamma$, which is the ratio of the light intensity within the active layer to the sum of light intensity both within and outside the active region.$$\Gamma=\frac{I_{\mathrm{active\ region}}}{I_{\mathrm{total}}}\cong1-e^{-Cd\Delta n}$$where:
	- $C$ is a constant
	- $\Delta n$ is the difference in refractive index
	- $d$ is the thickness of the active region

### Optical Cavity 光学谐振腔

#### Optical Gain

The photons released by stimulated emission can cause further stimulations as long as there is **population inversion**. This process is called **optical gain**.
只要存在**粒子数反转**，由受激发射释放的光子就能进一步引发更多的受激发射。这一过程被称为**Optical Gain**。

The gain obtained in a single travel in the active region is small.
在有源区内单次传播获得的增益很小。

To increase the optical gain, multiple passes of a wave must occur. This can be achieved by an optical cavity which is essentially a resonant cavity in which the photons have multiple reflections.
为了增加光学增益，光波必须进行多次传播。这可以通过光学腔体来实现，光学腔体本质上是一个谐振腔，光子在其中进行多次反射。

For semiconductor lasers, the most widely used cavity is the Fabry-Perot cavity.
对于半导体激光器，最广泛使用的腔体是法布里-佩罗谐振腔。

#### Fabry-Perot Cavity

![[Pasted image 20241103032241.png]]
- (a) A typical laser structure showing the Fabry-Perot cavity.
  展示法布里-佩罗谐振腔的典型激光结构。
	- The **Fabry-Perot Cavity** is formed by mirrored surfaces on two sides (**left and right**). The other two sides (**front and back**) are roughened.
	  法布里-佩罗谐振腔由两侧（**左侧和右侧**）的镜面形成，其他两侧（**前侧和后侧**）粗糙。
- (b) The stationary states of the cavity.
  谐振腔的稳定状态。
	- The photons to be emitted towards these mirrored sides are multiple reflected back. Photons at **resonant modes** are allowed to build up through stimulated emission. 
	  光子向这些镜面发射时会被多次反射。光子在**谐振模式**下通过受激辐射积累。
- (c) The variation of refractive index (or dielectric constant) responsible for optical confinement.
  负责光限制的折射率（或介电常数）的变化。

##### Resonant Modes

- Resonant modes are those for which integer multiple half wavelength of the light in the cavity equals the length of the cavity:$$m\left(\frac{\lambda}{2n}\right)=L$$or$$m\lambda=2nL$$where:
	- $m$ is an integer
	- $L$ is the cavity length
	- $n$ is the refractive index of the cavity
	- $\lambda$ is the light wavelength
![[Pasted image 20241103035316.png#pic_center]]
- Many values of $λ$ can satisfy the resonance condition but only those within the spontaneous emission spectrum will be produced.
  许多 $λ$ 的值可以满足谐振条件，但只有波长在自发辐射光谱内的会被产生。
- Due to optical loss, only the strongest can survive.
  由于光损耗，只有最强的可以留存
- The separation $\Delta \lambda$ between the allowed modes in the longitudinal (propagating) direction is the difference in the wavelengths corresponding to $m$ and $m+1$.
	- It can be obtained by differentiating $m\lambda=2nL$ and is expressed as$$\Delta \lambda=\frac{\lambda^2\Delta m}{2nL\left(1-\frac{\lambda}{n}\frac{\mathrm{d}n}{\mathrm{d}\lambda}\right)}$$
	- Although $n$ is a function of $\lambda$ but the change $\frac{\mathrm{d}n}{\mathrm{\lambda}}$ is very small. $\Delta m=1$. Therefore,$$\left|\Delta \lambda\right|\cong\frac{\lambda^2}{2nL}$$

## Double-Heterojunction (DH) Laser

The energy diagram of a DH lasers made of GaAs/AlGaAs
![[Pasted image 20241103040341.png#pic_center|]]
- The stimulated emission is from the GaAs, and the emission frequency $\nu$ is such that $h\nu=E_g(\mathrm{GaAs})$. The corresponding wavelength$$\lambda(\mu \mathrm{m})=1.24/E_g(e\mathrm{V})=0.880\mu \mathrm{m}$$
  受激发射源于GaAs，其发射频率$\nu$满足$h\nu=E_g(\mathrm{GaAs})$。
- To achieve tuning wavelength of laser, an AlGaAs layer should be the active layer instead of GaAs. But the bandgap of the AlGaAs active layer must be less than that of the p-AlGaAs and n-AlGaAs barrier layers.
  为了实现激光波长可调，有源层应该使用AlGaAs而不是GaAs。但AlGaAs有源层的带隙必须小于p-AlGaAs和n-AlGaAs势垒层的带隙。

### Threshold Current & Threshold Current Density

- The threshold current is the minimum current required for lasing to occur.
- The current upto threshold is given by the usual forward biased **p-n junction current equation**.
  小于阈值电流的电流表达式由普通的正向偏置 p-n 结电流方程给出。$$I=I_o\left(e^{\frac{V_A-IR_S}{V_T}}-1\right)$$Where:
	- $V_A$ is the applied voltage
	- $I_o$ is the saturation current at the operating temperature $T(K)$
	- $R_S$为串联等效电阻
- Once laser action starts above the threshold, then the junction voltage drop is $\frac{E_g}{q}$ , where $E_g$ is the active layer bandgap. The current now will be
  一旦激光作用超过阈值，结电压降为 $\frac{E_g}{q}$，其中 $E_g$ 是有源层的带隙。此时的电流将会是$$I=\frac{V_A-E_g/q}{R_S}$$ ^9ec28f
- The threshold current density can be expressed as$$J_{\mathrm{threshold}}=\frac{1}{\beta}\left[\alpha+\frac{1}{2L}\mathrm{ln}\left(\frac{1}{R_1R_2}\right)\right]$$where:
	- $\beta$ is the **gain factor**
	- $\alpha$ is the loss per unit length from absorption and other scattering mechanism
	- $L$ is the cavity length
	- $R$ is the reflectance of the cavity$$R=\left(\frac{n-1}{n+1}\right)^2$$
  $J_{\mathrm{threshold}}$ may be different in different book

### Threshold Current Varies With Temperature

![[Pasted image 20241103044849.png]]

- (a) Light Output versus Diode Current for a GaAs/AlGaAs DH laser.
	- the output power becomes lower at high temperature
	- $I_{\mathrm{threshold}}$ increases with temperature
- (b) Temperature Dependence of the Continuous-Wave Current Threshold.
	- $I_{\mathrm{threshold}}$ follows an exponential relation with temperature,$$I_{\mathrm{threshold}}=I_o e^{\frac{T}{T_o}}$$where:
		- $I_o$ is a **constant**, dependent on device type and size
		- $T_o$ is called **characteristic temperature**, 110 Celsius for this laser

### Example

A double heterojunction laser diode is connected in a closed circuit with a series resistor and a variable power supply. The device shows no emission at a bias of 2V and an injected current of 0.9A but strong emission at a bias of 5.7V and a current of 2A. Assume that the device operates at room temperature and has a saturation current of 0.1A.

#### Solution

由于在室温（300K），所以热电压为$V_T=26m\mathrm{V}$

饱和电流$I_S=0.1\mathrm{A}$

在2V正向电压时没有发射，在此时套用普通的pn结电流公式：$$I=I_S\left(e^\frac{V_F-IR_S}{V_T}-1\right)$$
（呃啊我草泥马不要什么地方都把pn结公式里的减1省掉啊草泥马）

代入饱和电流和热电压可以解得$$R_S=2.16\Omega$$

代入超过阈值的电流公式求带隙：$$I=\frac{V_A-E_g/q}{R_S}\implies E_g=1.38e\mathrm{V}$$（这里的单位选择电子伏特会比较好算）

算波长$$\lambda=\frac{ch}{E_g}=898.4\mathrm{nm}$$
上式中：
- $c$为光速
- $h$为普朗克常数

## Quantum Well Lasers

### Single Quantum-Well lasers

- The structure of a quantum-well (QW) laser is similar to that of a **DH Laser** except the thickness of the active layer in a QW laser is very small, less than $20 \mathrm{nm}$.
![[Pasted image 20241103050241.png#pic_center|]]
- The band diagram of a **single QW Laser** where the central GaAs region $L_y=20 \mathrm{nm}$, sandwiched by two AlGaAs layers.
- **Carriers and photons are confined in the single QW**

### Multiple Quantum-Well (MQW) Lasers

![[Pasted image 20241103050930.png#pic_center|cross section schematic of Separate-Confinement-Heterostructure (SCH) InGaAs/InGaAsP MQW laser]]

The 4 InGaAs QWs with InGaAsP barrier layers are sandwiched by the two InP cladding layers to form a waveguide with a step index change.

![[Pasted image 20241103051806.png#pic_center|Schematic of the bandgap of the SCH MQW layers.]]

- The InGaAs wells are $8\mathrm{nm}$ thick with a $E_g$ of $0.75e\mathrm{V}$ The GaInAsP barriers are 30 nm thick with a $E_g$ of $0.95e\mathrm{V}$.
- The alloy compositions make them **Lattice Matched** to InP.

> ### Lattice Match 晶格匹配
> The two materials have the same **Lattice Constant**s, e.g. AlAs on GaAs.
> 两种材料有相同的晶格常数。
>> ### Lattice Constant 晶格常数
>> ![[Lattice Constant.png#pic_center|]]
>> 晶格常数一般由6个参数组成：$a$、$b$、$c$、$\alpha$、$\beta$、$\gamma$
>> 由于在半导体中一般为立方结构，所以可以只用一个参数表示晶胞的物理尺寸。

#### Graded-Index SCH MQW Lasers

- One can also introduce graded-index (GRIN) to the SCH laser by increasing the $E_g$ of the cladding layers through many small stepwise increases rather than one step change. It will be called GRIN-SCH-MQW laser.

![[Pasted image 20241103053442.png#pic_center|energy bandgaps of a GRIN-SCH MQW laser]]
- It is also possible to change the energy bandgap of the GRIN cladding layer gradually rather than by steps.
![[Pasted image 20241103054013.png|Schematic of a Triple-Quantum-Well (TQW) Laser with GRIN-SCH]]

![[Pasted image 20241103054233.png#pic_center|Light output power vs current curves measured at different temperatures for the GRIN-SCH TQW laser]]

### Advantages Compared to DH Lasers

- Smaller $I_{\mathrm{th}}$ (17mA vs 80mA at room temperature, $I_{\mathrm{th}}$ os as small as possible)
- Higher $T_O$ (260℃ vs 110℃, higher the better)
	- This is because the GRIN-SCH structure can confine **both carriers and the optical field** more effectively.

### Example

For high temperature laser operation, it is important to have a low-temperature coefficient of the threshold current, defined as$$\xi=\frac{\mathrm{d}I_{th}}{\mathrm{d}T}\frac{1}{I_{th}}$$
1. What is the coefficient for the laser with $T_O=110\mathrm{^\circ C}$?
2. If $T_O=50\mathrm{^\circ C}$, is this laser better or worse for high temperature operation?
#### Solution

1. 考虑阈值电流与温度的表达式（在DH Laser那里写了。您也没说这公式在SQW Laser也成立啊）：$$\displaylines{I_{th}=I_Oe^{\frac{T}{T_O}}\implies\xi=\frac{\mathrm{d}}{\mathrm{d}T}\left(I_Oe^{\frac{T}{T_O}}\right)\frac{1}{I_Oe^{\frac{T}{T_O}}}\\=\frac{I_O}{T_O}e^{\frac{T}{T_O}}\cdot \frac{1}{I_O e^{\frac{T}{T_O}}}=\frac{1}{T_O}=0.0091{^\circ C}^{-1}}$$
2. $$\xi=1/50=0.02{^\circ C}^{-1}>0.0091{^\circ C}^{-1}\implies \mathrm{worse}$$

## Surface Emitting Lasers

- The edging emitting lasers (DH Laser and MQW Lasers) can have high quality. However, as the light is emitted from the edge, there are difficulties to integrate them with other devices in the real application circuits.
  边缘发射激光器（包括上述的DH激光器和QW激光器）可能有高质量。然而，由于光从边缘发射，在实际电路应用中将它们与其他设备集成时存在困难。
- Surface emitting lasers emit photons from surface.
- The structures of the surface emitting lasers also **include a QW or a few QWs as an active region**. In addition, there are n-type and p-type **distributed Bragg Reflectors (DBRs)** to better confine the generated photons.
  表面发射激光器的结构也包括作为有源区的一个量子阱或几个量子阱。此外，还有n型和p型分布式布拉格反射器 (DBRs) 以更好地限制生成的光子。
- They are called vertical cavity surface emitting lasers (VCSELs) as they have a vertical cavity.
  它们被称为垂直腔面发射激光器 (VCSELs)，因为它们的谐振腔是垂直的。

### Structure of Surface Emitting Lasers

![[Pasted image 20241103061227.png|Schematic of a Surface Emitting Laser with an active region of GaAs/InGaAs QWs]]

![[Pasted image 20241103062106.png|Light Output Power vs Injection Current for adevice of 15μm×15μm]]
- Main advantage of VCSELs:
	- Small threshold current
	- Small power consumption
	- Easy for integrating with other devices.


# Quantum-Well Infrared Photodetectors

- The quantum well lasers (你在搞什么？这里是Laser吗？是Photodetectors吧) rely on transitions of carriers between the conduction band and valence band, (called interband transitions). The energy of the photons generated is approximately equal to the bandgap energy.
  
- Device applications can also rely on **intersubband transitions**.
  
## Subbands in Quantum-Wells

![[Pasted image 20241103062828.png]]
- (a) Band structure of a single quantum well.
- (b) Construction:
	- **Discrete electron subbands** in the conduction band well and **discrete hole subbands** in the valence well.
	  导带阱中的**离散电子子带**和价带阱中的**离散空穴子带**。
	- $n=1$ is **ground subband** (or level), $n=2$ and above are excited subbands.
	  $n=1$是**基态子带**（或能级），$n=2$及以上是激发子带。

### Energy of Subbands

- For the QW with infinite barriers height, the quantized energy levels or subbands are given by
  对于具有无限势垒高度的量子阱，量子能级或子带由以下公式给出：$$E_n=\frac{\hbar^2}{2m^*}\left(\frac{n\pi}{W}\right)^2$$Where:
	- $m^*$ is the Effective Mass of the carriers in the wells
	- $n=1,2,3$ is quantum number
	- $W$ is well width
	- $\hbar=\frac{h}{2\pi}=6.582\times10^{-16}eV\cdot s$ is reduced Plank constant
- For the QWs with finite barrier hight, the energy levels can be obtainable using numerical or graphic methods.
  对于具有有限势垒高度的量子阱，可以使用数值或图形方法来获得能级。
![[Pasted image 20241103064857.png]]
- The electron in the ground level (one subband) can jump to a higher energy level, say $n=2$, (another subband) by absorbing a photon. Or electron can drop to a low energy level by releasing a photon.
  处于基态（一个子带）的电子可以通过吸收光子跃迁到更高的能级，例如$n=2$（另一个子带）。或者通过释放光子跃迁到较低的能级。

> ### Effective Mass 有效质量
> 晶体中电子的作用不止受到外加场的作用，还受到内部周期势场的作用，所以使用有效质量求电子的加速度。有效质量与惯性质量不同，有效质量可以有正负（想想在水中上浮的物体，有效质量为负）。$$\mathbf{a}=\frac{-e\mathbf{E}}{m_n^*}$$
>
> 由于粒子的运动是三维的，所以可以将有效质量分解。$$m^*=\left(g^2m_xm_ym_z\right)^{1/3}$$
> 式中的$g$为简并度，硅材料中$g=6$

## Quantum-Well Structures for Long Wavelength Fnfrared Detection

- In general, the efficiency of interband transition is much higher than that of intersubband transition.
  普遍地，带间跃迁的效率远高于带内跃迁。
- Why ones still rely on intersubband transition for long wavelength detection?
  为什么人们依然依赖带内跃迁进行长波探测？
	- There are not many reliable narrow bandgap materials available.
	  并没有什么小带隙的材料可用。
- For the long wavelength infrared of $10\mu m$, the corresponding energy is $0.124e\mathrm{V}$. The typical semiconductor with such small bandgap is HgCdTe (Mercury Cadmium Telluride or MCT). But it is a big challenge to fabricate repeatable high-quality materials with controllable parameters.
  对于10微米的长波红外，其对应的能量是0.124电子伏特（eV）。具有如此小带隙的典型半导体是HgCdTe（碲镉汞，或称MCT）。但要制造出具有可控参数的高质量、可复现的材料是一个巨大的挑战。

### N-Type Quantum-Well Infrared Photodetectors (QWIPs)

![[Pasted image 20241103065638.png]]
- **All wells are doped by donors**, and **all barriers are undoped**.

#### Test of n-type QWIPs

![[Pasted image 20241103193416.png#pic_center|]]
- Cross-hatched two layers are $n^+$ for ohmic contact
  交叉阴影的两层是$n^+$，用于欧姆接触
- QWs between them are for detecting light
  它们之间的量子阱用于检测光线
- Light incidence is from a $45^\circ$ polished substrate surface
  光从45°抛光的衬底表面射入
- Note that n-type QWIPs can not detect normal incident photons because of the polarization selection rules of intersubband transitions.
  注意：由于带内跃迁偏振选择规则的限制，n型QWIP不能检测垂直入射的光子
- If ones use n-type QWIPs to detect normal incident photons, gratings on top should be fabricated so that the normal incidence could have an angle when reaches the QWs.
  如果要用n型QWIP检测垂直入射的光子，其上需要制造一个光栅使入射光在抵达量子阱时存在一定角度

#### Dark Current and Photocurrent

![[Pasted image 20241103195309.png#pic_center|]]
- Dark Current is the current measured by applying a bias when no light illuminates the QWIPs
- The dark current $I_d$, is mainly due to tunneling $I_t$ and thermionic emission $I_{\mathrm{thermonic}}$, $I_d=I_t+I_{\mathrm{thermonic}}$
- Dark Current is a background current, the smaller the better.

- Photocurrent is due to the electrons jumped from ground level to the excited level after absorbing incident photons. $$I_p=n_pq\mu \xi$$where:
	- $n_p$ is the photogenerated electron concentration
	- $\mu$ is Carrier Mobility
	- $\xi$ is electrical field

> ### Carrier Mobility 载流子迁移率
> 描述金属或半导体内部载流子在电场作用下移动快慢程度的物理量。符号是$\mu$
> 从漂移电流密度的表达式中可以得到
> $$\mu=\frac{q\tau}{m^*}=\frac{v_D}{E}$$
>>
>> ### Drift Current Density 漂移电流密度
>> 电子漂移电流密度：$$J_{n,drift}=qn\mu_n E$$
>> 空穴漂移电流密度：$$J_{p,drift}=qp\mu_pE$$
>> 式中的$\mu_n$和$\mu_p$为Carrier Mobility，要注意的是$J_{n,drift}$和$J_{p,drift}$都是正的（很好理解，相同电场下空穴和电子的电流方向是一样的）。
>>
>> 推导：
>> 在没有外加电场的时候，载流子的静速度是0（随机运动）
>> 平均自由程Mean free path: $l$，两次碰撞之间的平均距离
>> 平均自由时间Mean free time: $\tau$，两次碰撞之间的平均时间
>> 
>> 施加电场$E$，载流子有效质量为$m^*$: 
>> 加速度：$a=-\frac{qE}{m^*}$
>> 漂移速度：$v_D=-\frac{qE\tau}{m^*}$
>> 
>> 电流密度：$J_{drift}=-qnv_d=\frac{qnq\tau E}{m^*}$
>> 定义$\mu=\frac{q\tau}{m^*}=\frac{v_D}{E}$为载流子迁移率，有$$J_{drift}=qn\mu E$$


![[Pasted image 20241103195934.png]]
- (a) Photon absorption in the conduction band quantum wells.
  导带量子阱中的光子吸收
- (b) How current flows after applying an external electrical field.
  电流在外部电场下的流动

When the QWIP is under illumination, the total current is the sum of dark and photocurrent but dominated by photocurrent,$$I_{\text{total}}=I_p+I_d\approx I_p$$

#### Detected Wavelength

- For a given material system, the peak absorption wavelength detected by the detector $\lambda_p$ varies with:
	- well width
	- barrier height
	- doping density in the wells

##### Wien's Displacement Law

![[Pasted image 20241103202329.png#pic_center|Absorption and Photocurrent as a function of photon energy.]]
$$\lambda_{\mathrm{max}}T=2.898\times10^{-3}\mathrm{m\cdot K}$$
For human body: $\lambda_{\mathrm{max}}\approx9.4\mu\mathrm{m}$

#### Example: Effect of well width

![[Pasted image 20241103202442.png#pic_center|]]
Consider three InGaAlAs/InAlAs QWIPs $M1$, $M2$ and $M3$, having well width of $W1=8.6nm$, $W2 =12nm$ and $W3=13.5nm$, respectively, while their barriers are fixed at 40nm.
考虑三个InGaAlAs/InAlAs量子阱红外探测器 (QWIP) $M1$、$M2$和$M3$，其阱宽分别为$W1=8.6\text{nm}$、$W2=12\text{nm}$ 和 $W3=13.5\text{nm}$，而它们的势垒层均固定为 $40\text{nm}$。

![[Pasted image 20241103203048.png#pic_center|]]
Intersubband absorption spectra (or Ip) from the three $In_{0.53}Ga_{0.3}Al_{0.17}As/In_{0.52}Al_{0.48}As$ MQW structures with well widths of 8.6, 12, and 13.5nm, respectively. Their barrier layers are all fixed at 40nm. They are measured using FTIR at room temperature.
来自三个$In_{0.53}Ga_{0.3}Al_{0.17}As/In_{0.52}Al_{0.48}As$多量子阱 (MQW) 结构的带间吸收光谱（或称Ip），其阱宽分别为8.6、12和13.5nm。它们的势垒层均固定为 40nm。这些样品是在室温下使用傅里叶变换红外光谱（FTIR）进行测量的。

| No. | Well Width $W\text{(nm)}$ | $\lambda_p\text(nm)$ | $D{(10^{-6}\text{nm}^{-1})}$ |
| :-: | :---------------------: | :----------------: | :-----------------------: |
| M1  |            8.6            |         9.7          |             0.13             |
| M2  |           12.0            |         14.5         |            0.097             |
| M3  |           13.5            |         17.4         |            0.094             |

![[Pasted image 20241103204717.png#pic_center|]]
$\lambda_p$ increases with Well Width $W$.

Theoretically, according to infinitely deep QW (Energy of Subbands): $$E_2-E_1=\frac{3\hbar^2\pi^2}{2mW^2}=\frac{hc}{\lambda}$$ $$\lambda=\frac{hc}{E_2-E_1}=DW^2$$
### P-Type QWIPs

- P-type QWIPs can directly detect normal incident light as the restriction introduced by the quantum mechanical selection rule is removed due to the coupling of heavyhole, light-hole and spin–orbit split-off subbands.
  P型量子阱红外探测器 (QWIP) 可以直接检测垂直入射的光，因为由量子力学选择规则引入的限制由于重空穴、轻空穴和自旋轨道分裂子带的耦合而被去除。
- P-type QWIPs have the same device structure as n-type except
	- the wells are $p$-type
	- the contact layers are $p^+$-type

#### Device Example

![[Pasted image 20241103210324.png]]
- A $p$-type QWIP contains 35 period of InGaAs/AlGaAs QWs with two contacting layers on top and at bottom.
  一个$p$型量子阱红外探测器 (QWIP) 包含35个周期的InGaAs/AlGaAs量子阱，并在顶部和底部有两个接触层。
- The wells are Be-doped and 3.5 nm thick, and the barriers are 30 nm thick.
  阱层掺有铍，厚度为3.5nm，势垒层厚度为30nm。
- The QWIP devices are $200\mu \text{m}$ in diameter.
  这个量子阱红外探测器（QWIP）器件的直径为$200\mu\text{m}$

![[Pasted image 20241103211618.png#pic_center|]]

#### Dark Current

- By applying a voltage to the detector without incident light, dark current $I_d$ can be measured at different temperatures.
  通过在无入射光的情况下对探测器施加电压，可以在不同温度下测量暗电流$I_d$。
- The $I_d$ can also be measured at different biases at a fixed temperature.
  在固定温度下，$I_d$也可以在不同偏压下测量。
![[Pasted image 20241103212515.png#pic_center|]]
- At $\text{80K}$ at $\text{1V}$, $I_d$ is about $10^{-9}\text{A}$, which was the lowest reported.

#### Light Detection

![[Pasted image 20241103213141.png#pic_center|]]
- Photocurrent is due to the transition of holes from ground level to the excited level.
  光电流是由于空穴从基态跃迁到激发态所致。
- Detected Wavelength $\lambda_p$ varies with well width, barrier height, and doping density in the wells.
  检测波长$\lambda_p$随阱宽、势垒高度和阱内掺杂浓度变化。
![[Pasted image 20241103213018.png#pic_center|]]
- $\lambda(\mu \text{m})=10,000/\text{Wave\ Number}$

#### Example: Effect of Doping Concentration

![[Pasted image 20241103213507.png#pic_center|Absorption Spectra]]
- Absorption spectra of three $p$-type InGaAs/AlGaAs QWIPs with different doping densities in the wells.
  三种不同掺杂浓度的$p$型InGaAs/AlGaAs量子阱红外探测器(QWIP)的吸收光谱。
- $\lambda_p$ varies from $8.35$ to $8\mu \text{m}$

![[Pasted image 20241103214037.png]]
- $\lambda_p$ shifts to smaller wavelength as doping concentration in the wells increases. (Heavy doping in the well material causes shrinkage of energy bandgap, which makes the $E_2-E_1$ increased and $\lambda=\frac{hc}{E_2-E_1}=\frac{1.24}{E_2-E_1}$ reduced)
  随着阱内掺杂浓度的增加，$\lambda_p$向短波长方向偏移。（阱材料中的重掺杂导致Bandgap带隙缩小，使得$E_2-E_1$增大，进而$\lambda=\frac{hc}{E_2-E_1}=\frac{1.24}{E_2-E_1}$减小）

# Summary

The operation of the four groups of photonic devices: LEDs, laser diodes, photodetectors, and solar cells depends upon the emission or absorption of photons. Recombination of electrons and holes can emit photons. Absorbed photons can excite electrons and holes.
四种光电子设备：LED、激光二极管、光探测器和太阳能电池依赖光子的吸收和发射过程。电子和空穴的复合能够产生光子，吸收光子可以激发电子和空穴。

A laser diode is a p-n junction operated under forward bias condition. The diode structure must provide the confinement of the carriers and the optical field so that the stimulated emission condition can be established. Laser diodes have evolved from the homojunction, to heterojunction and to quantum-well structures. The main objectives are to lower the threshold current density for lasing and to have all emitted photons at a single frequency. The laser diode is a key device for long distance, optical fiber communication systems. It is also extensively used for video recording, high-speed printing, and optical reading.
激光二极管是一个在正向偏置条件下工作的p-n结。二极管结构必须提供载流子和光场的约束，以便建立受激发射条件。激光二极管的发展经历了从同质结到异质结再到量子阱结构的过程。主要目标是降低激光的阈值电流密度，并使所有发射的光子在同一频率上。激光二极管是长距离光纤通信系统的关键设备，也广泛用于视频录制、高速打印和光学读取。

There are subbands in the n-well and p-well. Their energy and densities can be estimated. Different from DH and Quantum-Well lasers, the Quantum-Well infrared photodetectors are based on intersubband transitions. It means that the carrier (electron or hole) in the ground states can excited up to the higher-energy subband after absorbing a photon in the wells, and vice versa. The energy of the photon absorbed is equal to the difference of the two subbands. This is the Band-to-band transition.
n型阱和p型阱中存在子带。它们的能量和密度可以估计得到。与双异质结和量子阱激光器不同，量子阱红外探测器基于子带间跃迁。这意味着载流子（电子或空穴）在基态中可以在阱中吸收光子后激发到更高能量的子带，反之亦然。吸收的光子的能量等于两个子带之间的差值。这就是带到带的跃迁。
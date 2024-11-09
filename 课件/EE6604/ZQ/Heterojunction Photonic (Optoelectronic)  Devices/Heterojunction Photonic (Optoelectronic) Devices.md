---
aliases: 
tags:
  - heterostructure
---

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
	- [[Population Inversion]]
	  粒子数分布反转
	- [[Carrier and Optical Confinements]]
	  载流子和光学限制
	- [[Optical Cavity]]
	  光学谐振腔

## Double-Heterojunction (DH) Laser

[[Double-Heterojunction (DH) Laser]]
## Quantum Well Lasers

[[Quantum-Well Lasers]]

## Surface Emitting Lasers

[[Surface Emitting Lasers]]

# Quantum-Well Infrared Photodetectors

- The quantum well lasers (你在搞什么？这里是Laser吗？是Photodetectors吧) rely on transitions of carriers between the conduction band and valence band, (called interband transitions). The energy of the photons generated is approximately equal to the bandgap energy.
  
- Device applications can also rely on **intersubband transitions**.
  
## Subbands in Quantum-Wells

[[Subbands in Quantum-Wells]]

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
  注意：由于带内跃迁偏振选择规则的限制，n型QWIP不能检测垂直入射的光子。垂直入射时光子的电场方向在电子跃迁方向上没有分量，不能激发电子。
- If ones use n-type QWIPs to detect normal incident photons, gratings on top should be fabricated so that the normal incidence could have an angle when reaches the QWs.
  如果要用n型QWIP检测垂直入射的光子，其上需要制造一个光栅使入射光在抵达量子阱时存在一定角度

#### Dark Current and Photocurrent

![[Pasted image 20241103195309.png#pic_center|]]
- Dark Current is the current measured by applying a bias when no light illuminates the QWIPs
- The dark current $I_d$, is mainly due to tunneling $I_t$ and thermionic emission $I_{\mathrm{thermonic}}$, $I_d=I_t+I_{\mathrm{thermonic}}$
- Dark Current is a background current, the smaller the better.

- Photocurrent is due to the electrons jumped from ground level to the excited level after absorbing incident photons. $$I_p=n_pq\mu \xi$$where:
	- $n_p$ is the photogenerated electron concentration
	- $\mu$ is [[Carrier Mobility]]
	- $\xi$ is electrical field

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

Theoretically, according to infinitely deep QW ([[Subbands in Quantum-Wells#Energy of Subbands|Energy of Subbands]]): $$E_2-E_1=\frac{3\hbar^2\pi^2}{2mW^2}=\frac{hc}{\lambda}$$ $$\lambda=\frac{hc}{E_2-E_1}=DW^2$$
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

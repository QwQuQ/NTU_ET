- Dry etch creates minimal resist lifting
  由于干式蚀刻很精确，所以光刻胶的剥离也少
- Dry etch processes use less chemicals than wet etch processes
- Plasma-induced damage is more common in dry etch processes
- The complexity and cost of dry etch equipment is higher

# Plasma Generation and Processes

- Plasma
	- An ionised gas with about equal amounts of positive ions and negatively charged particles
	  一种含有大约等量的正离子和带负电荷的粒子的电离气体
	- Usually electrons, positive ions, and a small amount of negative ions
	  通常是电子、正离子和少量负离子
	- It has a neutral charge in macroscopic sense
	  它在宏观意义上呈电中性

## Plasma Generation

![[Pasted image 20250222020841.png#pic_75center|]]

 - A neutral gas is placed within a tube with a DC potential applied across two electrodes
   将中性气体放置在管内，在两个电极之间施加直流电势
 - The released electrons accelerate toward the positive electrode or anode, and along the way undergo a series of elastic and inelastic collisions, and the plasma is therefore formed
   释放的电子向正极或阳极加速，并在此过程中经历一系列弹性和非弹性碰撞，从而形成等离子体
 - Kinetic energy is conserved in elastic collisions. An electron has a smaller mass than an atom, the energy transfer is negligible and the electron will simply change direction
   动能在弹性碰撞中是守恒的。电子的质量比原子小，能量转移可以忽略不计，电子只会改变方向
 - All other types of electron collision are inelastic and will result in ionised species or excited neutral species in the plasma
   所有其他类型的电子碰撞都是非弹性的，会导致等离子体中的电离物质或激发的中性物质

### Ionisation & Recombination

- **Ionisation**
	- Electron impact ionisation (**inelastic collisions**)
	  电子碰撞电离（**非弹性碰撞**）
	- The primary electron removes an electron from the atom, producing a positive ion and two electrons
	  初级电子从原子中移除一个电子，产生一个正离子和两个电子
	- 例子：$$e^-+M\rightarrow M^++2e^-$$其中$M$为气体分子
- **Recombination**
	- Inverse process of ionisation
	  电离逆过程
	- An **electron coalesces with a positive ion** to form a neutral atom
	  **电子与正离子结合**形成中性原子
	- 例子：$$e^-+M^+\rightarrow M$$

## Excitation & Relaxation

- **Excitation**
	- Energy provided to atoms enables the electron to jump to a higher energy level within the atom with a corresponding quantum absorption of energy, but insufficient to ionise the atom
	  提供给原子的能量使电子能够在原子内跃迁到更高的能级，并相应地吸收能量，但不足以电离原子
	- It can result from both electron impact excitation or photo excitation
	  它可能是由电子碰撞激发或光激发引起的
	- 例子：$$e^-+M\rightarrow M^*+e^-$$
- **Relaxation**
	- Inverse process of excitation
	- The excited states are rather unstable and the electron configuration soon returns to the ground state in one or several transitions, with lifetimes varying from nanoseconds to seconds
	  激发态相当不稳定，电子结构很快就会在一次或多次跃迁中恢复到基态，寿命从纳秒到秒不等
	- Each transition is accompanied by the emission of a photon of various specific energy $h \nu$
	  每个跃迁都会伴随着各种特定能量 $h \nu$ 的光子的发射

## Dissociation of Gas Molecules

> Dissociation: 分解

![[Pasted image 20250222021931.png#pic_33center|]]
- As the energy of plasma electrons is much higher than the chemical bond energy, molecules in a plasma are essentially randomised, breaking down into all conceivable fragments
  由于等离子体电子的能量远高于化学键的能量，等离子体中的分子基本上是随机的，分解成所有可能的碎片
- For example, a plasma of methane ($\mathrm{CH_4}$) can be expected to include the fragments of $\mathrm{CH_3}$, $\mathrm{CH_2}$, $\mathrm{H}$ and $\mathrm{C}$
  例如，甲烷等离子体（$\mathrm{CH_4}$）可能包括$\mathrm{CH_3}$、$\mathrm{CH_2}$、$\mathrm{H}$和$\mathrm{C}$的碎片

## $\mathbf{CF_4}$ Gas

- Dissociation:$$\mathrm{CF_4}+e^-\rightarrow \mathrm{CF_3}+e^-$$
- Ionisation:$$\mathrm{CF_3}+e^-\rightarrow \mathrm{CF_3}^+2e^-$$
- Dissociative Ionisation:$$\mathrm{CF_4}+e^-\rightarrow \mathrm{CF_3}^++\mathrm{F}+2e^-$$
- Excitation: $$\mathrm{CF_4}+e^-\rightarrow \mathrm{CF_4}^++e^-$$
- Recombination: $$\mathrm{CF_3}^++\mathrm{F}+e^-\rightarrow \mathrm{CF_4}$$ $$\mathrm{F}+\mathrm{F}\rightarrow \mathrm{F_2}$$

# Plasma Interaction with the Substrate

## Physical Interaction (Sputter Etching)

![[Pasted image 20250222024107.png#pic_50center|Sputter Etching]]

- Surface bombarded with energetic ions. The ions' loss of kinetic energy on the surface dominates the interaction. E.g. Argon (inert gas) plasma etching
  表面受到高能离子的轰击。离子在表面上的动能损失主导了相互作用。例如氩（惰性气体）等离子体蚀刻
- High particle energy ($>500e\mathrm{V}$) noble gas ions ($\mathrm{Ar^+}$) created by DC/RF power to remove the target surface
  由DC或者RF能量产生的高能高稀有气体粒子，用来去除表面
- Operatin pressure: 0.01 to 0.1 torr
  工作压力：0.01至0.1托
  > Torr: 是一种压力单位，通常用于测量真空系统中的气压。1 Torr 等于 1 毫米汞柱（mmHg），也大约等于 133.322 帕斯卡（Pa）
- Interaction is purely physical, with no chemical reaction between the gas ion and the target
  相互作用是纯物理的，气体离子和靶之间没有化学反应
- Due to the vertical bombardment of ions onto the target surface, good anisotropy can be achieved
  由于离子垂直轰击靶表面，可以实现良好的各向异性
- Poor selectivity (no differentiation between different target elements)
  选择性差（不同目标元素之间没有区别）
---
- Argon gas is usually used for physical plasma etching:
	- Argon is an inert gas
	  氩气是一种惰性气体
	- Relatively heavy gas for momentum transfer
	  较重的气体，用于动量传递
	- High energy bombardment to sputter away the surface
	  高能轰击以溅射掉表面
![[Pasted image 20250222024615.png#pic_33inline|]]![[Pasted image 20250222024635.png#pic_33inline|]]
- Sputter Yield:
	- Ratio of the number of ejected target atoms per bombarding ion at a given energy
	  给定能量下，每一个离子轰击走的原子数
	- Yield depends on the angle of ion flux
	  产量取决于离子通量的角度

## Physical + Chemical interaction (reactive ion etching)

- In addition to physical etching, chemical erosion by the bombarding ions contribute to etching process. E.g.: $\mathrm{CF_4}$ (reactive gas) plasma etching
  除了物理蚀刻外，轰击离子的化学侵蚀也有助于蚀刻过程。例如：$\mathrm{CF_4}$（反应气体）等离子体蚀刻
- Reactive ions ($\mathrm{CF_4}$ is used to replace argon ions as the etchant)
  反应离子（氟化碳（$\mathrm{CF_4}$）用于替代氩离子作为蚀刻剂）
- Two etching mechanisms involved: physical and chemical mechanisms
	- Physical: Ion bombardment induced momentum transfer
	  离子轰击引起的动量传递
	- Chemical: Formation of volatile etch products between reactive etchants and target surface
	  在反应性蚀刻剂和目标表面之间形成挥发性蚀刻产物
- Since reactive ions are used as the etchant, such technique is usually called **Reactive ion Etching (RIE)**
  由于使用反应性离子作为蚀刻剂，这种技术通常被称为 **反应离子蚀刻（RIE）**
---
- RIE uses one or more reactive gases as the etchants
  RIE使用一种或多种反应性气体作为蚀刻剂
- Operating pressure: $10\mathrm{mtorr}-100\mathrm{mtorr}$ to confine the plasma between two parallel plates
  工作压力：$10\mathrm{mtorr}-100\mathrm{mtorr}$ 以将等离子体限制在两个平行板之间
- Substrates are normal to the gas flow and the RF field, resulting in a high degree of anisotropy because ions strike perpendicularly onto the surface
  衬底垂直于气体流动和射频场，从而导致高度各向异性，因为离子垂直撞击到表面
---
![[Pasted image 20250222030129.png#pic_50center|]]
- Two parallel electrode plates
  两个平行电极板
- Top electrode plate is grounded
  顶部电极板接地
- Bottom electrode is driven by a $13.56\mathrm{MHz}$ RF generator, connected through a capacitor and an impedance matching circuit
  底部电极由一个 $13.56\mathrm{MHz}$ 的射频发生器驱动，通过电容器和阻抗匹配电路连接
- The function of the capacitor is to block the electrode from discharging through the power supply
  电容器的功能是阻止电极通过电源放电
	- A blocking capacitor, normally available in the Tuning Network, acts as conductor for the RF AC field but also acts as an isolator for a self-induced DC field (preventing the discharging of electrons).
	  通常在调谐网络中用隔直电容器充当射频交流场的导体，但也充当自感直流场的隔离器（防止电子放电）
- The sample (substrate) is placed on the bottom electrode
  将样品（基板）放置在底部电极上
- Etch gas is fed into the etch chamber which is kept under a vacuum evacuated environment
  蚀刻气体被送入蚀刻室，蚀刻室保持在真空机抽真空的环境下
- Dark Space: Plasma sheath/dark space with high electric field region
  暗空间：具有高电场区域的等离子体壳层/暗空间。

### Operating Principles

1. Electrons in chamber gained energy by applied RF power.
   腔室内的电子通过施加射频功率获得能量
2. When the bottom electrode is positive, many highly mobile electrons are accelerated towards the electrode, causing a significant accumulation of negative charge.
   当底部电极为正极时，许多高度可移动的电子被加速向电极，导致负电荷的显著积累。
3. When the bottom electrode is negative and heavy, immobile ions accelerate towards it. However, only relatively few of these ions strike the electrode as compared to the number of electrons in the previous cycle. Hence, in a steady state, this electrode is negative biased, and therefore is called a cathode.
   当底部电极为负且较重时，静止的离子会向其加速。然而，与前一个循环中的电子数量相比，这些离子中只有相对较少的离子撞击电极。因此，在稳定状态下，该电极被负偏压，因此被称为阴极。
	1. The impinging of electrons on the powered electrode allow the buildup of a negative DC field in addition to the AC field. This negative potential is the DC self-bias.
	   电子撞击到供电电极上，除了交流电场外，还可以建立负直流电场。这种负电势是直流自偏压。
4. A high electric field region is then formed around the cathode. This region is known as the plasma sheath, or the dark space, where ion acceleration takes place before bombarding the electrode
   然后在阴极周围形成高电场区域。这个区域被称为等离子体鞘层或暗空间，在轰击电极之前，离子在这里加速
5. Ions are accelerated in dark space before bombarding the substrate
   在轰击基板之前，离子在黑暗空间中被加速

### Plasma Potential

![[Pasted image 20250222031521.png#pic_75center|]]

- The plasma potential is determined by the expression$$\left|Vc\right|=Va\left(\frac{Aa}{Ac}\right)^4$$其中：
	- $Vc$是通电电极（阴极）与等离子体之间的电势差
	- $Va$是接地电极（阳极）与等离子体之间的电势差
	- $\frac{Aa}{Ac}$是两个电极区域大小的比
- 阳极区域需要比阴极大$$\left|Vc\uparrow\right|=Va\left(\frac{Aa}{Ac}\uparrow\right)^{4}$$这样能够提高轰击离子的能量，从而提高蚀刻速率

### Ion Acceleration and Physical Plasma Interaction in RIE System

- The acceleration of ions by the high field region (dark space) in RIE system yields high energy ion bombardment on the substrate, resulting in the physical etching on the substrate.
  RIE系统中高场区域（暗空间）将离子的加速，高能粒子轰击在衬底上，导致衬底上的物理蚀刻。

### RIE Mechanism

![[Pasted image 20250222034644.png#pic_75center|]]

1. **Transportation**: The etchant (positive ions) accelerates to the substrate surface
   **运输**：蚀刻剂（正离子）加速到基板表面
2. **Adsorption**: The etchant chemisorbs onto the surface of the substrate
   蚀刻剂化学**吸附**在基材表面
3. **Reaction** with the substrate and the formation of the volatile by- product (gaseous form)
   与基板的**反应**及形成挥发性副产物（气态形式）
4. **Desorption** of the volatile by-product away from the substrate
   挥发性副产物从基板上**脱附**
---
![[Pasted image 20250222035355.png#pic_75center|]]
1. Etchant gases enter chamber
   蚀刻剂进入腔室
2. Dissociation of reactants by electric fields
   在电场作用下反应物的分解
3. Recombination of electrons with atoms creates plasma
   电子与原子复合形成等离子体
4. Reactive $\mathrm{+ions}$ bombard surface
   反应性正离子轰击表面
5. Adsorption of reactive ions on surface
   活性离子在表面吸附
6. Surface reactions of radicals and surface film
   自由基和表面薄膜反应
7. Desorption of by-products
   副产物解吸附
8. By-product removal
   副产物移除
---
- Etch Rate-Limited Conditions
	- **Transportation-limited condition**: The rate of etchant transportation is significantly slower than the etchant-substrate reaction rate. The rate of step (1) and (4) determines the overall etch rate in dry etching.
	  **运输限制条件**：蚀刻剂的运输速度明显慢于蚀刻剂与基材的反应速度。步骤（1）和（4）的速率决定了干法蚀刻中的整体蚀刻速率
	- Reaction-limited condition: The rate of etchant-substrate reaction rate is significantly slower than the rate of etchant transportation. The rate of step (2) and (3) determines the overall etch rate in dry etching.
	  **反应限制条件**：蚀刻剂-基板反应速率明显慢于蚀刻剂运输速率。步骤（2）和（3）的速率决定了干蚀刻的总体蚀刻速率

### Gases Used to Etch Films in Wafer Fabrication

- For etching of $\mathrm{Si}$-based films, fluorocarbon ($\mathrm{C_X F_Y}$)-based chemistry is used
  对于基于$\mathrm{Si}$的薄膜的蚀刻，使用基于氟碳化合物（$\mathrm{C_X F_Y}$）的化学物质
- For etching of organic films, oxygen-based chemistry is used
  对于有机薄膜的蚀刻，使用氧基化学物质
- For etching of metal lines, chlorine-based or fluorine-based chemistry is used
  对于金属线的蚀刻，使用氯基或氟基化学物质

### Plasma Etching of Silicon/ Silicon Oxide

- In the case of RIE of $\mathrm{SiO2}$ in $\mathrm{C_2 F_6}$ plasma, the dissociation process may produce:$$\mathrm{C_2F_6}\xrightarrow{e\text{-dissociation}}\mathrm{C_x F_y}^a, \mathrm{C}^b, \mathrm{F_z}^c$$
- Both carbon and fluorine can act as active etching species in this case,m with carbon responsible for reaction with $\mathrm{O_2}$ and fluorine with silicon
  在这种情况下，碳和氟都可以作为活性蚀刻物种，其中碳与 $\mathrm{O_2}$ 反应，而氟与硅反应
- The following etching mechanisms are proposed (*ads = adsorption*)
	- Chemisorption（化学吸收）：$$\mathrm{C_x F_y}^a,\mathrm{C}^b,\mathrm{F_z}^c\rightarrow \left(\mathrm{C_x F_y}\right)_{\text{ads}},\left(\mathrm{C}\right)_{\text{ads}}, \left(\mathrm{F_z}\right)_{\text{ads}}\left[+\text{electrons}\right]$$
	- Reaction（反应）：$$\left(\mathrm{C_x F_y}\right)_{\text{ads}},\left(\mathrm{C}\right)_{\text{ads}},\left(\mathrm{F_z}\right)_{\text{ads}}+\mathrm{SiO_2}\rightarrow w\left(\mathrm{SiF_4}\right)_{\text{ads}}+\left(\mathrm{CO_2}\right)_{\text{ads}}$$
	- Desorption（解吸附）：$$w\left(\mathrm{SiF_4}\right)_{\text{ads}}+\left(\mathrm{CO_2}\right)_{\text{ads}}\rightarrow w\left(\mathrm{SiF_4}\right)_{\text{gas}}+\left(\mathrm{CO_2}\right)_{\text{gas}}$$
  其中$w$, $x$, $y$, $z$为1或者2，$a$, $b$, $c$可以是任意正负电荷
- When only $\mathrm{CF_4}$ is used as the feed gas in RF plasma etch, no etching of $\mathrm{Si}$ or $\mathrm{SiO_2}$ occur
- Etching starts after $\mathrm{O_2}$ is added to the feed gas
- Atomic $\mathrm{F}$ is the active etchant for $\mathrm{Si}$ and $\mathrm{SiO_2}$ through the formation of the volatile $\mathrm{SiF_4}$ and $\mathrm{O_2}$: $$\displaylines{\mathrm{Si}+\mathrm{4F}\rightarrow \mathrm{SiF_4} \\ \mathrm{SiO_2}+\mathrm{4F}\rightarrow\mathrm{SiF_4}+\mathrm{O_2}}$$

### Tailoring Gas Composition for RIE (Addition of $\mathbf{O_2}$ Gas)

- Oxygen is added to $\mathrm{CF_x}$ plasma to increase the amount of reactive $\mathrm{F}$ species. Highly probable due to the presence of $\mathrm{O_2}$
  向 $\mathrm{CF_x}$ 等离子体中加入氧气以增加反应性氟（$\mathrm{F}$）物种的数量。由于存在氧气（$\mathrm{O_2}$），这一反应非常可能发生$$\mathrm{CF_2}+\mathrm{O}\rightarrow \mathrm{COF}+\mathrm{F}$$
- Oxygen reacts with $\mathrm{CF3}$ and $\mathrm{CF_2}$. Hence reducing the recombination rate of $\mathrm{F}$ and prevents the formation of the unreactive $\mathrm{CF_4}$. 
  氧气与 $\mathrm{CF_3}$ 和 $\mathrm{CF_2}$ 反应，从而减少氟（$\mathrm{F}$）的复合速率，并防止形成不活泼的 $\mathrm{CF_4}$ $$\mathrm{CF_2}+2F\rightarrow \mathrm{CF_4}$$可能性较小，因为形成了$\mathrm{COF}$
- However, the etch rate will decrease if more $\mathrm{O_2}$ is introduced, due to the dilution of $\mathrm{CF4}$ concentration
  翻译成中文：然而，如果引入更多的氧气（$\mathrm{O_2}$），蚀刻速率将会降低，因为氟化碳（$\mathrm{CF_4}$）浓度被稀释

# Factors Controlling the Plasma Etch Rate

## Steady State Pressure

- 系统的静压（$\rho$）可以表示为: $$p=\frac{F\cdot 760}{S}(\mathrm{Torr})$$其中：
	- $F$和$S$是进气速率和排气速率（$\text{litre}/\text{second}$，$1\mathrm{atm}=760\mathrm{Torr}$）
	- $p$是腔室中的压力

## Average Residence Time

- Residence time of a gas molecule is the average time it remains in the process chamber before being pumped away. Average residence time, $t_r$ (in seconds)
  气体分子的停留时间是指在被抽走之前，它在工艺腔内停留的平均时间。平均停留时间，$t_r$（以秒为单位）$$t_r=\frac{V\cdot p }{760\cdot F}$$其中：
	- $V$是腔室的体积
- 将上述两式联立可以得到：$$t_r=\frac{V}{S}$$
- For a constant $S$, $t_r$ does not vary with the changing pressure brought about by the change in flow rate ($F$). Hence, we should not assume that increasing $F$ will increase the residence time and the corresponding etch rate.
  对于常数$S$，$t_r$ 不随流速($F$)变化带来的压力变化而变化。因此，我们不应该假设增加流速($F$)会增加停留时间及相应的蚀刻速率。（上面那个公式不是一个决定式，仅用于计算）

## Throughput/Gas load

- Throughput or the gas load $Q$, equals to $pS$ (pressure times the pumping speed)
  通量或气体负荷$Q$等于$pS$（压力乘以抽速）$$Q=pS$$
- Hence, it is proportional to the flux of molecules passing through the pump
  因此，它与通过泵的分子流量成正比
- Units for throughput is $\text{torr litre}/\text{second} (\mathrm{lt/s})$, but standard cc per minute (sccm) is more commonly used. Standard referring to standard temperature (°C) and standard pressure (1 atm, or 760 torr)$$1\mathrm{sccm}=\frac{10^{-3}[\text{litres}]\times760 [\text{torr}]}{60[\text{s}]}=0.01266$$ $$1 \mathrm{torr\ litre/s}=78.9\mathrm{sccm}$$

## Practice 

- A conventional $13.56\mathrm{MHz}$ parallel plate reactive ion etching (RIE) system was deployed to etch $\mathrm{SiO_2}$ film with $\mathrm{C_2 F_6}$ plasma. The cathode plate of the RIE system has a diameter of $20\mathrm{cm}$ and a chamber volume of $20\mathrm{L}$. The etching was carried out at a cathode potential ($Vc$) of $-450\mathrm{V}$ with a $\mathrm{C_2 F_6}$ flow rate of $25\mathrm{mL}/\mathrm{s}$ and a radio-frequency (RF) power of $\mathrm{100W}$. The average residence time of the plasma is $1 \mathrm{second}$.

- The power density of the process
  功率密度是射频功率与阴极面积的商（在这里是一个平面的功率）
  $$\frac{100\mathrm{W}}{\pi (\frac{20\mathrm{cm^2}}{2})}\approx 0.318 \mathrm{W\cdot cm^{-2}}$$
- The anode diameter, assuming the anode potential ($Va$) of $15\mathrm{mV}$
  根据阴极阳极电势差和面积的公式$$\displaylines{\left|Vc\right|=Va\left(\frac{Aa}{Ac}\right)^4 \\ \implies\sqrt[4]{\frac{Vc}{Va}}Ac=Aa \\ \implies\sqrt[4]{\frac{450\mathrm{V}}{0.015\mathrm{V}}}\times(20\mathrm{cm})^2\times\pi=\pi\times(D_{\text{anode}})^2 \\ \implies D_{\text{anode}}\approx72.6\mathrm{cm}}$$
- The etch pressure of the chamber
	- 题干给出的信息有：
		- 进气流量$F=25\mathrm{mL}\cdot \mathrm{s^{-1}}$
		- 腔室容积$V=20\mathrm{L}$
		- Average Residence Time: $t_r=1\mathrm{s}$
	- 能够参考的公式有：
		- Steady State Pressure: $$p=\frac{F\cdot 760}{S}$$但是pumping speed并未给出
		- Average Residence Times: $$t_r=\frac{V\cdot p}{760\cdot F}$$所有条件齐全
		- Throughput: $$Q=p\cdot S$$$Q$没有给出
	- 所以计算过程为：$$\displaylines{t_r\frac{V\cdot p}{760\cdot F} \\ \implies 1\mathrm{s}=\frac{20\mathrm{L}\times p}{760\cdot 25\mathrm{mL\cdot s^{-1}}} \\ \implies p=0.95 \mathrm{torr}}$$
- Calculate the speed of the pump
  套公式：$$p=\frac{F\cdot 760}{S}\implies S=20\mathrm{L\cdot s^{-1}}$$

# Plasma Damage and General Issues in Etching

## Plasma Damage

- High ion fluxes of $10^{15} \text{ion}/\mathrm{cm^2}$ are delivered at energies of 300 to 700 $eV$ in plasma etching
- The high ion bombardment energy causes damage to the material, and considerable degradation to the electrical and optical properties of devices
- The degree of damage is highly dependent on the accelerating potential and the mass of the ion species

![[Pasted image 20250222215532.png#pic_75center|]]

- **Edge Damage:** For materials near to patterned edges, the rebound ions, sputtered material and chemical reactants may also cause damage to the edge
  对于靠近图案边缘的材料，反弹离子、溅射材料和化学反应物也可能会对边缘造成损害
- **Surface Damage:** The principal source of surface damage may result directly from the ion flux
  表面损伤的主要来源可能直接来自于离子流
- **Sidewall Damage:** Sidewalls suffer damage form the direct bombardment by directional ions and reactive radicals, and possibly deposition and recocheting particles form the bottom surface
  侧壁受到定向离子和反应性自由基的直接轰击，以及可能来自底表面的沉积和反弹颗粒的损害

- Plasma damage会导致：
	- Reduce the carriers mobility of semiconductors
	  减少半导体的载流子迁移率
	- Deactivate dopants
	  使掺杂失活
	- Increase the resistivity
	  增加电阻
- Annealing of samples using a RTP(Rapid Thermal Processor) or furnace at temperatures in the range of 450 to 800 $\degree \mathrm{C}$ for a few seconds to a few minutes may partially or totally remove the damage
  使用RTP（快速热处理器）或炉子在450至800 $\degree \mathrm{C}$的温度范围内进行几秒至几分钟的退火处理，可能会部分或完全消除损伤

## Surface Contamination

![[Pasted image 20250222220620.png#pic_75center|]]

- Contaminants such as fingerprints, dust particles, etc. may contaminate the semiconductor by leaving behind non-volatile by-products.
  像指纹、尘埃颗粒等污染物可能会通过留下不挥发的副产物污染半导体
- These contaminants may deposit on the semiconductor surface and act as micro masks during the etching of the semiconductor
  这些污染物可能会沉积在半导体表面，并在蚀刻半导体时充当微掩膜
- These micro-masks could inhibit the subsequent etching of the semiconductor and also cause the etched surface to be rough
  这些微掩膜可能会抑制随后的半导体蚀刻过程，并使蚀刻表面变得粗糙

## General Issues Associated with Etching

- **Uniformity**: Across wafer
- **Etching rate**: Fast enough to be practical, and slow enough to be controllable
- **Selectivity**: Should be high
- **Anisotropy**: Directional dependence of etch rate
- **By-products**: Volatile or otherwise, easily removed

# Plasma Etching Conditions and Issues

- Parameters that can be directly controlled in standard parallel plate systems:
	- RF Power
	- Pressure
	- Gas Compositions
	- Flow Rates

## Power Density

- $\text{Power Density} \sim 0.1 \text{ to } 5 \mathrm{W\cdot cm^{-2}}$
- $\text{Power density on the wafer} \sim 0.1 \text{ to }3\mathrm{W\cdot cm^{-2}}$
- $\text{Power density to generate the plasma}\sim 3\text{ to }10\mathrm{W\cdot cm^{-2}}$
- Increasing the RF power increases the plasma density and the self-bias (voltage drop between the plasma and electrodes), which increases the ion energy ($10-700 V$ range)
  增加射频功率会增加等离子体密度和自偏压（等离子体与电极之间的电压降），从而增加离子能量（$10-700$V范围）
- HDP systems: Separate power sources for the plasma and wafer bias (Can achieve high density without necessarily getting high ion energy)
  HDP 系统：为等离子体和晶圆偏压提供独立的电源（可以在不获得高离子能量的情况下实现高密度）

## Pressure Range in Plasma Etching

- Reactive ion etching: $10\text{ to } 100 \mathrm{mTorr}$
- HDP System: $1\text{ to }10\mathrm{mTorr}$ (biasing chamber)
- Increasing the pressure causes more gas phase collisions to occur, decreasing the directionality of the etching
  增加压力会导致更多气相碰撞发生，从而减少蚀刻的方向性
- Increasing the pressure also increases the plasma density, up to certain point
  增加压力也会在一定程度上增加等离子体密度
- Above a certain pressure, the collisions between the gas molecules and electrons limit the energy of the electrons and thus limit the ionization rate
  在超过某个压力后，气体分子与电子之间的碰撞会限制电子的能量，从而限制电离率

## Temperature

- Except during Al etching, the temperature of the etch system is not intentionally raised during plasma etching
  除了在铝（Al）蚀刻过程中，等离子蚀刻期间通常不会故意升高蚀刻系统的温度。
- Plasma supplies the energy for the process, and heating the gas or wafer does not generally increase the etch rate or improve the process
  等离子体为工艺提供能量，加热气体或晶圆通常不会增加蚀刻速率或改善工艺。
- Exception: during Al etching, heat the system to 35-65C, to help keep the species volatile and remove byproducts
  例外：在铝蚀刻过程中，将系统加热到35-65摄氏度，以帮助保持物质挥发性并去除副产物
- Unintentional heating may occur ($\sim 90 \text{ to }100\degree C$). Need to control this because, for example, sidewall inhibitor deposition decreases as temperature goes up, hence less directional etching
  在这个温度下，可能存在不必要的加温。需要控制这一点，因为例如，随着温度升高，侧壁光刻胶沉积减少，从而导致蚀刻的方向性降低。
- Recent trends: better wafer temperature control (heat removal at the chuck)
  最新趋势：更好的晶圆温度控制（在卡盘处散热）

## Macroscopic Loading Effects

- Depletion of the etchant species can occur across the wafer or across the etch chamber
  刻蚀剂的消耗可能发生在整个晶圆或刻蚀腔内
- "Macroscopic Loading" – more wafers in the chamber or more area exposed on each wafer (depends upon the mask pattern), results in a slower etch rate
  **宏观负载**：腔室内的晶圆数量增加或每个晶圆上暴露的区域增加（取决于掩膜图案），会导致蚀刻速率变慢
- Loading effect can be described by this equation: $$R=R_0/(1+kA)$$其中：
	- $R_0$是空腔体的蚀刻率
	- $A$是暴露的需要蚀刻区域的面积
	- $k$是常数
- 这很难控制，一般都是经验结论

## Micro-loading Effects

![[Pasted image 20250222230533.png#pic_75center|]]

- "Micro-loading" – the etch rate varies over small distances on the surface of the wafer
  **微观负载**：蚀刻速率在晶圆表面的小距离内变化
	- Density of the unmasked area can vary over small distances, depending upon the mask pattern, resulting in differences analogous to macroscopic loading
	  未掩膜区域的密度会因掩膜图案的不同而在小距离内变化，导致类似于宏观负载的差异
	- Differences in aspect ratios (AR dependent etching - ARDE, also called RIE lag). Lower etch rate for higher AR trenches (smaller widths)
	  纵横比差异（AR依赖蚀刻：ARDE，也称为RIE滞后）。纵横比较高的沟槽（较小的宽度）蚀刻速率较低。
		- **等离子体进入困难**：等离子体中的离子和自由基难以深入到底部，从而导致蚀刻速率下降
		- **副产物堆积**：蚀刻过程产生的副产物更容易堆积在沟槽底部，进一步阻碍蚀刻反应
		- **反应物供应不足**：高纵横比沟槽的狭窄空间限制了反应物的供应，导致蚀刻速率降低
	- 高AR的蚀刻要求各向异性程度高（不然侧面会被蚀刻掉）


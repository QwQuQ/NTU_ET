---
aliases:
  - Heterojunction Bipolar Transistors
  - 异质结双极型晶体管
tags:
  - HBT
  - heterostructure
---
The bandgap of a [[Vegard’s Law#Ternary Alloys|Ternary or Auaternary Alloy]] semiconductor can be varied, by simply adjusting the composition $x$ or $y$.
[[Vegard’s Law#Ternary Alloys|三元合金或四元合金半导体]]的带隙可以通过简单地调整组成$x$或$y$来改变。

The heterostructures formed by alloy semiconductors, therefore, have immense applications in various fields.
因此，合金半导体形成的异质结在各个领域都有巨大的应用。

## Limitations of Homojunction BJTs

![[HBT_FIG1.png|Carrier Distribution]]

- The [[Emitter Injection Efficiency]] $\gamma$ is:
  发射极注入效率$\gamma$是：$$\gamma=\frac{I_{En}}{I_{En}+I_{Ep}}$$ since $I_{Ep} \ll E_{En}$, if follows:
  因为$I_{Ep} \ll E_{En}$，它遵守：$$\gamma=1-\frac{p_{E0}D_E W_{bn}}{n_{B0}D_BL_E}$$ where,
	- $p_{E0}$: Equilibrium hole concentration in the emitter
	  发射极热平衡载流子浓度
	- $n_{B0}$: Equilibrium electron concentration in the base
	  基极热平衡载流子浓度
	- $W_{bn}$: Neutral width of the base
	  基极的特征长度（？）
	- $D_E$, $D_B$: Diffusion coefficients of minority carriers in emitter and base respectively
	  少数载流子在发射极和基极的扩散系数
	- $L_E$: Diffusion length of minority carriers in the emitter
	  少数载流子在发射极中的扩散长度
- The [[Base Transport Factor]] $\alpha_T$ is:
  基极传输因子$\alpha_T$为：$$\alpha_T=\frac{I_{Cn}}{I_{En}}\approx \frac{I_C}{I_{En}}=1-\frac{W_{bn}^2}{2L_B^2}$$ where, 
	- $L_B$: The diffusion length of minority carriers in the base
	  基区中少数载流子的扩散长度
- The [[Common Base Current Gain]] $\alpha_0$ is:
  共基极电流增益为：$$\alpha_0=\frac{I_C}{I_E}=\frac{I_C}{I_{En}}\cdot \frac{I_{En}}{I_E}=\alpha_T\cdot \gamma$$ Substituting the expressions for $\alpha_T$ and $\gamma$, we get $$\alpha_0=\left[1-\frac{W_{bn}^2}{2L_B^2}\right]\cdot \left[1-\frac{p_{E0}D_E W_{bn}}{n_{B0}D_B L_E}\right]$$
- The [[Common Emitter Current Gain]] $\beta_0$ is:
  共发射极电流增益为：$$\beta_0=\frac{\alpha_0}{1-\alpha_0}\approx\frac{n_{B0}D_B L_E}{p_{E0}D_EW_{bn}}$$ To achieve a high $\beta_0$,
  为了达到高$\beta_0$
	- $p_{E0} \ll n_{B0} \implies n_{E0} \gg p_{B0}$
	- $W_{bn}$ is very small, and $W_{bn} \ll L_B$
  These mean
	- Emitter doping should be very high and base doping should be relatively much lower.
	  集电极掺杂需要非常高，但是基极的掺杂相对非常低
	- The base should be very narrow.
	  基极需要非常窄

### Limitations

- Too narrow and lightly doped base will result in
  基区过窄和轻掺杂会导致：
	- Large base resistance
	  基区电阻大
	- Smaller breakdown voltage
	  击穿电压小
- Too heavy doping in emitter will cause bandgap of emitter to shrink.
  发射极重掺杂会导致带隙缩小

It will then cause the base injection to increase, emitter injection to decrease and eventually leading to decrease in the emitter efficiency and current gain.
这将导致基极注入增加，发射极注入减少，最终导致发射极效率和电流增益降低。

#### Effect of Emitter Doping

The bandgap shrinkage caused by heavy doping in the n-type emitter results in a higher barrier for electron injection and lower barrier for hole injection. ^099bec
n型发射极中重掺杂引起的带隙缩小导致电子注入的势垒更高，空穴注入的势垒更低。

![[HBT_FIG2.png]]

In Si, the bandgap shrinkage due to doping is approximately given by
硅中由于重掺杂效应的带隙缩小为$$\Delta E_g=-22.5\left(\frac{N_d}{10^{18}}\cdot\frac{300}{T}\right)^{1/2}(meV)$$
and the [[Common Emitter Current Gain]] becomes
共射电流增益变成$$\beta\approx \beta_0 exp(-\frac{\left|\Delta E_g\right|}{kT})$$ decreasing with heavy doping.
随着掺杂变重而缩小

Thereffore, with a simple n-p homojunction for the emitter-base, the performance of the npn BJT is limited.
因此，由于BE区采用简单的n-p同质结，npn BJT的性能受限。

## Remedy

- Use a large bandgap material for n-type emitter. The deivce will then become a heterojunction bipolar transistor (HBT)
  在n型发射极使用带隙更大的材料。这个器件会成为异质结双极型晶体管
- The main advantage of HBT is the high emitter efficiency
  HBT主要的优势是发射极高效率
- HBTs also have high speed and high frequency capability in circuit operation
  HBT也有高速和高截止频率的工作特性

![[HBT_FIG3.png|A HBT with an n-AlGaAs emitter and a p-GaAs base transistor (a) Device structure, (b) Band diagram at thermal equilibrium]]

### Common Emitter Current Gain of HBTs

- From the definition, $$\beta_0\approx\frac{n_{B0}D_B L_E}{p_{E0}D_E W_{bn}}$$ and from [[PN Product#Law of Mass Action|Law of Mass Action]], $np=n_i^2$, the minority carrier concentration in the emitter $p_{E0}$, is
  发射极中的少数载流子浓度可以表示为（使用掺杂浓度代替多子浓度）：$$p_{E0}=\frac{n_o^2(\mathrm{emitter})}{N_E(\mathrm{emitter})}=\frac{N_CN_V exp(-\frac{E_{gE}}{kT})}{N_E}$$ where,
	- $N_C$: [[Effective Density of States]] in the conduction band
	  导带有效态密度
	- $N_V$: Effective Density of States in the valence band
	  价带有效态密度
	- $E_{gE}$ is the bandgap of the emitter
	  发射级的带隙
- The minority carrier concentration in the base $n_{B0}$ is
  基极的少数载流子浓度为：$$n_{B0}=\frac{n_i^2(\mathrm{base})}{N_B(\mathrm{base})}=\frac{N_C^\prime N_V^\prime exp(-\frac{E_{gB}}{kT})}{N_B}$$ where, 
	- $N_C^\prime$ and $N_V^\prime$: [[Effective Density of States]] in conduction band and valence band respectively
	  导带和价带的有效态密度
	- $E_{gB}$: bandgap of base
	  基极的带隙

Hence $$\displaylines{\beta_0=\frac{n_{B0}D_B L_E}{p_{E0} D_E W_{bn}}\approx \frac{N_E D_B L_E}{N_B D_E W_{bn}}exp(\frac{E_{gE}-E_{gB}}{kT})\\=\frac{N_E D_B L_E}{N_B D_E W_{bn}}exp(\frac{\Delta E_g}{kT})}$$

![[HBT_FIG4.png#pic_center|]]

- Note that even if the base is heavily doped, the barrier for hole injection will be very high due to the large $\Delta E_V$ of E-B junction.
  注意，如果基极是重掺杂的，空穴注入的势垒由于E-B的$\Delta E_V$变大将会变得非常高
	- This means that one can dope the base heavily and achieve low base resistance.
	  这意味着基极可以重掺杂以达到很小的基极电阻
	- One can also make the base narrower to achieve high speed.
	  也可以让基极更薄来达到更高的速度
	- Thus, all our requirements for a good performance transistor can be met by having a larger band gap emitter.
	  至此，所有我们对于高性能晶体管得需求都可以通过一个大带隙的发射极解决

### Further Description

The superior performance of the HBT results directly from the valence-band discontinuity $\Delta E_V$ at the heterointerface (E-B junction). $\Delta E_V$ increases the **valence band barrier height** in the E-B heterojunction and thus **reduces the injection of holes from the base to the emitter**.
HBT的好性能直接来自于价带的$\Delta E_V$，它增加了E-B结价带的势垒高度从而减少了空穴从基极注入发射极

- This effect in the HBT allows the use of a heavily doped base while maintaining a high emitter efficiency and current gain. The heavily doped base can reduce the base sheet resistance. In addition, the base can be made very thin without concern about the punch-through effect in the narrow base region.
  这个效应使得异质结双极性晶体管（HBT）在使用重掺杂基区的同时保持高发射效率和电流增益。重掺杂基区可以降低基区电阻。此外，可以将基区做得非常薄，而不必担心在窄基区中发生击穿。
- A thin base region is desirable because it reduces the base transit time and enhances the cutoff frequency.
  薄基区是可取的，因为它减少了基区的渡越时间并提高了截止频率。

### Example

A HBT has a bandgap of $1.62eV$ for the emitter, and a $1.42eV$ for the base. A BJT has a bandgap of $1.42eV$ for both the emitter and base materials. It has an emitter doping of $10^{18}cm^{-3}$ and a base doping of $10^{15}cm^{-3}$.
1. If the HBT has the same doping as the BJT, find the improvement of $\beta_0$.
2. If the HBT has the same emitter doping and the same $\beta_0$ as the BJT, how much can we increase the base doping of the HBT? Assume that all other device parameters are the same.

#### Solution

1. 列出本征共射电流增益$\beta_0$的公式：$$\beta_0\approx \frac{N_E D_B L_E}{N_B D_E W_{bn}}exp\left(\frac{E_{gE}-E_{gB}}{kT}\right)$$ 在本题中HBT和BJT有着相同的掺杂浓度，所以可以得出：
	- $N_E(HBT)=N_E(BJT)$
	- $N_B(HBT)=N_B(BJT)$
	- 假设$D_B$、$D_E$、$L_E$、$W_{bn}$也是相同的（这也没说啊）
	- $\Delta E_g(HBT)=1.62-1.42=0.2eV$
	- $\Delta E_g(BJT)=0eV$
	所以可以得出：$$\displaylines{\frac{\beta_0(HBT)}{\beta_0(BJT)}=\frac{exp\left(\Delta Eg(HBT)/kT\right)}{exp(\Delta E_g(BJT))}=exp(\Delta E_g(HBT)/kT)\\=e^{0.2eV/0.0259eV}=2257}$$ 记得在算$kT$的时候转化成电子伏特。
2. 还是列出本征共射电流增益$\beta_0$的公式：$$\beta_0\approx \frac{N_E D_B L_E}{N_B D_E W_{bn}}exp\left(\frac{E_{gE}-E_{gB}}{kT}\right)$$ 所以可以列出一个等式：$$\displaylines{\frac{N_E D_B L_E}{N_B(HBT)D_EW_{bn}}exp\left(\frac{\Delta E_g(HBT)}{kT}\right)\\=\frac{N_E D_B L_E}{N_B(BJT)D_EW_{bn}}exp\left(\frac{\Delta E_g(BJT)}{kT}\right)}$$ 约掉没有关系的东西：$$\frac{1}{N_B(HBT)}exp(\frac{\Delta E_g(HBT)}{kT})=\frac{1}{N_B(BJT)}$$ $$\displaylines{\implies N_B(HBT)=N_B(BJT)\cdot exp(\Delta E_g(HBT)/kT)\\=10^{15}\times e^{0.2/0.0259}=2.257\times 10^{18}cm^{-3}}$$

## Technologies Available

### $\mathrm{GaAs/AlGaAs}$ HBTs

The bandgap of $\text{AlGaAs}$ can be made much higher than $\mathrm{GaAs}$ and be used as an emitter material for HBT.
AlGaAs的带隙可以做得比GaAs高很多，可以用来当HBT的发射极
$$E_g(x)=1.42+1.247x\ \left(eV\right),\ x<0.45$$
$\mathrm{Al_x Ga_{1-x}}$ is [[Lattice-Matched Heterostructures|Lattice Match]] to $\mathrm{GaAs}$ for all composition $x$. $\mathrm{GaAs}$, with a high bandgap ($1.42eV$) compared to $\mathrm{Si}$, can form a high-quality substrate.
$\mathrm{Al_x Ga_{1-x}}$和$GaAs$在任何比例$x$下都是晶格匹配的，与硅对比有非常高的带隙，可以做一个高质量的衬底。

![[HBT_FIG5.png|(a) Schematic cross section of an n-p-n HBT structure, (b) Energy band diagram of a HBT operated under active mode.]]
The [[Common Emitter Current Gain]] varies with the [[Vegard’s Law#^648b21|Mole Fraction]] of $\mathrm{Al}$.
共射电流增益随着Al的摩尔分数改变而改变

### $\mathrm{InGaAs/InP}$ and $\mathrm{InGaAs/InAlAs}$ HBTs

- The $\mathrm{InP}$ based $\mathrm{In_{0.53}Ga_{0.47}As}$ ($E_g\cong 0.75eV$) and $\mathrm{In_{0.52}Al_{0.48}As}$ ($E_g=1.4eV$) are lattice matched to $\mathrm{InP}$ ($E_g=1.35eV$)
- $\mathrm{InGaAs}$ has smallest $E_g$ and should be used as base
- The $\mathrm{InGaAs/InP}$ (emitter) structure has very low [[Surface Recombination]]. And electrons have higher [[Carrier Mobility]] in $\mathrm{InGaAs}$ than in $\mathrm{GaAs}$. Such HBTs have a cutoff frequency of **254GHz**.
- Collector can be any one as long as the requirement for breakdown voltage can be met.
  集电极可以是任意材料，只要击穿电压能够满足

![[HBT_FIG6.png#pic_center|InAlAs as the emitter]]

![[HBT_FIG13.png#pic_center|InP as the emitter]]

![[HBT_FIG7.png#pic_center|Current gain as a function of operating frequency for an InGaAs/InP HBT.]]

### $\mathrm{Si/Si_x Ge_{1-x}}$ HBTs

- The alloy $\mathrm{Si_x Ge_{1-x}}$ will be the base due to a smaller band gap.
- $\mathrm{Si/SiGe}$ system is attractive for HBT due to:
	- high speed capability
	- small trap density at $\mathrm{Si}$ surface which minimizes [[Surface Recombination]] current and ensures a high current gain even at low collector current
	- compatibility with standard $\mathrm{Si}$ technology
![[HBT_FIG8.png#pic_center|Device structure of an npn Si/SiGe/Si HBT]]
![[HBT_FIG9.png#pic_center|Collector and base current versus Vbe for a HBT and BJT]]
The $\mathrm{Si/SiGe}$ HBT has a higher current gain than homojunction $\mathrm{Si}$ BJT, but a lower cutoff frequency than $\mathrm{GaAs}$ and $\mathrm{InP}$-based HBTs because of the lower carrier mobility in $\mathrm{Si}$.

## The Ways to Further Improve HBTs’ Performance

### Emitter Region

The conduction band discontinuity $\Delta E_C$ between the emitter and base is not desirable, since it will make the electrons to transport by means of [[Thermionic Emission]] across a barrier or by tunneling through it.
导带的不连续性是不被希望的，因为它会导致电子在运输过程中以热激发的方式运输或者隧穿过势垒。

![[HBT_FIG10.png#pic_center|]]

- Therefore, the emitter efficiency and the collector current will suffer.
  如此，发射极效率和集电极电流将遭罪
- The problem can be alleviated by using improved structures such as using an emitter with a graded-layer near the E-B junction.
  这一问题可以通过使用一个在E-B结附近渐变的发射极改善。
- The figure shows an energy band diagram in which the $\Delta E_C$ is eliminated by a graded layer placed between the emitter and base heterojunction. The thickness of the graded layer is $W_g$.
  这一张图展示了有渐变层情况下E-B结的$\Delta E_C$被尽可能减小，渐变层的厚度为$W_g$

![[HBT_FIG11.png#pic_center|The dashed line shows the energy bandgap of the graded layer.]]

### Base Region

- The base region can also have a graded profile, which results in a reduction of the bandgap from the emitter side to the collector side.
  基极也能用渐变的掺杂，这将导致带隙从从发射极向集电极方向减小
- There is an electric field $\xi_{bi}$ ($\xi=\frac{1}{q}\frac{\mathrm{d}E}{\mathrm{d}x}$) in the quasi-neutral base. It results in a reduction in the minority carrier transit time and, thus, an increase in the common-emitter current gain and the cutoff frequency of the HBT.
  在准中性的基区中存在一个电场$\xi_{bi}$，这将导致少数载流子寿命减小，从而导致HBT的共射电流增益和截止频率减小
- $\xi$ can be realized by varying linearly the $\mathrm{Al}$ [[Vegard’s Law#^648b21|Mole Fraction]] $x$ of $\mathrm{Al_x Ga_{1-x} As}$ in the base from $x=0.1$ to $x=0$.
  $\xi$可以在基极中线性地改变$\mathrm{Al_x Ga_{1-x} As}$的摩尔分数实现，从$x=0.1$到$x=0$

### Collector Region

- Two factors need to be considered for the collector layer:
  两个在集电极需要被考虑的因素
	- the transit time delay
	  传输时间延迟
	- the breakdown voltage
	  击穿电压
- A thicker collector layer will improve the breakdown voltage of the B-C junction but increase the transit time.
  一个更厚的集电极能够改善B-C结的击穿电压，但将导致传输时间增加
- In most devices for high-power applications, the carriers move through the collector at their saturation velocities but they need very large-electric fields to be maintained in this layer.
  在高功率设备中，载流子以速度饱和的速度通过基极但这需要在这一层中维持巨大的电场强度
- It is possible to increase the velocities by lowering the electric field with certain doping profile in the collector layer.
  降低电场强度但增加速度可以通过在集电极以特定掺杂方式实现
	- One way is to use $p^−$ or $i$ collectors with a $p^+$ pulse-doped layer near the subcollector for an n-p-n HBT.
	  一种方法是在npn HBT中使用$p^-$或者本征集电极和子集电极附近的一个$p^+$脉冲掺杂层
	
![[HBT_FIG12.png#pic_center|]]

Electrons entering the collector layer can maintain their higher mobility during most of the collector transit time due to the **slightly doped** $p^-$ collector (less impurity scattering). Such a device is called a **ballistic collector transistor (BCT)**.
电子在进入集电极时，在大部分集电极传输时间内，由于轻掺杂的$p^-$集电极（更少的杂质散射）能够维持它们的高迁移率。这种器件被称为弹道集电极晶体管（BCT，什么怪名字）

## SUMMARY

（这AI写的吧）
- The current gain and frequency limitations of a conventional bipolar junction transistor are the result of the [[课件/EE6604/ZQ/Heterojunction Electronic Devices/Heterojunction Electronic Devices#^099bec|Bandgap Shrinkage]] of emitter at high doping, low base doping and relatively wide base. To overcome these limitations, a heterojunction bipolar transistor (HBT) formed by using a wider bandgap semiconductor as emitter can have much high base doping and a much narrower base. The HBT has gained popularity in millimeter-wave and high-speed digital applications.
  由于高掺杂发射极带来的带隙缩小、低掺杂和相对宽的基极，传统BJT的电流增益和频率受到限制。为了解决这些限制，HBT通过使用大带隙半导体制作发射极以获得更高的基极掺杂浓度和更小的基极宽度。HBT逐渐在毫米波和高速数字领域受到青睐。
- The [[课件/EE6604/ZQ/Heterojunction Electronic Devices/Heterojunction Electronic Devices#Technologies Available|Technologies Available]] include $\mathrm{GaAs/AlGaAs}$ lattice matched to $\mathrm{GaAs}$ substrate, $\mathrm{InGaAs/InAlAs}$ lattice matched to $\mathrm{InP}$ substrate and $\mathrm{Si/SiGe}$ on $\mathrm{Si}$ substrate. Among them, the $\mathrm{InP}$ based HBTs ($\mathrm{InP/InGaAs/InP}$ or $\mathrm{InAlAs/InGaAs/InP}$) can have a cutoff frequency of **250GHz**.
  可用的技术包括上面这么多，全是化学式，不想翻译了
- The **[[课件/EE6604/ZQ/Heterojunction Electronic Devices/Heterojunction Electronic Devices#Emitter Region|Bandgap Discontinuity]]** $\Delta E_C$ between the emitter and base is **not desirable** since the carriers need to overcome a barrier, which makes the emitting efficiency and collector current suffer. The problems can be alleviated by improved structures such as the **graded-layer**.
  发射极和基极之间导带的不连续$\Delta E_C$并不理想，因为电子需要跨过一个势垒，这将导致发射极效率和集电极电流遭罪。这可以用渐变层等改进的结构解决。
- [[课件/EE6604/ZQ/Heterojunction Electronic Devices/Heterojunction Electronic Devices#Base Region|Graded-base]] and $i$ collector with a $p^+$ pulse-doped layer near the subcollector can also improve device performance.
  渐变层和子集电极带$p^+$脉冲掺杂层本征集电极都可以改善器件的性能。

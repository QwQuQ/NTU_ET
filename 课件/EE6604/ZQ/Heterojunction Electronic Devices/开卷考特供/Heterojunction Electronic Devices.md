# Fundamentals

- A heterojunction is defined as a junction (structure) formed by two different semiconductor materials.
  异质结的定义是由两种不同的半导体材料组成的结（结构）
- Such semiconductors are mostly alloy (compound) semiconductors
  这些半导体材料大部分都是合金半导体
- Examples:
	- $\mathrm{Si Ge_{1-x}}$ on $\mathrm{Si}$
	- $\mathrm{Al_x Ga_{1-x} As}$ on $\mathrm{GaAs}$
	- $\mathrm{Ga_x In_{1-x} As}$ on $\mathrm{Al_x Ga_{1-x} As}$
	- etc.

## Material Parameters of Alloy Semiconductors

- An **alloy semiconductor is a combination of two or more semiconductors**, elemental semiconductors ($\text{Si}$ with $\text{Ge}$) or semiconductor compound from the same group ($\text{GaAs}$ with $\text{InAs}$ or $\text{ZnS}$ with $\text{ZnSe}$).
  合金半导体是两种或更多半导体元素的组合（Si与Ge）或者同族元素的化合物（GaAs与InAs或者ZnS和ZnSe）
- An alloy is formed from a physical mixture of two or more compounds, while a compound is formed from a chemical reaction. $\text{GaAs}$ (or $\text{InAs}$) is a compound semiconductor.
  合金由两种或更多化合物组成，化合物由化学反应生成，GaAs就是一种化合物半导体
- $\mathrm{Ga_{1−x} In_x As}$ is an alloy compound consisting of $\mathrm{GaAs}$ and $\mathrm{InAs}$ with a mole ratio of $(1−x):x$.
  $Ga_{1-x}In_xAs$是一种以摩尔比例$(1−x):x$混合$GaAs$和$InAs$化合物的合金
- **Alloy semiconductors** could be binary ($\mathrm{SiGe}$, $\mathrm{GaAs}$, $\mathrm{InP}$), or ternary ($\mathrm{Al_x Ga_{1-x} As}$, $\mathrm{In_x Al_{1-x} As}$), or quaternary ($\mathrm{In_x Ga_{1-x} As_y P_{1-y}}$).
  合金半导体可以是二元的（$\mathrm{SiGe}$, $\mathrm{GaAs}$, $\mathrm{InP}$），或者三元的（$\mathrm{Al_x Ga_{1-x} As}$, $\mathrm{In_x Al_{1-x} As}$），或者四元的（$\mathrm{In_x Ga_{1-x} As_y P_{1-y}}$）
- The material parameters include energy bandgap, lattice constant, thermal conductivity, melting point, etc. The first two, **[[#Energy Bandgap|Bandgap]]** and **[[Lattice Constant]]** are the most important ones.
  材料的特性包括带隙、晶格常数、导热率、熔点等。带隙和晶格常数是最重要的两个。

#### Vegard's Law

- Usually, the parameters of the binary materials are known. The parameters of the ternaries and quaternaries can be derived using Vegard’s Law. (In 1921 by Lars Vegard, a Norwegian physicist)
  一般来说，二元材料的特性是已知的。三元和四元材料的特性可以用维加德定律得出

##### Ternary Compound

- For a **ternary compound** $A_xB_{1-x}C$ (where $A$ and $B$ are the same group elements (group III or group V elements), the parameter $P$, which may be **bandgap** $E_g$ or [[Lattice Constant]] ($LC$), can be expressed as
  对于一个三元化合物$A_xB_{1-x}C$，其中$A$和$B$是同族元素（第三族或第五族），参数$P$可以用来表示带隙$E_g$或者晶格常数（$LC$），它的表达式为$$P(A_xB_{1-x}C)=xP_{AC}+(1-x)P_{BC}$$ where $x$ is **mole fraction** or composition which can vary from 0 to 1.
  其中$x$叫摩尔分数，取值范围为0-1 ^648b21

##### Quaternary Compound

- For a **quaternary compound** $A_xB_{1-x}C_yD_{1-y}$ (where $A$ and $B$ are the same group of elements, and $C$ and $D$ are the same group of elements), the parameter $P$ can beobtained from the respective values of the four binaries. 
  对于一个四元化合物$A_xB_{1-x}C_yD_{1-y}$（其中$A$和$B$是同族元素，$C$和$D$是同族元素），参数$P$可以用四个二元化合物的参数得到$$\displaylines{P\left(A_xB_{1-x}C_yD_{1-y}\right)\\=xyP_{AC}+x(1-y)P_{AD}+(1-x)yP_{BC}+(1-x)(1-y)P_{BD}}$$

##### Ternary Alloys

- If the parameters of the ternary alloys $A_xB_{1-x}C$, $A_xB_{1-x}D$, $AC_yD_{1-y}$, and $BC_yD_{1-y}$ are available, then parameter P can be modified as
  如果三元化合物$A_xB_{1-x}C$、$A_xB_{1-x}D$、$AC_yD_{1-y}$、$BC_yD_{1-y}$的参数已知，参数P可以表示为$$\displaylines{P(A_xB_{1-x}C_yD_{1-y})\\=\frac{x(1-x)[(1-y)P_{ABD}+yP_{ABC}]}{x(1-x)+y(1-y)}+\frac{y(1-y)[xP_{ACD}+(1-x)P_{BCD}]}{x(1-x)+y(1-y)}}$$

### Lattice Constant

- Lattice constant follows [[Vegard’s Law]] well.
  晶格常数非常遵守维加德定律
- Example:
	- $\mathrm{LC (InAs): 6.0583} \mathrm{\overset{\circ}{A}}$
	- $\mathrm{LC (GaAs): 5.6533} \mathrm{\overset{\circ}{A}}$
	- $\mathrm{LC (In_{0.3} Ga_{0.7} As): 0.3 \times 6.0583 + 0.7\times 5.6533 = 5.7748 \overset{\circ}{A}}$, or $\mathrm{0.57748nm}$

![[Lattice Constant.png#pic_center|]]
晶格常数一般由6个参数组成：$a$、$b$、$c$、$\alpha$、$\beta$、$\gamma$
由于在半导体中一般为立方结构，所以可以只用一个参数表示晶胞的物理尺寸。

#### Lattice Constant Variation as a Function of Mole Fraction

![[Lattice Constant Variation as a Function of Mole Fraction.png#pic_center|]]

### Energy Bandgap

- The bandgaps of the [[Vegard’s Law#Ternary Compound|Ternary Compound]] and [[Vegard’s Law#Quaternary Compound|Quaternary Compound]] semiconductors only approximately follow Vegard’s Law.
  三元和四元化合物的带隙只大致符合维加德定律$$E_g(A_xB_{1-x}C)=xE_g(AC)+(1-x)E_g(BC)$$
- In most alloys, there is a **bowing effect** arising from the increasing disorder due to alloying of different elements. The energy bandgap of alloy semiconductors can bebetter described by the following expression:
  对于大部分合金来说，化合不同元素增加的无序性会导致一种弯曲效应。合金半导体的带隙使用下式能够更好地表示$$E_g(\mathrm{alloy})=a+bx+cx^2$$

![[Compositional Dependence of Energy Bandgap.png|Compositional Dependence of Energy Bandgap of the III-V Alloys at 300 K]]

## Lattice Match and Mismatch Heterostructures

- There are two kinds of heterostructures:
	- **Lattice-Matched Heterostructures**
		- The two materials have the same Lattice Constants, e.g. AlAs on GaAs.
		  两种材料有相同的晶格常数。
	- **Lattice-Mismatched Heterostructures**
		- The **lattice-mismatched heterostructures** can be further classified as **Strained Heterostructure** and **Unstrained Heterostructure**.

![[Lattice Match and Mismatch Heterostructures.png#pic_center|Lattice Match and Mismatch Heterostructures]]

### Strained Heterostructure


![[Pasted image 20241030011450.png#pic_center|Strained Heterostructure]]

- Assume
	- $a_s$ [[Lattice Constant]] of Si substrate
	  $a_s$为Si衬底的晶格常数
	- $a_f$ [[Lattice Constant]] of the SiGe bulk film
	  $a_f$为SiGe薄片的晶格常数
- If the epitaxially grown SiGe is **very thin**, the heterostructure will be **strained**.
  如果外延生长的SiGe非常薄，这个异质结就会被拉紧（应变）
- In this case, the normal cubic unit cell of the grown SiGe film $a_f\cdot a_f\cdot a_f$, will be distorted to a tetragonal cell $a_{f\parallel}\cdot a_{f\parallel}\cdot a_{f\perp}$. That is, $a_{f\parallel}=a_s$, $a_{f\perp}\neq a_{f\parallel}$ and $a_f\neq a_{f\perp}$.
  在这种情况下，SiGe外延薄片的正常立方晶胞（$a_f\cdot a_f\cdot a_f$）会变为长方体晶胞（$a_{f_s}\cdot a_{f_s}\cdot a_{f\perp}$），这意味着$a_{f\parallel}=a_s$，注意$a_f\neq a_{f\perp}$

- The strain parallel to the interface is
  平行于界面的应力为$$\epsilon_\parallel=\frac{a_{f\parallel}-a_f}{a_f}=\frac{a_s-a_f}{a_f}$$
- The strain perpendicular to the interface 
  垂直于界面的应力为$$\epsilon_\perp=\frac{a_{f\perp}-a_f}{a_f}$$
- The substrate-film lattice mismatch (or misfit) is defined as:
  衬底-薄片的错配度被定义为$$M=\frac{a_s-a_f}{a_f}$$$M$ is the same as the parallel strain.
  $M$与平行于界面的应力相同 ^5aff88

### Unstrained Heterostructure

- If the growing SiGe film is **thick** enough, the heterostructure will be **unstrained**.
  如果外延胜场的SiGe薄片足够厚，这个异质结就会变成非应变的
- In this case, the grown film and the substrate have their own bulk [[Lattice Constant]]s.
  在这种情况下，外延胜场的薄片和衬底有它们各自的晶格常数
- The two materials, SiGe film and Si substrate have cubic symmetry. That is, the cubic unit cell $a_f\cdot a_f\cdot a_f$ is for the film and $a_s\cdot a_s\cdot a_s$ is for the substrate.
  这两种材料，即SiGe薄膜和Si基底，具有立方对称性。也就是说，薄膜的立方晶胞为$a_f\cdot a_f\cdot a_f$，基底的立方晶胞为$a_s\cdot a_s\cdot a_s$
  
![[Pasted image 20241030012030.png#pic_center|Unstrained Heterostructure]]

- In this case, the atoms of the film and the substrate do **NOT** have a one-to-one correspondence at the interface.
  在这种情况下，薄膜和基底的原子在界面处**没有**一一对应关系
- This results in the formation of defects at the interface of the two materials, called **misfit dislocations**.
  这导致在两种材料的界面处形成缺陷，称为**错配位错**

### Critical Thickness

- There is a critical thickness $h_c$ below which the film grown is strained without misfit dislocation (*pseudomorphic growth*), and above which the film becomes unstrained or relaxed, associated with formation of misfit dislocations at the interface.
  在一个临界厚度$h_c$之下，生长的薄膜受到应变且没有错配位错（_伪同晶生长_）；而当超过该厚度时，薄膜变为无应变或松弛状态，并伴随在界面形成错配位错$$h_c=\frac{b}{8\pi(1+v)M}\left[ln\left(\frac{h_c}{b}\right)+1\right]$$
- where $b=\frac{a}{\sqrt{2}}$ for most (100) semiconductor systems (a is [[Lattice Constant]] of substrate), $v$ is [Poisson' ratio]([泊松系数_百度百科](https://baike.baidu.com/item/%E6%B3%8A%E6%9D%BE%E7%B3%BB%E6%95%B0/9914992?fr=ge_ala)) with an approximate value of 0.274, $M$ is the [[Strained Heterostructure#^5aff88|mismatch]].
  对于大多数(100)半导体系统，$b=\frac{a}{\sqrt{2}}$（其中$a$是基底的，$v$是[泊松比](https://baike.baidu.com/item/%E6%B3%8A%E6%9D%BE%E7%B3%BB%E6%95%B0/9914992?fr=ge_ala)，其近似值为0.274，$M$为错配度

![[Critical thickness vs. Mismatch for Si Substrate.png#pic_center|Critical thickness vs. Mismatch for Si Substrate]]
  
> ### Mismatch 错配度
> $$M=\frac{a_s-a_f}{a_f}$$
> ### Poisson's ratio 泊松系数
> 泊松系数指的是在固体力学中，材料的横向变形系数，即泊松比，称为泊松系数。


![[Critical thickness vs. Mismatch for Si Substrate.png#pic_center|Critical thickness vs. Mismatch for Si Substrate]]
- A greater mismatch corresponds to a smaller critical thickness
  失配越大，临界厚度越小
- A smaller mismatch corresponds to a greater critical thickness
  失配越小，临界厚度越大

## Bandgap Discontinuity

- Two materials have different energy bandgaps. There are possibly three types of band-edge lineups:
  两种材料具有不同的带隙。可能有三种类型的带边排列：
	- Straddling
	- Staggered
	- Broken Gap
- Each of these has unique and special band structure and device applications.
- 考虑这个的时候需要把[[Vacuum Level]]对准（不是费米能级）

### Straddling Bandgap

右边半导体的导带低于左边半导体的导带，而其价带高于左边半导体的价带。左边半导体的带隙大于右边半导体的带隙。
![[Straddling.png#pic_center|Straddling]]

### Staggered Bandgap

右边半导体的导带和价带都低于左边半导体的能带。在该交错间隙中，尽管右边半导体的带隙仍然部分地包含在左边半导体中，但其带隙不再局限于小于左边半导体。
![[Staggered.png#pic_center|Staggered]]

### Broken Gap

右边半导体的导带与左边半导体的价带重叠。由于这种重叠，在界面处没有禁带，并且右边半导体的带隙不再被左边半导体的带隙所包含。
![[Broken Gap.png#pic_center|Broken Gap]]

## The Band Diagram for Heterostructures

![[Energy band diagrams for nonuniform band structure and doping.png|Energy band diagrams for nonuniform band structure and doping. (a) before contact; (b) after contacted.]]

- Consider the energy band diagrams for two materials with different [[Electron Affinity]] $\mathrm{q}\chi$ , the energy gaps $E_g=E_c-E_v$ and the chemical potentials or [[Fermi Level|Fermi Energy]] $E_f$.
  考虑两个具有不同电子亲和能$\mathrm{q}\chi$、能量带隙$E_g=E_c-E_v$以及化学势或费米能级$E_f$的材料的能带图
- Note:
	- [[Vacuum Level]] must be continuous
	  真空能级必须连续
	- The band bending upward means an increase in electron energy, decrease in electron density
	  能带向上弯曲意味着电子能量增加，电子密度减少
	- The band bending downward means a decrease in electron energy, increase in electron density
	  能带向下弯曲意味着电子能量减少，电子密度增加

> ### Electron Affinity 电子亲和能
> 电子亲和能是导带最小值与真空能级之间的能量差。它表示电子从真空能级进入导带的难易程度，通常在讨论半导体的掺杂和表面态时非常关键。符号为$\chi$

>  ### Vacuum Level 真空能级
>  代表电子在材料外部静止时的能量，是所有其他能量的参考点。

> ### Fermi Level 费米能级
> 在费米-狄拉克分布中，费米能级可视为热力学平衡时，电子有50%概率占据的假想能级。
> 
> - 绝缘体中，$E_F$位于能隙上，与导带和价带相距甚远。
> - 金属、半金属中，$E_F$位于导带上。
> - 无杂质半导体或少量掺杂的半导体中，$E_F$虽位于能隙上，但与导带和价带较近。
> 
> - 在掺杂的半导体中，费米能级会产生偏移。
> 	- 对于N型半导体，费米能级为：$$E_F-E_i=kTln\left(\frac{N_d}{n_i}\right)$$
> 	- P型半导体的费米能级为：$$E_i-E_F=kTln\left(\frac{N_a}{n_i}\right)$$ $N_d$为施主浓度；$N_a$为受主浓度；$E_i$为本征费米能级

### Bandgap Offset

![[Bandgap Offset.png|Bandgap Offset]]

$$\displaylines{
\Delta E =& E_{g1}-E_{g2}=\Delta E_C+\Delta E_V \\
\Delta E_C =& E_{C1}-E_{C2} \\
\Delta E_V =& E_{V2}-E_{V1}
}$$
- The ratio $\Delta E_C/\Delta E_V$ varies with material systems and is not easy to be determined.
  $\Delta E_C/\Delta E_V$的比率随材料系统而变化且不易确定。
- The $\mathrm{GaAs/AlAs}$ and $\mathrm{GaAs/AlGaAs}$ systems have type I structure, and the ratio $\Delta E_C/\Delta E_V$ is about 60:40.
  $\mathrm{GaAs/AlAs}$和$\mathrm{GaAs/AlGaAs}$系统具有Ⅰ型结构，$\Delta E_C/\Delta E_V$的比率约为60:40。

- The band diagram of Metal/AlGaAs/GaAs Heterostructure under Thermal Equilibrium
![[Pasted image 20241030020138.png#pic_center|The band diagram of Metal/AlGaAs/GaAs Heterostructure]]

> ### Thermal Equilibrium 热平衡
> 在半导体中指材料中的载流子，产生数等于复合数。

# Heterojunction Bipolar Transistors (HBTs)

The bandgap of a Ternary or Auaternary Alloy semiconductor can be varied, by simply adjusting the composition $x$ or $y$.
三元合金或四元合金半导体的带隙可以通过简单地调整组成$x$或$y$来改变。

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
  HBT也有高速和高截止频率的电路工作特性

![[HBT_FIG3.png|A HBT with an n-AlGaAs emitter and a p-GaAs base transistor (a) Device structure, (b) Band diagram at thermal equilibrium]]

### Common Emitter Current Gain of HBTs

- From the definition, $$\beta_0\approx\frac{n_{B0}D_B L_E}{p_{E0}D_E W_{bn}}$$ and from [[PN Product#Law of Mass Action|Law of Mass Action]], $np=n_i^2$, the minority carrier concentration in the emitter $p_{E0}$, is
  发射极中的少数载流子浓度可以表示为（使用掺杂浓度代替多子浓度）：$$p_{E0}=\frac{n_o^2(\mathrm{emitter})}{N_E(\mathrm{emitter})}=\frac{N_CN_V exp(-\frac{E_{gE}}{kT})}{N_E}$$ where,
	- $N_C$: [[Effective Density of States]] in the conduction band
	  导带有效态密度
	- $N_V$: Effective Density of States in the valence band
	  价带有效态密度
	- $E_{gE}$ is the bandgap of the emitter
	  发射机的带隙
- The minority carrier concentration in the base $n_{B0}$ is
  基极的少数载流子浓度为：$$n_{B0}=\frac{n_i^2(\mathrm{base})}{N_B(\mathrm{base})}=\frac{N_C^\prime N_V^\prime exp(-\frac{E_{gB}}{kT})}{N_B}$$ where, 
	- $N_C^\prime$ and $N_V^\prime$: [[Effective Density of States]] in conduction band and valence band respectively
	  导带和价带的有效态密度
	- $E_{gB}$: bandgap of base
	  基极的带隙

> ### Law of Mass Action
> $$p_0n_0=n_i^2$$
> $E_g$为半导体的禁带宽度。
> $p_0$和$n_0$为两种**平衡载流子浓度**
> 由于电中性，在本征半导体中有$p_i=n_i$

> ### Equilibrium Carrier Concentration 平衡载流子浓度
> 在硅和其他半导体中，导带热平衡载流子浓度：$$n_0=N_c\times exp\left(-\frac{E_c-E_F}{kT}\right)$$
> 价带热平衡载流子浓度：$$p_0=N_v\times exp\left(-\frac{E_F-E_v}{kT}\right)$$
> - 符号：
> 	- $n_0$: 热平衡电子浓度
> 	- $p_0$: 热平衡空穴浓度
> 	- $N_c$: 导带有效态密度
> 	- $N_v$: 价带有效态密度
> 	- $E_F$: 费米能级
> 	- $k$: 玻尔兹曼常数
> 	- $T$: 开尔文温度

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
The common emitter current gain varies with the mole fraction of $\mathrm{Al}$.
共射电流增益随着Al的摩尔分数改变而改变

### $\mathrm{InGaAs/InP}$ and $\mathrm{InGaAs/InAlAs}$ HBTs

- The $\mathrm{InP}$ based $\mathrm{In_{0.53}Ga_{0.47}As}$ ($E_g\cong 0.75eV$) and $\mathrm{In_{0.52}Al_{0.48}As}$ ($E_g=1.4eV$) are lattice matched to $\mathrm{InP}$ ($E_g=1.35eV$)
- $\mathrm{InGaAs}$ has smallest $E_g$ and should be used as base
- The $\mathrm{InGaAs/InP}$ (emitter) structure has very low **Surface Recombination**. And electrons have higher Carrier Mobility in $\mathrm{InGaAs}$ than in $\mathrm{GaAs}$. Such HBTs have a cutoff frequency of **254GHz**.
- Collector can be any one as long as the requirement for breakdown voltage can be met.
  集电极可以是任意材料，只要击穿电压能够满足

![[HBT_FIG6.png#pic_center|InAlAs as the emitter]]

![[HBT_FIG13.png#pic_center|InP as the emitter]]

![[HBT_FIG7.png#pic_center|Current gain as a function of operating frequency for an InGaAs/InP HBT.]]

### $\mathrm{Si/Si_x Ge_{1-x}}$ HBTs

- The alloy $\mathrm{Si_x Ge_{1-x}}$ will be the base due to a smaller band gap.
- $\mathrm{Si/SiGe}$ system is attractive for HBT due to:
	- high speed capability
	- small trap density at $\mathrm{Si}$ surface which minimizes Surface Recombination current and ensures a high current gain even at low collector current
	- compatibility with standard $\mathrm{Si}$ technology

> ### Surface Recombination 表面复合
> 半导体的表面充满缺陷（悬空的键和环境中的杂质），这导致表面态和表面附近的能带弯曲。所以在未钝化的半导体表面，非辐射复合的速度更快。
> 关于表面复合的速度：$$\text{recombination\ rate}=S_eA\left(n-n_0\right)$$
> 上式中：
> - $S_e$表示表面复合速度$cm/s$
> - $A$表面的面积$cm^2$
> 所以符合速度的单位是$s^{-1}$

![[HBT_FIG8.png#pic_center|Device structure of an npn Si/SiGe/Si HBT]]
![[HBT_FIG9.png#pic_center|Collector and base current versus Vbe for a HBT and BJT]]
The $\mathrm{Si/SiGe}$ HBT has a higher current gain than homojunction $\mathrm{Si}$ BJT, but a lower cutoff frequency than $\mathrm{GaAs}$ and $\mathrm{InP}$-based HBTs because of the lower carrier mobility in $\mathrm{Si}$.

## The Ways to Further Improve HBTs’ Performance

### Emitter Region

The conduction band discontinuity $\Delta E_C$ between the emitter and base is not desirable, since it will make the electrons to transport by means of [[Thermionic Emission]] across a barrier or by tunneling through it.
导带的不连续性是不被希望的，因为它会导致电子在运输过程中以热激发的方式运输或者隧穿过势垒。

> ### Thermionic Emission
> 一种通过热激发发射载流子的方式。
> 
> 这个现象发生的原因是，提供给载流子的热能使它们能够克服束缚势能（在金属材料中，这束缚势能也被称为逸出功。通过热发射产生的载流子可能是电子或者离子。发射载流子之后原始区域会产生一个于被发射载流子总和大小相同、极性相反的载流子。产生电子的热发射被称为**热电子发射**。
> > ### Work Function 逸出功
> > 指要使一粒电子立即从固体内部移到固体外部，所必须提供的最小能量。半导体为费米能级到真空能级的能量。**注意与电子亲和能区分**

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

# Modulation-doped Field Effect Transistors (MODFETs)

- In a FET there is a gate-controlled channel through which current is allowed to flow.
  场效应管中有一个受到栅极控制的沟道，电流能够在其中流动
- The gate must be isolated from the channel current flow. Otherwise, an input signal current, while on its way to the output, would “leak” through the gate, leading to a poor gain for the FET.
  栅极必须与沟道电流隔离。否则，输入信号电流在到达输出时会“泄漏”到栅极，导致FET增益变差。

## Two types of conventional FETs

![[MODFET_FIG1.png#pic_center|MOSFET]]

1. Metal Oxide Semiconductor FETs (MOSFETs)
   金属氧化物场效应管
	- The gate isolation is provided by depositing an oxide between the gate and the active channel.
	  栅极使用在栅极与有源沟道之间的氧化物绝缘
	- **The n-channel is induced at the p-type $\mathrm{Si}$ surface due to strong inversion associated with band bending and controlled by gate voltage $V_{GS}$.**
	  在p型衬底表面的n型沟道在强反型的作用下会发生能带弯曲，受到$V_{GS}$的控制
	- The electron flow in the channel forms current $I_{DS}$ when $V_{GS}> V_T$ , and $V_{DS}>0$.
	  当$V_{GS}>V_T$、$V_{DS}>0$时，电子流过沟道形成$I_{DS}$

![[MODFET_FIG2.png#pic_center|MESFET]]

2. Metal Semiconductor FETs (MESFETs)
   金属半导体场效应管
	- In a Metal Semiconductor FET (**no oxide**), the metal gate forms a [[Schottky Barrier]] with the semiconductor.
	  在MESFET中（没有氧化物），金属栅极与半导体形成了肖特基势垒
	- **The n-channel is a part of the n-type Si, which is not covered by the depletion region of the [[Schottky Barrier]], and controlled by the reverse-biased Shottky contact.**
	  n型沟道是n型衬底的一部分，不与肖特基势垒的空间电荷区重合，受到反偏肖特基接触的控制。

> ### Schottky-Barrier 肖特基势垒
> #### 热平衡
> 在金属与半导体接触中，形成肖特基势垒的接触称为肖特基接触或者整流接触。一般都是金属与一个n型半导体接触。
> 
> 符号：
> - 金属的功函数$e\phi_m$
> - n型半导体的功函数$e\phi_s$
> - n型半导体的电子亲和能$\chi$
> ![[Pasted image 20241102020725.png]]
> 在n型半导体与金属发生接触时，由于真空能级必须连续，所以n型半导体的导带发生弯曲以匹配金属的功函数。同时二者作为一个热平衡的系统，费米能级必须相同，所以在远处n型半导体与金属的费米能级必须在同一能级上。
> 
> 所以就发生如图的能带弯曲，规定：
> - 势垒高度$\phi_{bn}=\phi_m-\chi /e$为金属中电子试图进入半导体时所遇到的势垒，这一势垒就是**肖特基势垒**
> - 内建势垒$V_D=\phi_{bn}-\phi_n$，其中$e\phi_n$为n型半导体中导带底与费米能级的能量差

## New FETs Developed Using Heterostructures

- Modulation-doped Field Effect Transistors (MODFETs)
- They are also called:
	- Heterostructure Insulated Gate FETs (HIGFETs)
	- High Electron Mobility Transistors (HEMTs)
	- Two-dimensional Electron Gas FETs (TEGFETs)

## Device Structures

![[MODFET_FIG3.png|A systematic of a GaAs/AlGaAs n-MODFET]]
1. Semi-Insulating GaAs Substrate.
   半绝缘GaAs
2. Undoped GaAs, 2-dimensional $e$ gas is formed on the surface of this layer.
   未掺杂的GaAs，这个区域会形成二维电子气
3. Undoped AlGaAs as a spacer which separates the electrons in undoped GaAs and the donor ions in doped AlGaAs.
   未掺杂的AlGaAs形成间隔层，将未掺杂GaAs层的电子和掺杂的AlGaAs层的施主离子隔离
4. Donor-doped AlGaAs.
   施主掺杂的AlGaAs
5. Metal gate which forms Schottky Barrier with the doped AlGaAs.
   金属栅极，与掺杂的AlGaAs形成肖特基势垒

The energy band profile shows band bending leading to a triangular quantum well at the $\mathrm{GaAs/AlGaAs}$ interface.
这个能带图展示了能带弯曲，导致了界面上有一个三角形的量子阱

![[MODFET_FIG4.png#pic_center|]]

## Modulation Doping

![[MODFET_FIG5.png#pic_center|]]
![[MODFET_FIG6.png#pic_center|]]

- The doped wide bandgap $n^+$ AlGaAs has donor ions and electrons.
  宽带隙的$n^+$ AlGaAs有施主离子和电子
- The electrons could transfer through the undoped AlGaAs spacer to the narrow bandgap undoped GaAs as it has lower energy states for electrons.
  电子穿过未掺杂的AlGaAs隔离层到窄带隙的GaAs，因为GaAs层的电子能级更小
- The positively charged donor ions and the negatively charged electrons are then spatially separated by the undoped AlGaAs spacer.
  正电荷施主离子和负电荷电子被未掺杂的AlGaAs层上在空间上分开
- The dipole effect produces band bending.
  偶极效应导致能带弯曲
- The energy states in undoped GaAs are quantized, $E_1$ is the ground level.
  未掺杂GaAs中能级是量子化的，$E_1$是基态

### Advantages of the Modulation Doping

- Because the electrons at the surface of the narrow gap GaAs are spatially separated from the positively charged dopant ions by the undoped AlGaAs spacer, these electrons are virtually free to move in the undoped GaAs channel and essentially remain free from impurity ion scattering. **Thus, they have high mobility**.
  由于在窄带隙GaAs表面的电子从空间上与带正电的杂质离子被未掺杂的AlGaAs隔离层隔离，这些电子在未掺杂的GaAs沟道中几乎可以自由移动，并且基本上不受杂质离子散射的影响。**因此，它们具有高迁移率**。
  ![[MODFET_FIG7.png#pic_center|2-dimensional property]]
- As the trapped electrons have 2-dimensional properties (moving in x-y plane), hence they are called two-dimensional electron gas. The sheet electron concentration is very high as they are limited to a very thin surface layer of the GaAs.
  由于被捕获的电子具有二维特性（在x-y平面内移动），因此它们被称为二维电子气。面电子浓度非常高，因为它们被限制在非常薄的GaAs的表面层。

![[MODFET_FIG8.png#pic_center|]]

- The two-dimensional electron gas has the highest [[Carrier Mobility]] at a **given temperature**.
  这个二位电子气在给定的温度下有最高的迁移率
- This is why such devices are also called **High Electron Mobility Transistors (HEMTs)**.
  这就是为啥这货叫HEMT

## Normally-off and normally-on Devices

- To control the drain-source current $I_D$ by means of a gate voltage $V_G$, the thickness of the wide bandgap layer between the gate metal and the 2DEG is critical.
  为了使用栅极电压$V_G$控制漏-源电流$I_D$，栅极金属和二位电子气之间宽带隙层的宽度非常关键
- By varying the thickness of the wide-bandgap layer, the MODFET can be made either a normally off (enhancement mode) or normally on (depletion mode) device.
  通过修改宽带隙层的厚度，MODFET可以制作成常开或者常闭器件

### Normally-off or Enhancement-mode MODFETs

- When the wide-bandgap layer is thin, the MODFET will be a normally-off device.
  当宽带隙层比较薄的时候，MODFET是一个常开器件。
  
![[Pasted image 20241102014640.png]]

- Energy band diagrams of a normally-off MODFET at
  常开MODFET的能带图，条件：
	- (a) [[Thermal Equilibrium]]
	  热平衡下
	- (b) The onset of threshold ($V_T>0$)
	  达到阈值电压
- $d_1$ and $d_0$ are the thicknesses of the doped and undoped regions of the wide bandgap semiconductor, respectively
  $d_1$和$d_0$分别是是掺杂和没掺杂的宽带隙层的厚度
- $\Delta E_C$ is the conduction bandgap offset
  $\Delta E_C$是导带带隙的偏移

- For small AlGaAs thickness, the gate Schottky Barrier can completely deplete the electrons in the AlGaAs as well as the 2DEG even at zero gate bias, thus leading to enhancement-mode type or normally off devices.
  AlGaAs厚度较小的情况下，即使没有栅极偏置，栅极的肖特基势垒也可以完全耗尽AlGaAs和二位电子气中的电子，从而获得了增强型或者常闭型器件。
  
  ![[MODFET_FIG9.png#pic_center|Depletion Width of Schottky Contact]]

- The depletion width of the Schottky contact $W$ is greater than $d_1+d_0$. No channel is formed at the narrow bandgap GaAs surface.
  肖特基接触的耗尽层宽度$W>d_1+d_0$，在窄带隙的GaAs表面未形成沟道
- A **positive gate** voltage (greater than the threshold voltage $V_T$) is required to turn the device on. When $V_G=V_T$ , the depletion width $W=d_1+d_0$
  大于阈值电压$V_T$的正栅极电压可以开启器件，当$V_G=V_T$时，$W=d_1+d_0$
  
![[Pasted image 20241102024935.png#pic_center|]]

The threshold voltage can be adjusted by control of AlGaAs thickness and doping.
阈值电压可以通过调整AlGaAs的厚度和掺杂实现$$V_T=\phi_{Bn}-\frac{\Delta E_C}{q}-V_p$$ Where
- $\phi_{Bn}$ is the barrier height
  势垒高度
- $V_p$ is a pinch-off voltage of the n-type AlGaAs
  n型AlGaAs的夹断电压$$V_p=\frac{q}{\epsilon_s}\int_0^d N_D(x)x\mathrm{d}x=\frac{qN_Dd_1^2}{2\epsilon_s}$$ Where
    - $\epsilon_s$ is the permittivity of the AlGaAs materials
      AlGaAs的介电常数
    -  $N_D$ is the doping concentration
      掺杂浓度

- When the gate voltage is larger than $V_T$, a charge sheet will be capacitively induced by the gate at the heterojunction interface.
  当栅极电压大于阈值时，受到栅极的影响，异质结的界面上将出现一个电容性的电荷层
    
![[Pasted image 20241102025701.png#pic_center|]]

The sheet carrier concentration (**number of the carriers per unit area**) is defined as
电荷层的载流子浓度被定义为：$$n_s(y)=\frac{C_g\left(V_G-V_T-V(y)\right)}{q}$$Where
- $y$ is zero at the source and $L$ at the drain
  $y$在源极为0，在漏极为$L$（沟道的长度）
- $V(y)$ is the voltage at position $y$ due to drain voltage
  沿着$y$方向的漏极电压
- $C_g$ is the deleption capacitance per unit area
  单位面积的耗尽电容$$C_g=\frac{\epsilon_s}{d_1+d_0+\Delta d}$$ Where
  - $\Delta d$ is a correction factor (some authors take $\Delta d$ as the thickness of channel or inversion layer)
    $\Delta d$是一个矫正系数（一些作者把这个定义为沟道或反型层的厚度）$$\Delta d=\frac{\epsilon_s\cdot a}{q}\approx8\mathrm{nm}$$

### Normally-on or Depletion-mode MODFETs

- When the wide bandgap layer is thick enough, the MODFETs will be Normally-on or Depletion-mode devices.
  当宽带隙层足够厚，MODFET会变成常闭器件
- For thicker AlGaAs layers, the depletion region of the [[Schottky Barrier]] does not deplete the electron gas at zero gate voltage ($W<d=d_1+d_0$). Such devices are Normally-on or Depletion-mode devices. (A channel exists at $V_G=0$). 
  对于更厚的AlGaAs层，在栅极电压为0的情况下，肖特基势垒并不会把二维电子气耗尽到0V（$W<d=d_1+d_0$）。这种器件被称为常闭或者耗尽型器件（$V_G=0$时存在沟道）
  
![[Pasted image 20241102030333.png#pic_center|]]

- A negative gate voltage is required to deplete the electron gas and pinch the device off. ($V_T<0$)
  负的栅极电压用来耗尽二维电子气以将设备关闭

![[Pasted image 20241102030724.png#pic_center]]

### Example

Consider an AlGaAs/GaAs heterojunction with n-AlGaAs doped to $2\times 10^{18} cm^{-3}$ and a thickness of $40\mathrm{nm}$. Assume the undoped spacer layer is $3\mathrm{nm}$ and the Schottky barrier height is $0.85e\mathrm{V}$ and $\Delta E_C/q=0.23\mathrm{V}$. The dielectric constant of the AlGaAs is 12.3. Calculate the two-dimensional electron gas concentration for such heterojunction at $V_G=0$.

#### Solution

- 首先判断器件类型（常开还是常闭），判断依据是阈值电压$V_T$ $$V_T=\phi_{Bn}-\frac{\Delta E_C}{q}-V_p$$
	- 肖特基势垒$q\phi_{Bn}=0.85e\mathrm{V}\implies \phi_{Bn}=0.85V$
	- $\frac{\Delta E_C}{q}=0.23V$
	- pinch-off voltage: $$V_p=\frac{qN_Dd_1^2}{2\epsilon_s}$$
		- 掺杂浓度$N_D=2\times 10^{18}\mathrm{cm}^{-3}$
		- AlGaAs厚度$d_1=40\mathrm{nm}=40\times10^{-7}\mathrm{cm}$
		- 相对介电常数$\epsilon_s=12.3$，所以介电常数为$\epsilon_s\cdot\epsilon_0$
		$$\implies V_p=2.35\mathrm{V}$$
	所以阈值电压$V_T$：$$V_T=0.85-0.23-2.35=-1.73\mathrm{V}$$
- 二维电子气浓度$n_s$： $$n_s=\frac{\epsilon_s\epsilon_0}{d_1+d_0+\Delta d}\frac{V_G-V_T}{q}=2.30\times 10^{12}cm^{-2}$$

## Current-Voltage Characteristics

- The current voltage characteristics of a MODFET can be obtained in the way similar to the MOSFET. The current at any point along the channel is
  MODFET的电压电流特性可以用和MOSFET类似的方式获得，沟道任意一点的电流为：$$I_D=Wq\mu_n n_s\xi_y=W\mu_nC_g\left[V_G-V_T-V(y)\right]\frac{\mathrm{d}V(y)}{\mathrm{d}y}$$ Where:
	- $W$ is the channel width
	  沟道宽度
	- $\xi_y$ is longitudinal electric field
	  沿着沟道的电场强度
- Since the current is constant along the channel, integrating the equation from source to drain ($y=0$ to $y=L$) gives
  因为这个电流在沟道中是一个常数，对这个等式从源到漏积分得到：$$I_D=\frac{W}{L}\mu_n C_g\left[(V_G-V_T)V_D-\frac{V_D^2}{2}\right]$$
	- When $V_D\ll(V_G-V_T)$, it is in linear region and
	  当$V_D\ll(V_G-V_T)$，它在线性区$$I_D=\frac{W}{L}\mu_nC_g\left[(V_G-V_T)V_D\right]$$
	- At large drain voltage, the charge sheet $n_s(y)$ at the drain is reduced to 0. So $V_{Dsat}=V_G-V_T$ and the saturation current is
	  漏极电压比较大的时候，漏极的电荷层$n_s(y)$被减小到0，$V_{Dsat}=V_G-V_T$。所以饱和电流为：
	  $$I_{Dsat}=\frac{W\mu_nC_g}{2L}\left(V_G-V_T\right)^2=\frac{W\mu_n\epsilon_s}{2L(d_1+d_0+\Delta d)}(V_G-V_T)^2$$
	- For high-speed operations, the longitudinal field along the channel is sufficiently high to cause carrier drift velocity saturation ($v_{ds}$). The current (maximum) in the velocity-saturation region is
	  对于高速应用，沿着沟道的电场非常大，导致载流子达到速度饱和。此时的最大电流为：$$I_{Dmax}=qn_sv_{ds}W=C_g(V_G-V_T)v_{ds}W$$

## Important Parameters

### Channel Conductance

$$g_d=\frac{\partial I_D}{\partial V_D}\Bigg|_{V_G}$$
The electron draft velocity is $v_d=\mu\xi$
电子漂移速度是：
where:
- $\mu$ is [[Carrier Mobility]]
  载流子迁移率
- $\xi$ is electric field and $\xi=\frac{V_D}{L}$ , $L$ is channel length
  电场强度

$$\displaylines{I_D=q n_s v_d W=Wq n_s\mu_n\xi_y=\frac{W}{L}V_D q n_s \mu_n\\\implies g_d=\frac{W}{L}q n_s \mu_n}$$

With $n_s=10^{12}\mathrm{cm^{-2}}$ in a channel $1\mu\mathrm{m}$ long and $10\mu\mathrm{m}$ wide, and $\mu_n$ of electrons in the GaAs channel is $7000cm^2\cdot V^{-1}s^{-1}$, then $g_d=1.12\times 10^{-2}\mathrm{S(siemens)}$, which is **10 times higher** than in a Si MOSFET.
比硅MOSFET高10倍

### Transconductance

$$g_m=\frac{\partial I_D}{\partial V_G}\Bigg|_{V_D}\implies g_m(\mathrm{sat})=\frac{\partial}{\partial V_G}C_g v_{ds}W(V_G-V_T)=C_g v_{ds}W$$
- 其中$v_{ds}$是速度饱和的速度

### Transit Time

$$t_r=\frac{L}{v_{ds}}$$
For $L=1\mu\mathrm{m}$ and $v_{ds}=2\times 10^7\mathrm{cm\cdot s^{-1}}$, the transit time is $5\mathrm{ps}$.

MODFETs have very small transit time that enables them to be used as high-speed devices.
MODFET有非常小的传输时间，适用于高速设备

## Cutoff Frequency

- The speed of a MODFET is measured by the cutoff frequency
  MODFET的速度使用截止频率衡量$$f_T=\frac{g_m}{2\pi(\mathrm{total\ capacitance})}=\frac{W v_{ds} C_g}{2\pi (WL C_g+C_p)}$$ where:
	- $C_p$ is the parasitic capacitance
	  寄生电容
- To improve $f_T$, we should consider a semiconductor with large $v_{ds}$, a gate structure with an ultra short gate length, and a device configuration with minimum parasitic capacitance.
  为了提高截止频率，我们要考虑一个有大速度饱和速度的器件，栅极极其短的栅极结构，设备结构上的寄生电容尽可能小

### Cutoff Frequency Versus Channel or Gate Length for Five Kinds of Field-Effect Transistors

![[Pasted image 20241102041324.png]]
- The best pseudomorphic SiGe MODFETs have a $f_T$ comparable to the GaAs MODFET. SiGe MODFETs are attractive because they can be processed with silicon fabrication facilities.
  最好的伪SiGe MODFET的截止频率与GaAs MODFET相当，SiGe MODFET相当有吸引力，因为它可以用硅的制造设备制造。
- The $\mathrm{Al_{0.48}In_{0.52}As-Ga_{0.47}In_{0.53}As}$ MODFET formed on a InP substrate has higher $f_T$, mainly due to the high electron mobility and velocities in the $\mathrm{Ga_{0.47}In_{0.53}As}$. The $f_T$ at a gate length of $50\mathrm{nm}$ can be as high as $600\mathrm{GHz}$.

## Summary

- The MODFET is a device which enhanced high-frequency performance. This device structure is similar to that of a MESFET except there is a heterojunction under the gate. A two-dimensional electron gas, i.e., a conductive channel, is formed at the heterojunction interface, and electrons with high mobility and high average drift velocity can be transported from the source through the channel to the drain.
  MODFET是一种增强高频性能的器件。其结构类似于MESFET，但在栅极下方有异质结。在异质结界面形成了二维电子气，即导电沟道，具有高迁移率和高平均漂移速度的电子可以从源极通过沟道到达漏极。
- The output characteristics of all field-effect transistors (FETs) are similar. They all have a linear region at low-drain biases. As the bias increases, the output current eventually saturates, and at a sufficiently high voltage, avalanche breakdown occurs at the drain. Depending on whether it requires a positive- or negative-threshold voltage, FET can be either normally off (enhancement mode) or normally on (depletion mode).
  所有场效应晶体管（FET）的输出特性都相似。它们在低漏极偏置时都有一个线性区域。随着偏置的增加，输出电流最终会饱和，并且在足够高的电压下，会在漏极处发生雪崩击穿。根据是否需要正阈值电压或负阈值电压，FET可以是常断型（增强模式）或常通型（耗尽模式）。
- The cutoff frequency $f_T$ is a figure of merit for the high-frequency performance of a FET. The conventional GaAs MODFET and the pseudomorphic SiGe MODFET have a $f_T$ about 30% higher than that of the GaAs MESFET. The GaInAs MODFET has the highest $f_T$ and it has a projected $f_T$ of $600\mathrm{GHz}$ at a gate length of $50\mathrm{nm}$.
  截止频率$f_T$是评估 FET 高频性能的指标。传统的 GaAs MODFET 和伪SiGe MODFET 的$f_T$大约比GaAs MESFET高30%.GaInAs MODFET具有最高的$f_T$,在$50\mathrm{nm}$栅极长度下的$f_T$为$600\mathrm{GHz}$。
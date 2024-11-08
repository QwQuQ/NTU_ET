---
aliases:
  - Modulation-doped Field Effect Transistors
tags:
  - semi_conductor
  - heterostructure
---

# Fundamentals

- [[Heterojunction]]

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

- [[Vegard’s Law]]

### Lattice Constant

- [[Lattice Constant]]

#### Lattice Constant Variation as a Function of [[Vegard’s Law#^648b21|Mole Fraction]]

![[Lattice Constant Variation as a Function of Mole Fraction.png#pic_center|]]

### Energy Bandgap

- The bandgaps of the [[Vegard’s Law#Ternary Compound|Ternary Compound]] and [[Vegard’s Law#Quaternary Compound|Quaternary Compound]] semiconductors only approximately follow Vegard’s Law.
  三元和四元化合物的带隙只大致符合维加德定律$$E_g(A_xB_{1-x}C)=xE_g(AC)+(1-x)E_g(BC)$$
- In most alloys, there is a **bowing effect** arising from the increasing disorder due to alloying of different elements. The energy bandgap of alloy semiconductors can bebetter described by the following expression:
  对于大部分合金来说，化合不同元素增加的无序性会导致一种弯曲效应。合金半导体的带隙使用下式能够更好地表示$$E_g(\mathrm{alloy})=a+bx+cx^2$$

![[Compositional Dependence of Energy Bandgap.png]]
- Compositional Dependence of Energy Bandgap of the III-V Alloys at 300 K

## Lattice Match and Mismatch Heterostructures

- There are two kinds of heterostructures:
	- **[[Lattice-Matched Heterostructures]]**
	- **[[Lattice-Mismatched Heterostructures]]**
		- The **lattice-mismatched heterostructures** can be further classified as **[[Strained Heterostructure]]** and **[[Unstrained Heterostructure]]**.

![[Lattice Match and Mismatch Heterostructures.png#pic_center|Lattice Match and Mismatch Heterostructures]]

### Critical Thickness

- [[Critical Thickness]]

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

- The band diagram of Metal/AlGaAs/GaAs [[Heterojunction|Heterostructure]] under [[Thermal Equilibrium]]
![[Pasted image 20241030020138.png#pic_center|The band diagram of Metal/AlGaAs/GaAs Heterostructure]]
# Heterojunction Bipolar Transistors (HBTs)

[[HBT]]

# Modulation-doped Field Effect Transistors (MODFETs)

[[MODFET]]

- **[[Wet Etching]]**
	- Wet etching is a process whereby materials are removed by liquid etchants
	  Wet etching是一种通过液体蚀刻剂去除材料的过程
	- Wet etching is fast, cheap and simple, but harder to control. Hence, it is not popular in nanofabrication
	  Wet etching快速、廉价、简单，但更难控制。因此，它在纳米制造中并不流行
- **[[Dry Etching]]**
	- Dry etch uses gas phase etchants in plasma
	  Dry etching使用等离子体中的气相蚀刻剂
	- In comparison, dry etching is slower, requires sophisticated equipment, but easier to control
	  相比之下，Dry etching速度较慢，需要复杂的设备，但更容易控制
	- It works for many dielectric materials and some metals (Al, Ti, Cr, Ta, W, etc.)

# Isotropic Etching

![[Pasted image 20250221192954.png#pic_33center|Isotropic Etching]]
![[Pasted image 20250221194002.png#pic_33center|Isotropic Etching]]
- Attacks the materials equally in all directions and result in the undercut of the mask. Thus, the obtained feature size will be larger than the mask design.
  在所有方向上均匀地蚀刻材料，导致掩模的底切。因此，所获得的特征尺寸将大于掩模设计。

# Anisotropic Etching

![[Pasted image 20250221193049.png#pic_33center|Anisotropic Etching]]
![[Pasted image 20250221194120.png#pic_33center|Anisotropic Etching]]
- Etching rate is faster in the vertical direction than in the horizontal direction, forming straight edge features.
  蚀刻速率在垂直方向上比在水平方向上快，形成竖直边缘特征。

# Figures of Merit: Degree of Anisotropy

> **Figures of Merit**：品质因素

- In most etching techniques, there is a mixture of isotropic and anisotropic features

![[Pasted image 20250221194801.png#pic_75center|Increasing Degree of Anisotropic]]

- **Degree of Anisotropy**
  各向异性程度：$$A=1-\frac{R_L}{R_V}$$其中：
	- $R_L$是侧面（lateral）的蚀刻比例
	- $R_V$是垂直（vertical）的蚀刻比例

# Etch Parameters

## Etch Rate

![[Pasted image 20250221202220.png#pic_50center|]]
$$\text{Etch Rate}=\frac{\Delta T}{t}$$
- $\Delta T$为厚度（Thickness）的改变量
- $t$为经过的时间

## Etching Undercut and Overetch

![[Pasted image 20250221202721.png#pic_75center|]]

## Selectivity

![[Pasted image 20250221202647.png#pic_50center|]]

- 定义为：$$\text{Selectivity (S)}=\frac{E_f}{E_r}$$其中：
	- $E_f$为高蚀刻率
	- $E_r$为低蚀刻率

- Selectivity is the ratio of the etch rates between the different materials, especially the material that needs to be etched as compared to the material that we do not want to remove.
  选择性是不同材料之间的蚀刻速率之比，特别是需要蚀刻的材料与我们不想去除的材料相比。
- The smaller the feature size of the process, the higher selectivity is needed
  特征尺寸越小的工艺，所需的选择性越高

- 影响因素：
	- Impurity type and/or concentration
	  杂质浓度或者类型
		- 使用$\mathrm{KOH}$蚀刻：
			- 掺杂浓度$10^{14}-10^{18}cm^{-3}$的硅，速度为$0.94\mathrm{\mu m/cm^{-3}}$
			- 掺杂浓度$10^{18}-10^{20}cm^{-3}$的硅，速度为$0.02\mathrm{\mu m/cm^{-3}}$
		- Highly doped $n/p$ layer inserted intentionally as etch stop.
		  可以使用高掺杂层作为蚀刻的阻隔
	- Material composition
	  材料
		- In $\mathrm{GaAs/AlGaAs}$ compound, the etch selectivity in removing $\mathrm{GaAs}$ is 95.
		- 可以用于$\mathrm{GaAs}$工艺
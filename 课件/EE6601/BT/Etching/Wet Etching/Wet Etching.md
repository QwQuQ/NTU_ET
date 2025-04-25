# Process

![[Pasted image 20250221195409.png#pic_75center|]]

1. Etchants diffuse to the reacting surface
   蚀刻剂扩散到反应表面
2. Chemical reaction at the surface
3. Removal of the products from the surface through diffusion
   通过扩散从表面去除产物

- Desirable to have a large, uniformed and well-controlled etch rate
  期望具有大的、均匀的和良好控制的蚀刻速率
- The overall etch rate is determined by the slowest sub-process, which is called as **rate-limiting step**
  整体蚀刻速率由最慢的子工艺决定，称为**rate-limiting step**
- The possible rate-limiting step in wet etching can either be step (1), (2) or (3)

- 加速的方法：
	- Etchant Agitation
	  搅拌蚀刻剂，针对第1和3步有效果
	- Etching in Elevated Temperature
	  高温下蚀刻，针对第2步有效果

# Silicon Etching Process

- Silicon can be etched away by a mixture of $\mathrm{HNO_3}$ and $\mathrm{HF}$, coupled with a diluent (water or acetic acid)
  硅可以用$\mathrm{HF}$和$\mathrm{HNO_3}$的混合物蚀刻，与稀释剂（水或者醋酸）混合
	- $\mathrm{HNO_3}$ oxidises $\mathrm{Si}$ to form $\mathrm{SiO_2}$
	  $\mathrm{HNO_3}$将硅氧化为氧化为二氧化硅
	- $\mathrm{HF}$ will etch away the formed $\mathrm{SiO_2}$
	  $\mathrm{HF}$蚀刻走形成的二氧化硅

![[Pasted image 20250221201111.png#pic_75center|]]

- Local anodisation, oxidising the silicon (holes are required to start this process). Oxidised by $\mathrm{HNO_3}$, “holes” are supplied by $\mathrm{HNO_3}$.
  局部阳极氧化，将硅氧化（需要空穴来开始这个过程）。使用硝酸氧化，空穴由硝酸提供$$\mathrm{Si}+2h^+\rightarrow\mathrm{Si^{2+}}$$
- 硝酸提供空穴的过程为：$$\mathrm{HNO_2}+\mathrm{HNO_3}\rightarrow 2\mathrm{NO_2}+2h^++\mathrm{H_2O}$$
- 水水解$$\mathrm{H_2O}\rightarrow \mathrm{OH}^-+\mathrm{H}^+$$
- Combines with $\mathrm{OH}^-$ to form the hydroxide
  与氢氧基形成氢氧化物$$\mathrm{Si^{2+}}+2\mathrm{OH}^-\rightarrow\mathrm{Si(OH)_2}$$
- Subsequently liberates hydrogen to form $\mathrm{SiO_2}$
  随后放出氢气形成二氧化硅$$\mathrm{Si(OH)_2}\rightarrow \mathrm{SiO_2}+\mathrm{H_2}$$
- Hydrofluoric acid ($\mathrm{HF}$) is used to dissolve $\mathrm{SiO_2}$ $$\mathrm{SiO_2}+6\mathrm{HF}\rightarrow \mathrm{H_2SiF_6}+\mathrm{H_2O}$$
- 总的反应为：$$\mathrm{Si}+\mathrm{HNO_3}+\mathrm{6HF}\rightarrow \mathrm{H_2SiF_6}+\mathrm{H_2O}+\mathrm{H_2}$$
- The by-products after etching are typically gaseous or water soluble for ease of removal.
  蚀刻后的副产物通常是气态或水溶性的，以便于去除

- 这种蚀刻的速度会随着时间变慢，原因是：
	- In regular $\mathrm{Si}$ etching, $\mathrm{SiO_2}$ etching reaction consumes $\mathrm{HF}$ and cause the reaction rate of $\mathrm{SiO_2}$ etching to decrease
	  在常规硅（$\mathrm{Si}$）蚀刻中，二氧化硅（$\mathrm{SiO_2}$）蚀刻反应会消耗氢氟酸（$\mathrm{HF}$），导致二氧化硅（$\mathrm{SiO_2}$）蚀刻反应速率下降
	- Buffered $\mathrm{HF}$ ($\mathrm{NH_4F}$) is used to provide consistent etch rate by maintain $\mathrm{HF}$ concentration.
	  缓冲氢氟酸（$\mathrm{NH_4F}$）用于通过维持氢氟酸（$\mathrm{HF}$）浓度来提供一致的蚀刻速率$$\mathrm{NH4F} \rightarrow \mathrm{NH_3} \uparrow + \mathrm{HF}$$

# Iso-Etch Curve

![[Pasted image 20250221203516.png#pic_75center|Iso-Etch Curve]]

- The silicon etch rate is determined under different concentrations of $\mathrm{HNO_3}$, $\mathrm{HF}$ and diluent

- The contour lines indicate the etch rate of $\mathrm{Si}$ at specific concentrations.
  等高线表示在特定浓度下硅的蚀刻速率
- The numbers in the bracket indicate the $\mathrm{Si}$ etch rates in $\mathrm{\mu m/min}$.
  括号中的数字表示硅的蚀刻速率，单位为微米/分钟（$\mathrm{\mu m/min}$）
- The solid lines indicate the etch rates when acetic acid diluent is used.
  实线表示使用乙酸稀释剂时的蚀刻速率
- The dash lines indicate the etch rates when water diluent is used
  虚线表示使用水稀释剂时的蚀刻速率

- How to determine the $\mathrm{Si}$ etch rate using Iso-etch curve? For example, if a mixture of 10% $\mathrm{HF}$, 70% $\mathrm{HNO_3}$, and 20% water diluent is used as $\mathrm{Si}$ etchant:
	- Draw a line of such from 10% $\mathrm{HF}$ axis
	- Draw a line of such from 70% $\mathrm{HNO_3}$ axis
	- Draw a line of such from 20% diluent axis
	- Intersection point of these three lines falls at 11.5 µm/min curve of the dash line (water diluent). Therefore, the $\mathrm{Si}$ etch rate is $11.5\mathrm{\mu m/min}$
---
- 在前文的例子中，如果用醋酸替代水作为溶剂，蚀刻速率将会上升到$33\mathrm{\mu m/min}$
- Acetic acid ($\mathrm{CH_3COOH}$) is frequently substituted for water as the diluent.
  醋酸经常替代水作为溶剂
- It has lower dielectric constant than water
  它比水的介电常数更低
- Produce less dissociation of the $\mathrm{HNO_3}$ and yields a higher oxidation power for the etching process.
  减少硝酸（$\mathrm{HNO_3}$）的解离，并为蚀刻过程提供更高的氧化能力
---
![[Pasted image 20250221204447.png#pic_75center|]]
区域1与区域2的分界点：硝酸30%、氢氟酸30%、水40%
- 区域1: High HF concentrations, low HNO3 concentration, insufficient HNO3 to oxidise the Si for HF to etch.
	- Reaction limited by $\mathrm{HNO_3}$
	- The $\mathrm{HNO_3}$ concentration controls the etch rate
	- Etch rate is limited by oxidation, less oxide is formed on $\mathrm{Si}$
- 区域2: High $\mathrm{HNO_3}$ concentrations, low  concentration, insufficient HF to etch away the silicon oxide formed by $\mathrm{HNO_3}$.
	- Reaction limited by $\mathrm{HF}$
	- Ability of $\mathrm{HF}$ to remove the SiO2 controls the etch rate
	- Etch rate limited by reduction, more oxide is formed on $\mathrm{Si}$

# Orientation Dependent Etching

![[Pasted image 20250222014935.png#pic_75center|(110) (111) (110)]]
![[Pasted image 20250222015522.png#pic_25inline|(110)]]![[Pasted image 20250222015533.png#pic_25inline|(111)]]
- Different $\mathrm{Si}$ atomic planes have different etch rates in $\mathrm{KOH}$ etchant
  不同的硅（$\mathrm{Si}$）原子平面在氢氧化钾（$\mathrm{KOH}$）蚀刻剂中的蚀刻速率不同
	- $0.6\mathrm{\mu m/min}\to (100) \text{plane}$
	- $0.1\mathrm{\mu m/min}\to (110) \text{plane}$
	- $0.006\mathrm{\mu m/min}\to (111) \text{plane}$
- $\mathrm{Si(111)}$ plane is closely packed $\rightarrow$ Slowest etching
- (111) plane of $\mathrm{Si}$ oxidises faster than other planes, thus the surface is covered faster with oxide, which blocks further dissolution
  硅（$\mathrm{Si}$）的（111）平面比其他平面氧化得更快，因此其表面更快地被氧化物覆盖，从而阻止了进一步的溶解

- Through an oxide mask, $\mathrm{KOH}$ etching of $\mathrm{Si}$ forms (111) planes at the side walls
  经过氧化掩模，硅（$\mathrm{Si}$）被氢氧化钾（$\mathrm{KOH}$）蚀刻，在侧壁形成（111）平面
![[Pasted image 20250222015821.png#pic_center|V-groove]]
![[Pasted image 20250222015848.png#pic_33center|V-groove]]
- Since (111) has slow etch rate, it forms a self-stopping V-groove
- (111) plane makes an angle of $54.7\defree$ with (100) naturally, the width ($W$) of the defined image approximately determines the depth ($d$) following the relation:$$d\approx\frac{W}{2}\mathrm{tan}54.7\degree\approx0.7W$$
- 
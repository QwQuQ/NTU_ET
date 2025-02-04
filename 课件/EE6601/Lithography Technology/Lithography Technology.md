# UV Light Spectrum and Resolution

## 大概是前置知识

### 波长和频率的关系（高中物理）

$$\lambda=\frac{c}{f}$$
- $v$是光速$3\times 10^8 \mathrm{m\cdot s^{-1}}$，$f$的单位是赫兹，$\lambda$的单位是$\mathrm{m}$

### 光谱

- Most resists react with visible UV
  大多数光刻胶与可见紫外光发生反应。

- Common UV wavelengths used in optical lithography
	- DUV: Deep Ultraviolet ($\lambda=248\mathrm{nm}$)
	- VUV: Vacuum Ultraviolet
	- EUV: Extreme Ultraviolet

### Resolution

- 更高的Resolution总是更好的
- Resolution是在晶圆上区分两个紧邻特征的能力
- Feature Size是形成了的图案的实际尺寸
- 最小的Feature Size是Critical Dimension (CD)
- Resolution is important for critical dimension

（怎么感觉都是废话）

### Light Intensity

- Higher intensity = Shorter exposure time
- Lower intensity = Longer exposure time
- KrF laser is preferred over Hg lamp DUV. 看图，KrF激光的Light Intensity在DUV上对比水银灯更强

（又都是废话）

## Excimer Laser （准分子激光）

- Deep UV by excimer lasers
  图上说准分子激光能够覆盖EUV到DUV
- $Kr+NF_3+(\text{energy})\rightarrow KrF+(\text{photon emission})$
- KrF（氟化氪）: $\lambda=248\mathrm{nm}$, (CD: $\leq 0.25 \mathrm{\mu m}$)
- ArF（氟化氩）: $\lambda=193\mathrm{nm}$, (CD: $\leq 0.18\mathrm{\mu m}$)
- $F_2$ （氟）： $\lambda=157\mathrm{nm}$, (CD: $\leq0.15\mathrm{\mu m}$)

## Mercury Arc Lamp（汞弧灯；水银灯！）

- 汞蒸气灯：玻璃灯中有汞的等离子体
- 产生许多不同波长的光
- 光强比较有限
- 图上说能够覆盖DUV、Mid-UV和紫光

- "g" line: $\lambda=436\mathrm{nm}$ (used to mid 1980s); Critical Dimension Resolution (µm): $0.5\mathrm{\mu m}$
- "h" line: $\lambda=405\mathrm{nm}$; Critical Dimension Resolution (µm): $0.4\mathrm{\mu m}$
- "i" line: $\lambda=365\mathrm{nm}$ (early 1990s, $>0.3\mathrm{\mu m}$); Critical Dimension Resolution (µm): $0.35\mathrm{\mu m}$
- DUV(Deep Ultraviolet): ($\lambda=248\mathrm{nm}$); Critical Dimension Resolution (µm): $0.25\mathrm{\mu m}$

# Negative and Positive Lithography

## Resist

- Resist是一种对光敏感的聚合物

- Positive Resist
  被光照射后可以溶解
- Negative Resist
  没被光照的可以溶解

- 主要功能
	- 保护下方的薄片（ie. $\mathrm{SiO_2}$、$\mathrm{Al}$、polysilicon、$\mathrm{Si_3 N_4}$）免受蚀刻
	- 描出金属接触和薄膜沉积的窗口
	- 在选择性离子注入中防止离子进入穿透进下方的硅
	- 利用剥离工艺在衬底上形成金属图案

### Lift-off Process

![[Pasted image 20250203144059.png#pic_center|Lift-off Process]]

1. 基板被涂覆上光刻胶，然后通过带有所需图案的掩模使光刻胶曝光
2. 显影光刻胶以在基板上获得所需图案
3. 金属薄膜被沉积到带有光刻胶图案的基板上
4. 沉积在光刻胶上的金属被移除（通常使用丙酮），金属图案将被保留在衬底上

- 在Microstructuring Technology中，Lift-off Process是一种在衬底上使用可被牺牲的材料创建目标材料图案的技术
- Lift-off Process是对更传统的减材技术如蚀刻而言的补充。

## Negative Lithography

![[Pasted image 20250203145109.png|Negative Lithography]]

## Positive Lithography

![[Pasted image 20250203145046.png|Positive Lithography]]

# Eight Basic Steps of the Lithography Process

## 0. Vapour Prime Pre-Step – Dehydration Bake

- 去除晶圆表面的水分子
- 保证晶圆表面干净又干燥

- 清洁样品非常重要，以确保其没有灰尘、污垢或残留的光刻胶。脱水烘烤将确保样品上的任何 H₂O 都被蒸发掉。对于那些容易氧化的样品（例如硅）这一步尤为重要。氧化物随后会与空气中的水蒸气结合。当光刻胶涂覆到样品上时，光刻胶会附着在 H₂O 上而非晶圆表面。

![[Pasted image 20250203152435.png#pic_center|在晶圆表面存在的水会由于表面污染和水分层的存在，导致光刻胶粘附不良和光刻胶脱落]]

## 1. Vapour Prime – Cleaning and Dehydration Bake

- 光刻的第一步
- 在这一步骤中经常集成Wafer Dehydration Bake
- 使用HMDS对晶圆进行处理
- 促进光刻胶和晶圆良好粘接

![[Pasted image 20250203161449.png#pic_center|由于表面污染和水分层的存在，导致光刻胶粘附不良和光刻胶脱落]]

### HMDS处理中的变化：

- HMDS将硅的表面由亲水性变为疏水性以让光刻胶良好粘接
- $\text{Si-dioxide}+\mathrm{H_2O}+\text{HMDS}\rightarrow \text{Hexamethyldisiloxane}+\text{Ammonia}$
![[Pasted image 20250203170107.png#pic_center|]]
- 脱水烘烤这些氧化样品之后，用HMDS底漆进行旋涂非常重要。HMDS底漆将与氧化物基团结合以隔绝水分
- $\mathrm{Si(CH_3)_3}$基团与光刻胶兼容，能够在样品和光刻胶之间建立粘附力

### Typical Process Sequence

- Dehydration bake (200°C to 250°C)
- Vapour priming
- Priming Techniques
	- Puddle spray dispense and spin

![[Pasted image 20250203161539.png|HMDS (Liquid) Dispense and Spin]]

### Process Summary

![[Pasted image 20250203162108.png#pic_center|Enclosed Chamber with Exhaust]]

- Dehydration bake in an enclosed chamber with exhaust
  在封闭带有排气的腔室中脱水烘烤
- Hexamethyldisilazane (HMDS) prime
  使用HMDS预处理
- 排气
- Clean and dry wafer surface (hydrophobic)
  清洁并干燥晶圆表面（变成疏水性了）
- Temperature ~ 200°C to 250°C
- Time ~ 60 seconds

## 2. Spin Coat

![[Pasted image 20250203171709.png#pic_center|]]

### Process Summary

- The wafer is held onto the vacuum chuck
  晶圆被固定在真空吸盘上
- Dispense $\sim 5\mathrm{ml}$ of the resist at static or slow spread speed of $\omega_1 \sim 500\mathrm{rpm}$
  在静止或者500rpm的低转速下加入5ml光刻胶
- Ramp up to $\omega_2 \sim 3000 \text{ to } 5000 \mathrm{rpm}$
  加速到$\omega_2 \sim 3000 \text{ to } 5000 \mathrm{rpm}$
- Quality measures:
	- Time
	- Speed
	- Thickness
	- Uniformity
	- Particles and Defects
- 
  

## 3. Soft Bake

## 4. Alignment and Exposure

## 5. Post-Exposure Bake



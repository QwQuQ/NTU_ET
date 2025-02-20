# Chemistry of Resist

|                                Positive Resist                                |                                Negative Resist                                 |
| :---------------------------------------------------------------------------: | :----------------------------------------------------------------------------: |
|                 Exposed region becomes more soluble<br>曝光区域溶解                 |                 Exposed region becomes less soluble<br>曝光区域不溶解                 |
| Exposed areas are removed and unexposed areas remain after resist development | Exposed areas remains and unexposed areas are removed after resist development |
|        Patterns formed on the wafer are the same as those of the mask         |         Patterns formed on the wafer are opposite as those of the mask         |

## Components of Resist

- **Solvent**:
	- Gives resist its flow characteristics
	  给予光刻胶流动特性
	- Keeps resist in liquid state
	- Allows spin coating of the resist
	- Solvent content determines viscosity and hence, the **thickness**
- **Resin**:
	- Mix of polymers used as binder; gives resist its mechanical and chemical properties
	  用于作为粘合剂的聚合物混合物，赋予光刻胶其机械和化学特性
	- Not opaque at $\lambda$
	  在特定的波长下透明
	- Give resist mechanical and chemical properties (reaction to developer, etc.)
	  赋予光刻胶机械和化学特性（对显影剂的反应等）
- **Sensitisers**:
	- Photosensitive component of the resist material
	  光刻胶的光敏组分
	- Photo active compound/group (PAC/PAG) at $\lambda$
	  $\lambda$下的光敏组分或光敏基团
- **Additives**:
	- Chemicals that control specific aspects of resist material
	  控制光刻胶材料特定方面
	- Capability for further process: Etch resistivity/implant blocking capability

|                                                      Positive Resist                                                       |               Negative Resist               |
| :------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------: |
|                                                 **Resin** (Novolac resin)                                                  | **Resin** (Cyclised synthetic rubber resin) |
|                                **Sensitiser / dissolution inhibitor** (PAC = Diazoquinones)                                |     **Sensitiser** (PAC = Bisarylzide)      |
| **Solvent** (Propylene Glycol Methyl Ether Acetate (PGMEA), N-Methyl Pyrrolidine <br>(NMP), N-butyl acetate, xylene, etc.) |       **Solvent** (Aromatic solvent)        |
|                                     **Developer**: Hydroxides (TMAH, KOH, NaOH, etc.)                                      |      **Developer** (Organic solvents)       |
- Positive and negative resist have different types of developer due to different photochemical reactions.

## Chemistry of Positive and Negative Resist

### Positive Resist
![[Pasted image 20250218175333.png#pic_center|]]
![[Pasted image 20250218175020.png#pic_75center|DQN]]

- Diazoquinone（重氮萘醌）受光照射后会产生一个Carboxylic Acid Group（羧基），这使得它能够溶于Base Solution（碱性溶液）

#### Photochemical Reaction in Positive Resist

![[Pasted image 20250219033440.png#pic_25inline|老师给的Diazoquinone化学式]]![[Pasted image 20250219033629.png#pic_25inline|Diazoquinone在wiki上的化学式]]
- Photo Active Compound(PAC)受到光照射后，不稳定的化合物通过Wolff重排反应形成烯酮。**老师的化学式与wiki给的并不一样，我不知道谁对谁错，将就着看吧**

![[Pasted image 20250219024852.png#pic_25inline|老师给的图]]![[Pasted image 20250219032040.png#pic_25inline|我自己推的图，可能有错]]
- 碳原子从苯环上脱离使化合物稳定，氧原子与碳原子形成共价键，此时形成Ketene（烯酮）。**根据wiki的前后关系我推出来了一张图，这张图上有烯酮标志性的两个碳碳双键，并且由于Wolff重排形成了5元环**

![[Pasted image 20250219022042.png#pic_25inline|老师给的图]]![[Pasted image 20250219033718.png#pic_25inline|wiki给的图]]
- 烯酮的化学性质很活泼。与水反应形成羧基（其中一个碳碳双键断开成为碳碳单键，并连接上氢氧基和氢原子），能够溶于碱性显影液（氢氧化钾）。**老师的图和wiki的图又开始不一样了，感觉老师的多了一个碳原子，wiki是比较正常的五元环**

### Negative Resist

- Exposed Region: Formed polymer cross-linking
  曝光区域：形成聚合物交联
- Unexposed Region: Soluble in **Organic Solvent(Organic Developer)**
  未曝光区域：能够溶于有机溶剂（有机显影液）

# Chemically Amplified (CA) DUV Resist

![[Pasted image 20250219040123.png#pic_75center|Absorbance vs Wavelength]]

- Conventional DNQ resist has large absorption problem below 365 nm wavelength and not suitable for DUV technology.
  传统的二氮萘醌 (DNQ) 抗蚀剂在波长低于 365 纳米时存在较大的吸收问题，不适用于深紫外 (DUV) 技术。
- Conventional resists cannot be used in deep UV lithography processes because these resists have high absorption and require high dose to be exposed in deep UV. This raises the concern of damage to stepper lens, lower exposure speed and reduced throughput.
  传统的抗蚀剂不能用于深紫外光刻工艺，因为这些抗蚀剂在深紫外光下具有高吸收率，需要高剂量才能曝光。这引发了对步进镜头损坏、曝光速度降低和产量减少的担忧。
- 人话：在短波长下，光刻胶不怎么能够对光作出反应，它们仅仅吸收光然后发热。

## Components

| Conponent       | Typical Chemicals                                                                                                                                       | Purpose                                                                                                                                                                       | Remarks                                                                                                                                                                                             |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Solvent**     | Propylene Glycol Methyl Ether Acetate (PGMEA)                                                                                                           | gives resist its flow characteristics<br>赋予光刻胶流动特性                                                                                                                            | Compatible to other components<br>与其他组分兼容                                                                                                                                                           |
| **Resin**       | - tertiary-butoxycarbonyl parahydroxystyrene (tBOC-PHS) (248nm) <br>- phenolic copolymer <br>- cyclic olefin / maleic anhydride (COMA) polymers (193nm) | tertiary-butoxycarbonyl (tBOC) dissolution inhibitor protection group for 248CAresist; gives resist mechanical and chemical properties<br>tBOC是248CA光刻胶的溶解抑制保护基团；赋予光刻胶机械和化学性能 | Resin is a phenolic copolymer with a protecting group that makes it insoluble in developer. Transparent to 193nm DUV Etch resistance to plasma<br>树脂是一种含有保护基团的苯酚共聚物，不溶解于显影剂。对193nm深紫外光透明，具有等离子刻蚀抗性。 |
| **Sensitizers** | triphenylsulfonium salt                                                                                                                                 | Photo-Acid-Generator, PAG photosensitive component of the resist material<br>光致酸生成剂，PAG是光刻胶的光敏组分                                                                              | PAG acts as $\mathrm{H}^+$ catalyst for the de-protection of dissolution inhibitor of resin<br>PAG作为$\mathrm{H}^+$催化剂，用于使树脂的溶解抑制剂停止保护                                                               |
| **Additives**   | Low MW additives to increase contrast, Surfactants, adhesion promoter, dyes                                                                             | chemicals that control specific aspects of resist material<br>控制光刻胶材料特定方面的化学品                                                                                                 | dyes can also be added into the photoresist composition to reduce scattered light from the reflection in the resist/substrate interface.<br>染料也可以添加到光刻胶成分中，以减少在抗蚀剂/基板界面反射的散射光                       |

## Chemical reaction of CA DUV resists

![[Pasted image 20250219140926.png#pic_33center|可以发现留下的线宽会比光刻的宽度小]]

- 在曝光之前，PHS的酚羟基被tBOC基团保护。树脂的主要成分在显影液如四甲基氢氧化铵 (TMAH) 溶液中不溶
- 三苯基磺酰盐作为光致酸生成剂，并在曝光期间生成酸。**主要的两个步骤**：
	- 光致酸产生剂在光子的作用下产生酸
	- 在[[Post-Exposure Bake|PEB（在Lithography章节中讲过这一步是针对Deep UV Resist的）]]温度下，酸导致tBOC-PHS的溶解保护基团tBOC脱落，并产生一个新的酸分子（链式反应，化学放大）
		- 酸会扩散到没有曝光的区域
		- 当PEB终止时，链式反应也随之终止
		- 光刻胶的基础组分会中和酸
- 最终，曝光区域生成酚羟基，并可以在碱性显影液中溶解。

![[Pasted image 20250219142748.png#pic_75center|完整的反应图？我觉得只放这张图就够了（]]	  

# Metrics of Resist

- Adhesion 粘合力
- Photo activity 
- **Resolution**
	- How fine a line the resist can reproduce from an aerial image
	  光刻胶能够从空间像（aerial image）中形成多细的线条
	- Resolution of resist is determined by:
		- Contrast, thickness, and proximity effects
		  **邻近效应（Proximity Effects）** 由于光散射、衍射和反射等因素导致的图案失真现象
		- Swelling and contraction after development
		  显影后的膨胀和收缩
- **Contrast**
	- Ability of resist to distinguish between transparent and opaque regions of the mask
	  光刻胶区分掩膜透明和不透明区域的能力
		- Measured by exposing the resist of given thickness to varying radiation dose and measuring dissolution rate
		  通过将特定厚度的光刻胶暴露在辐射中，通过溶解度来测量
	- Higher ability to distinguish → Higher contrast → Sharper edge
	  更高的区分能力→更高的对比度→更锐利的边缘
- **Viscosity** 黏稠度

## Contrast Curve

- The contrast curve of the resist presents the fraction of remaining resist as a function of exposure dose $\mathrm{mJ}/\mathrm{cm}^2$
  对比度曲线表示残留光刻胶的比例与曝光剂量的函数关系
- 与功率的关系：$$\mathrm{mJ}/\mathrm{cm}^2=\mathrm{mW}/\mathrm{cm}^2\times\text{sec}$$

![[Pasted image 20250219163228.png#pic_33inline|Positive Resist]]![[Pasted image 20250219163250.png#pic_33inline|Negative Resist]]
- 明显地，Negative Resist的灵敏度高于Positive Resist

## Contrast of a Resist

![[Pasted image 20250219164007.png#pic_33inline|Low Resist Contrast]]![[Pasted image 20250219164128.png#pic_33inline|High Resist Contrast]]
- **Low Resist Contrast**
	- Sloped Walls 
	- Swelling 膨胀
	- Poor contrast
- **High Resist Contrast**
	- Sharp edges
	- No Swelling
	- Good contrast

- 对比度$\gamma$的定义是：$$\gamma=\left[\mathrm{log}_{10}\frac{D_{100}}{D_{0}}\right]^{-1}$$上式中：
	- $D_{100}$是使光刻胶无残留的最低光照剂量
	- $D_{0}$是使光刻胶发生变化的最低光照剂量
- 典型值，在同样的显影条件下：
	- $-\gamma_{\text{p}}=2.2$
	- $\gamma_{\text{n}}=1.5$
	- DNQ g-line/i-line resist: $\gamma\approx 2-3$
	- CA DUV resist: $\gamma\approx5-10$
- Resists with higher contrast result in better resolution because of more vertical resist profile
  高对比度的光刻胶由于具有更垂直的光刻胶轮廓，因此能够实现更好的分辨率

## Sensitivity and Contrast for Resists

- 灵敏度：$D_{100}$, $D_{f}$
- Large sensitivity for CA DUV resists compared with conventional DQN resist: $20-40 \mathrm{mJ}/ \mathrm{cm}^{2}$ compared to $100 \mathrm{mJ}/ \mathrm{cm}^{2}$ typical for DNQs
  CA DUV光刻胶比DQN光刻胶灵敏度更高
- Post-exposure bake very critical in DUV resist technology (chemical reaction occurs)
  [[Post-Exposure Bake|PEB]]很重要（废话，前面提过了）
	
## Resist Viscosity

- Solvent 溶剂：
	- Keeps photoresist in liquid state
	  使光刻胶保持在液体状态
	- Allows spin coating of the photoresist
	- Solvent content determines resist viscosity and hence, the **thickness**
	  溶剂影响黏稠度，进而影响厚度
- 厚度公式：$$I_R\approx\left[\frac{\text{viscosity}\times\text{solid content}(\%)}{\sqrt{\text{spin speed}}}\right]$$可以看出转速越高，厚度越小

# Advantages and Disadvantages of Positive and Negative Resist

## Negative Resist

### Advantage

- Well established
  大家都在用
- Shorter exposure time as compared to positive resist, higher throughput

### Disadvantage

![[Pasted image 20250219171517.png#pic_75center|Developed Negative Resist]]
- Dashed Lines Indicate Mask Pattern: Solvent-Induced Swelling
  能够看到溶剂导致的膨胀
- Solvent-Induced Swelling: 
	- Broadening of linewidth during development phase
	  显影阶段导致线宽加大
	- Not suited to $\text{features} < 2\mathrm{\mu m}$

## Positive Resist

### Advantage

- Does not suffer from swelling
- Better resolution
- Thick resist available (for etching)

### Disadvantage

- Requires much larger energy and longer exposure time: Lower throughput

# Critical Resist Modulation Transfer Function (CMTF)

$$\text{CMTF}=\frac{D_{100}-D_{0}}{D_{100}+D_{0}}=\frac{10^{1/\gamma}-1}{10^{1/\gamma}+1}$$
![[Pasted image 20250219173117.png#pic_33center|Ideal Resist: Vertical Resist Profile]]
- 极端值思想：如果$D_{100}=D_{0}=D_{\text{cr}}$那么此时$\gamma\implies \infty$, $\text{CMTF}=0$
	- 上式中：$D_{\text{cr}}$是critical exposure dose，任何受到辐射值大于$D_{\text{cr}}$的部分都将溶解，而小于的部分将保留
- 实际的值：
	- DNQ g-line/i-line resist: $\gamma \approx 2-3$, $\text{CMTF}\approx 0.4$
	- DUV CA resist: $\gamma\approx 5-10$, $\text{CMTF}\approx 0.1-0.2$

- 回忆光刻中出现的[[Modulation Transfer Function|MTF]]，为了让光刻胶显现正确的特征，需要满足：$$\text{MTF}_{\text{exposure system}}>\text{CMTF}_{\text{resist}}$$
	- 如果$\text{MTF}=1$，那么CMTF就可以是任意值
	- 如果$\text{CMTF}=0$，那么MTF就可以是任意值

# Standing Wave Effect in Resist

场波的大手伸到哪里，哪里的同学就泛滥成灾

![[Pasted image 20250220170452.png#pic_50center|能够看到界面处的半波损失]]

![[Pasted image 20250220170739.png#pic_center|Standing wave effect causes modulation of the developed photoresist edges. 驻波会让显影后的光刻胶边缘出现调制的样子]]

- Photoresist Reflective Notching Due to Light Reflections from non-planarized surface
  由于非平面化表面的光反射导致光刻胶反射缺口
- Constructive and destructive interference between incident and reflected light results in a periodic intensity distribution across the resist thickness.
  相长干涉和相消干涉在入射波和反射波之间发生，并厚度方向上产生周期性的强度变化
- With change in exposure (light intensity) comes change in resist dissolution rate, leading to zigzag resist profile after development.
  随着曝光（光强度）的变化，光刻胶的溶解度也改变，从而导致了显影后出现锯齿状的轮廓

![[Pasted image 20250221032123.png#pic_50center|Swing Curve]]

- The standing wave interference effect will also result in the variation in linewidth with changing photoresist thickness and such phenomenon is sometimes called the **Swing Curve**.
  驻波干涉效应还会导致随光刻胶厚度变化而引起的线宽变化，这种现象有时被称为**Swing Curve**
- **Preferred resist thickness**: an extreme point of the swing curve to reduce line-width variation

- Reflected waves from wafer surface in particular those reflective layers such as metals causes reflective notching and standing wave effect
  从晶圆表面，特别是那些金属等反射层反射回来的波会引起反射缺口和驻波效应
- Standing wave effect is a serious problem for fine line lithography when exposing on reflective surfaces
  在反射表面光刻高质量的线时，驻波效应是一个严重的问题

- 驻波的强度影响因素：
	- Resist thickness
	- Resist absorbance
	- Light incident angle
	- The substrate film:
		- reflectivity
		- refractive
		- index
- 驻波的周期：$$\text{period}=\frac{\lambda}{2n}$$其中$n$为光刻胶的折射率

## Reduction of Standing Wave Effect

### Dyeing the photoresist

![[Pasted image 20250221034636.png#pic_33inline|]]![[Pasted image 20250221034650.png#pic_33inline|]]![[Pasted image 20250221034704.png#pic_33inline|]]
- Increased absorbance of S1813J2 dyed version photoresist on exposure
---
- Dyeing the photoresist to increase absorption on exposure and reduce reflected waves intensity
  将光刻胶染色以增加曝光时的吸收率，并减少反射波的强度。

- The exposure modulation can be partially compensated using dyed version of the photoresist by increasing the absorbance of the exposed photoresist and hence reducing the reflected UV light intensity from the reflective substrate.
  曝光调制一定程度上可以通过使用染色的光刻胶来补偿，通过增加曝光光刻胶的吸收率，从而减少反射性基板反射的紫外光强度。

- Problem with Dyed Photoresist: Excessive Resist Absorption
	- The light intensity at the bottom of the resist is considerably less than that received at the top
	- To achieve straight-wall images, the resist absorption <20 %: new resist materials for DUV 248nm and 193nm
	  为了实现直壁图像，光刻胶的吸收率应低于20%. 需要针对用于DUV（深紫外线）248纳米和193纳米波长的新光刻胶材料。
	  > 在光刻过程中，直壁图像是指光刻图形的侧壁垂直度很高，这对于高精度的微细图形制备非常重要。光刻胶的吸收率决定了其对光的吸收程度。如果吸收率过高，会导致曝光过程中产生更多的热效应和散射效应，从而影响图形的分辨率和边缘直线度。因此，为了获得高质量的直壁图像，光刻胶的吸收率需要控制在20%以下，特别是在使用248纳米和193纳米深紫外线光源的新光刻胶材料中。这样可以减少光刻胶对光的过多吸收，提高曝光过程中图形的保真度和直线度。

## PEB

![[Pasted image 20250221035300.png#pic_25inline|Exposure to UV light]]![[Pasted image 20250221035325.png#pic_25inline|Striations in resist]]![[Pasted image 20250221035338.png#pic_25inline|PEB causes PAC diffusion]]![[Pasted image 20250221035357.png#pic_25inline|Result of PEB]]
![[Pasted image 20250221035452.png#pic_75center|SEM photographs of resist image of 0.35 µm pattern in 0.98 µm thick i-line resist developed with (right) and without PEB (left)]]
- [[Post-Exposure Bake|PEB]] also helps by smoothing out the zigzag due to resist thermal reflow

## ARC

- Anti-reflective coating (ARC) to reduce reflection wave intensity
  抗反射涂层（ARC）用于减少反射波的强度
---
![[Pasted image 20250221035848.png#pic_75center|The use of anti-reflective coatings can help prevent interference by reducing the reflected wave intensity]]
![[Pasted image 20250221040524.png#pic_75center|SEM photographs showing that ARC process improves linewidth narrowing (right with BARC) at a step on a topographic substrate. Linewidth is 0.25µm]]
- Bottom ARC (BARC) prior to resist spinning
  在旋涂光刻胶之前使用底部抗反射涂层（BARC）
---
![[Pasted image 20250221040440.png#pic_75center|]]
![[Pasted image 20250221040418.png#pic_75center|]]

- Phase-Shift Cancellation of Light
  通过设计抗反射涂层的折射率和厚度，使从底部反射回来的光和从表面反射的光产生相干干涉，从而抵消彼此的影响，进一步减少反射
---
![[Pasted image 20250221040632.png#pic_75center|]]
- Top ARC (TARC) after resist spinning
  在旋涂光刻胶之后使用顶部抗反射涂层（TARC）
# Chemistry of Resist

|                                                      Positive Resist                                                       |                                Negative Resist                                 |
| :------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------: |
|                                            Exposed region becomes more soluble                                             |                      Exposed region becomes less soluble                       |
|                       Exposed areas are removed and unexposed areas remain after resist development                        | Exposed areas remains and unexposed areas are removed after resist development |
|                               Patterns formed on the wafer are the same as those of the mask                               |         Patterns formed on the wafer are opposite as those of the mask         |

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



# Metrics of Resist

# Advantages and Disadvantages of Positive and Negative Resist

# Critical Resist Modulation Transfer Function (CMTF)

# Standing Wave Effect in Resist
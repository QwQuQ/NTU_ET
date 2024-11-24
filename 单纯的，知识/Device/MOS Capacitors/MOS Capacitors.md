---
aliases:
  - MOS电容
  - MOSC
tags:
  - device
---
## p-MOSC（对应nMOS中的p衬底）的四种情况

### Flatband

没有外接电压，$E_{F,\text{metal}}=E_{F,\text{bulk}}$

### Accumulation

![[Pasted image 20241121003113.png#pic_center|Accumulation]]

栅极电压小于0，$E_{F,\text{metal}}>E_{F,\text{bulk}}$。空穴在氧化物界面累积，栅极下面有空穴，氧化物内有电场。

### Depletion

![[Pasted image 20241121003133.png#pic_center|Depletion]]

栅极电压大于0，$E_{F,\text{metal}}<E_{F,\text{bulk}}$，金属中的电子能量相比衬底降低。衬底的能带向价带弯曲，栅极的空穴浓度下降，电子浓度增加。硅衬底的表面多数载流子（空穴）减少，形成厚度为$W_D$的耗尽层。

### Inversion

![[Pasted image 20241121003149.png#pic_center|Inversion]]

- 栅极的正电压足够高时，栅极附近的硅衬底的本征费米能级低于费米能级（费米能级更加靠近导带，变成n型半导体了，所以叫反型层）。
- 由于电子在p型衬底中是少子，所以需要通过**热激发（价带电子被激发到导带）**来形成反型层。
- 根据[[Boltzmann Distribution|玻尔兹曼分布]]，电子浓度和$E_F$与$E_i$的差成指数关系

- 弱反型：本征费米能级和费米能级相同
- 强反型：栅极附近的电子浓度等于p衬底的空穴浓度
	- 强反型下硅中的负电荷包括：
		- 表面反型层的电子（可以动）
		- 掺杂的负电荷（不能动）
	- 由于**electrostatic screening effect**，反型层的最大厚度为$W_{D,\text{max}}$

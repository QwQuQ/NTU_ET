	这好像很多都是概念，不知道怎么考，以PPT原文为准

# 电势，电容与电荷

高中物理的知识，应该都看得懂
$$Q=CV$$
$$I=\frac{\mathrm{d}Q}{\mathrm{d}t}=C\frac{\mathrm{d}V}{\mathrm{d}t}$$

# ESD耦合

## Direct discharge to an electronic component

直接摸元件
![[Pasted image 20241125160320.png#pic_center|]]

## Direct discharge to an electronic equipment housing

用手摸电器的外壳，老印的图很魔性。
![[Pasted image 20241125153547.png#pic_center|]]
## Indirect discharge

- 适用于具有非金属外壳或者屏蔽不良且未直接接触ESD放电的设备
![[Pasted image 20241125153830.png#pic_75center|还是很魔性的图]]
# Magnetic Field Coupling from ESD current

- 直导线产生的磁场：$$H=\frac{I}{2\pi d}\mathrm{A/m}$$
  上式中：
	  - $d$是空间中一点到直导线的距离
	  - $I$是流过直导线的电流
  - 磁感应强度：$$B=\mu_0\mu_rH=\frac{\mu_0\mu_rI}{2\pi d}$$
    上式中：
	- $\mu_0$是真空磁导率，$\mu_r$是介质的相对磁导率，空气中相对磁导率是1
- 感应到的电压：$$V=\frac{\mathrm{d}\phi}{\mathrm{d}t}=\frac{\mathrm{d}}{\mathrm{d}t}\left(BA\right)$$
  上式中：
	  - $B$是磁感应强度，$A$是被磁感线穿过的面积，共同构成磁通量$\phi$

![[Pasted image 20241126004910.png#pic_center|]]
一般在这个图中，电流的上升沿可以用直线来拟合，$$\frac{\mathrm{d}I}{\mathrm{d}t}=\frac{0.8I_0}{\tau_r}$$

# ESD Testing

## 怎么测试的

- 使用ESD Test Gun
- 标准：IEC 61000-4-2

## ESD Generation

![[Pasted image 20241125161003.png#pic_75center|]]

## Test Methods

- Contact discharge – The charged electrode of the test generator is kept in contact with the EUT or coupling plane and the discharge is actuated by the discharge switch within the generator.
  接触放电：测试发生器的带电电极保持与被测设备（EUT）或耦合平面接触，并通过发生器内的放电开关激活放电。
	- This typically applied to EUT with metallic casing or directly discharged to connector/component pins.
	  这通常适用于带有金属外壳的被测设备（EUT），或直接放电到连接器/组件引脚。
- Air discharge – The charged electrode of the test generator is moved towards the EUT until it touches the EUT.
  空气放电：测试发生器的带电电极向EUT移动，直到接触到EUT。
	- This typically applied to EUT with insulating casing/surfaces.
	  这通常适用于具有绝缘外壳/表面的被测设备（EUT）。

# ESD Protection

## ESD protection while handling electronics

- use of Anti-static Bags
  使用防静电袋
- ANSI/ESD S541-2003 : Packaging materials for ESD sensitive items
- ESD protective bags are typically made of conductive or dissipative materials.
  ESD防护袋通常由导电或耗散性材料制成。
- ESD Controlled Room
  控制ESD的房间
	- Flooring
		- Conductive Vinyl tile
		  导电乙烯瓷砖
		- “Computer grade” carpet
		  “电脑级”地毯（？？？
		- Conductive rubber
		  导电橡胶
	- Ionizer that produces clouds of “+” and “-” ions in the air to neutralize static accumulation
	  给空气充满正负离子（增强导电性）
	- Humidifier
	  加湿器（增强导电性）
  - Static safe workbench
	  - Table ESD mat
	  - Floor ESD mat
	  - ESD grounding strip
	  - Ionizer
	  - Humidity monitor
  - Static safe chair
	  - ESD safe fabric
	  - Low charging material or metal for casters

## Chassis design - Metallic enclosure

- Ensure good grounding for the chassis
- Minimize number and size of openings
	- use multiple small holes for ventilation
	- ensure opening dimension is much smaller than the wavelength of the highest susceptible frequency
	- use thick casing to increase attenuation
	- use honeycomb/wire mess for large opening
- Ensure shielding continuity
	- use conductive gaskets/finger stocks at joints of lid/door
	- ensure screw spacing is less than 1/4 wavelength of highest susceptible frequency
	- use shielded window for open screen
（这块是不是在Chamber那里也讲过）

## Chassis design - Non-metallic enclosure

- Acting on plastic wall thickness and separation distance to nearest conductive part inside, will increase the withstanding voltage against ESD arcing.
  考虑塑料壁厚和与内部最近导电部分的间距，增加对ESD电弧的耐受电压。

## Cables, power lines design

- Long external cables poses much greater ESD problem to electronics. Besides direct contact, he long cable act as antenna and can pick up ESD radiation, convert nto induced voltage and currents
- Most vulnerable types are flat cables terminating into plastic connector.
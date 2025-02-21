---
aliases: 
tags:
  - lithography
  - lithography_printing
---

# Step-and-Repeat Aligner (Stepper)

![[345678.png#pic_75center|Step-and-Repeat Projection Aligner]]

# Projection Printing

![[1t6437851415.png#pic_75center|Projection Printing]]

- **Reticle**: May contain the pattern of one or more die.
- **Projection Lens**: Reduces the size of reticle field to be printed onto the wafer surface
- **Single Field Exposure**: Includes focus, align, expose, step, and repeat process
- Wafer stage controls the position of the wafer in $\mathrm{X}$, $\mathrm{Y}$, $\mathrm{Z}$, and $\mathrm{\theta}$

### Numerical Aperture

![[Pasted image 20250211004807.png#pic_75center|Projection Printing]]

- The numerical aperture (NA) of an optical system is a measure of the ability to collect light, which is a measure of the light gathering power.
- 从PPT上的图可以看出，$NA$越大，衍射效应对于光学系统的影响越小，光学系统的分辨率越高
- Numerical Aperture, (NA) can be defined as: $$NA=n\mathrm{sin}\theta$$其中：
	- $n$为系统所浸没的介质的折射率，如果是空气的话$n=1$
	- $\theta$为物镜的接受角的一半
- 当$n=1$的时候，$NA$可以被定义为：$$NA=\mathrm{sin}\theta\approx\mathrm{tan}\theta=\frac{d/2}{f}=\frac{d}{2f}$$注意：
	- 当$\theta < 12\degree$时$\mathrm{tan}\theta\approx\mathrm{sin}\theta$
	- 所以投影物镜的数值孔径也是孔径和焦距之间的几何比
	- Step-and-Repeat的$NA$典型值为$0.60-0.68$

### Rayleigh Criterion for Resolution

![[Pasted image 20250218155034.png#pic_75center|Projection Printing]]

- Diffraction light from theAperture on the mask is collected by the Focusing Lens to project an image of the mask at the image plane on the photoresist on the wafer. The finite size of the condenser lens means that some of the diffracted light is lost.
掩模上的孔径产生的衍射光被聚焦透镜收集，用于在晶圆上的光刻胶图像平面上投影掩模的图像。由于聚光透镜的尺寸有限，部分衍射光会丢失。

![[Pasted image 20250218155332.png#pic_75center|]]

- The Rayleigh’s criterion for resolution of the images occurs when the center of one “Airy” pattern is at the first minimum of the other “Airy” pattern
瑞利判据用于图像分辨率的情况是，当一个“艾里斑”的中心位于另一个“艾里斑”的第一个极小值处时。
- Resolution (minimum distance between the two sources) is given by$$W_{\text{min}}=k_1\frac{\lambda}{NA}$$$k_1$ factor has no well-defined physical meaning. It is an experimental parameter, depends on the lithography system and resist properties. Typical values are close to 1.
   $k_1$因子没有明确的物理意义。它是一个实验参数，取决于光刻系统和光刻胶的特性。典型值接近1。 ^d1580e

## Depth of Focus (DOF)

- **Depth of focus**: Range of focus error that a process can tolerate $$\sigma=\pm\frac{W_{\text{min}}/2}{\mathrm{tan}\theta}\cong\frac{\frac{k_1\lambda}{2NA}}{\mathrm{sin}\theta}$$
	- $\mathrm{tan}\theta \sim \mathrm{sin}\theta$对于$\theta<12\degree$成立
	- 之前的PPT写的是$W_{\text{min}}=k_1 \frac{\lambda}{NA}$，这里写的是$W_{\text{min}}=\frac{k\lambda}{NA}$，为了前后一致写$k_1$
- 继续替换$n\mathrm{sin}\theta=NA$，可以得到：$$\sigma=\pm\frac{\frac{k_1\lambda}{2NA}}{\frac{NA}{n}}\cong\frac{k_2\lambda}{NA^2}$$显然可以得到：$$k_2=\frac{n}{2}k_1$$由于$k_1$是一个经验参数，所以$k_2$也是

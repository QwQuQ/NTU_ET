---
aliases: 
tags:
  - 这个ppt做得真棒大赏
---
- 吸收：$$A=0.686\left(\frac{t}{\delta}\right)\mathrm{dB}$$
- 反射：$$R=20lg\Big|\frac{Z_W}{4Z_S}\Big|$$
	- 自由空间波的特征阻抗$Z_W$：
		- 近场，电场：$$Z_W=\frac{1}{2\pi f\epsilon_0 r}$$
		- 近场，磁场：$$Z_W=2\pi f \mu_0 r$$
		- 远场：$$Z_W=377\Omega$$
	- 屏蔽材料内的特征阻抗：$$Z_S=\sqrt{\frac{\omega \mu}{\sigma}}$$
	- 补正（近场，磁场，$t<\delta$）：$$B=20lg\left(1-e^{-2t/\delta}\right)$$
- 开洞（$d<\lambda/2$），大了是0：$$SE=20log\left(\frac{\lambda/2}{d}\right)$$
	- 开很多洞：$$SE=20lg\left(\frac{\lambda/2}{d}\right)-20lg\sqrt{n}=20lg\left(\frac{\lambda/2}{d}\right)-10lg\ {n}$$
	- 用波导开洞：
		- 圆形波导：$$f_c=\frac{1.753\times 10^8}{d}$$ $$SE=32\left(\frac{L}{d}\right)\mathrm{dB}$$
		- 矩形波导：$$f_c=\frac{1.5\times 10^8}{d}$$ $$SE=27.3\left(\frac{L}{d}\right)\mathrm{dB}$$
- 谐振：$$f_{mnl}=\frac{c}{2\pi\sqrt{\mu_r \epsilon_r}}\sqrt{\left(\frac{m\pi}{L}\right)^2+\left(\frac{n\pi}{W}\right)^2+\left(\frac{l\pi}{H}\right)^2}\mathrm{Hz}$$ $$150\sqrt{\left(\frac{m}{L}\right)^2+\left(\frac{n}{W}\right)^2+\left(\frac{l}{H}\right)^2}\mathrm{MHz}$$
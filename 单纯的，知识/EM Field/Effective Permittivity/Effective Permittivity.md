---
aliases: 
tags:
  - rf
  - transmission_line
  - microstrip_line
---
由于微带线一半是PCB的基板，一半是空气，二者介质存在差异，所以需要用一个Effective Permittivity来等效描述介电常数，其中最主要的理论就是取二者平均$$\epsilon_{\text{eff}}\approx\frac{1+\epsilon_{r}}{2}$$继续添加其他修正项后可以得到：$$\epsilon_{\text{eff}}\approx\frac{1+\epsilon_{r}}{2}+\frac{\epsilon_r-1}{2}\left(1+12\times\frac{h}{w}\right)^{-0.5}$$
---
aliases:
  - 体效应参数
tags:
  - MOSFET
---
体效应影响MOS管的[[Threshold Voltage|阈值电压]]$$V_T=V_{T0}+\gamma\left(\sqrt{2\phi_F+V_{SB}}-\sqrt{2\phi_F}\right)$$
上式中：
- $V_{SB}$是源极到体的电压$(V)$
- $\phi_F$是表面电势$(V)$ $$\phi_s=2V_T\mathrm{ln}\frac{N_A}{n_i}$$
- $\gamma$是体效应参数$(V^{1/2})$ $$\gamma=\frac{t_{ox}}{\epsilon_{ox}}\sqrt{2q\epsilon_{\text{Si}}N_A}=\frac{\sqrt{2q\epsilon_{\text{Si}}N_A}}{C_{ox}}$$
- 不存在体电压时$V_T=V_{T0}$
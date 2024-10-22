---
aliases:
  - 体偏置效应
---

在源到体电压$V_{SB}$存在时，体偏置效应产生。体偏置效应影响[[Threshold Voltage|阈值电压]]

$$V_T=V_{T0}+\gamma\left(\sqrt{\phi_S+V_{SB}}-\sqrt{\phi_S}\right)$$
由于有时候没法把源连接到衬底，此时会导致[[Threshold Voltage|阈值电压]]改变。
$\phi_S$为MOSFET达到阈值时的表面电势，$\phi_S=2v_Tln\frac{N_A}{n_i}$
$\gamma$为体效应系数，公式为$\gamma=\frac{t_{ox}}{\epsilon_{ox}}\sqrt{2q\epsilon_{\mathrm{si}}N_A}=\frac{\sqrt{2q\epsilon_{\mathrm{si}}N_A}}{C_{ox}}$，同样也取决于受主浓度$N_A$
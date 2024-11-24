	受到某佬的启发，重新整理一下Filter，See圣虽然PPT写得不错但还是有提升的空间（

# LISN

在50Hz频率下，LISN会将市电传递给EUT（Equipment Under Test）；在EMI频率下（很高的频率），LISN会将这些电流送到频谱仪（50欧输入阻抗）。

所以差模阻抗是$50+50=100\Omega$，而共模阻抗是$50//50=25\Omega$

差模噪声电流在LN线之间流动，共模噪声电流在L//N线与地线之间流动。

# Exercise 1

A SMPS is powered by an AC power mains. It generates RF noise currents into the power mains through the power cord.

![[Pasted image 20241029201003.png#pic_center|]]

- The AC power mains can be modelled as a 50Hz AC source with a source resistance of $R_s$
- The SMPS can be modelled as a noise source $V_n$ with a source resistance of $R_n$

1. If $V_n=10mV$ and $R_n=30\mathrm{\Omega}$ at 1MHz, what is the expected level of RF noise current at 1MHz in the power line for $R_s=10\mathrm{\Omega}$?
2. If $R_s$ changes to $100\mathrm{\Omega}$, what is the expected level of RF noise current?

##### 解

- As we are only interested in RF noise current at 1 MHz, we could treat the 50Hz AC source as a short circuit for ease of analysis.
1. When $R_s=10\mathrm{\Omega}$, $$I_n=\frac{V_n}{R_n+R_s}=250\mathrm{\mu A}=48\mathrm{dB\mu A}$$
2. When $R_s=100\mathrm{\Omega}$, $$I_n=\frac{V_n}{R_n+R_s}=77\mathrm{\mu A}=37.7\mathrm{dB\mu A}$$

# Exercise 2

A power converter is connected to the 230V AC power mains. The power mains can be modeled as a termination resistance of $25\Omega$. The noise from the power converter can be modeled as a noise source with a source resistance of $5\Omega$. Either a shunt capacitor or series inductor can be used as a low-pass EMI filter to attenuate the noise. If the required filter attenuation is 40 dB at 100 kHz, estimate the value of the filter component for the following filter. Assume the filter component is ideal.

1. Shunt capacitor as low-pass EMI filter
2. Series inductor as low-pass EMI filter

## 解


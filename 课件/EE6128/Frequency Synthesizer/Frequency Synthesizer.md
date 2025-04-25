# Introduction

- What is a frequency synthesizer?
	- Generates one out of a large number of frequencies on external command
	  根据外部命令生成大量频率中的一种
	- High resolution
	  高分辨率
	- Output frequency $f_o$ is a rational multiple of a single standard frequency $f_s$.
	  输出频率 $f_o$ 是单一标准频率 $f_s$ 的有理数倍
	- Output frequency is stable and pure
	  输出频率稳定且纯净
	- Fast switching time
	  切换时间快
	- Low cost, small size, low power consumption
	  低成本、小体积、低功耗

- What are the properties of a frequency synthesizer?
	- Incorporates a frequency standard (reference oscillator)
	  包含频率标准（参考振荡器）
		- Output with high short- and long-term stability, low noise
		  输出具有高短期和长期稳定性，低噪声
		- Low cost crystal oscillators:
			- Long-term aging: 1 ppm per year
			- Frequency drift: 1 ppm over $-55\degree C$ to $100\degree C$
		- Higher quality crystal oscillators:
			- Long-term aging: 0.015 ppm per year
			- Frequency drift: 0.003 ppm over $0\degree C$ to $50\degree C$
	- Resolution: Frequency difference between adjacent output frequencies
	  分辨率：相邻输出频率之间的频率差：
		- 100 kHz: for general communications
		  用于常规通信
		- 0.01Hz: low-rate tracking systems; highly accurate frequency translations
		  用于低速跟踪系统和高精度频率转换
	- Number of frequencies
		- Varies: $100$ to $5\times 10^9$ discrete output frequencies
		  范围：$100$ 至 $5\times 10^9$ 离散输出频率
		- Eliminates need for so many high performance oscillators
		  消除了对许多高性能振荡器的需求
	- Programmability:
		- Output frequencies specified by the control signal
		  输出频率由控制信号指定
	- Switching time
		- Varies: $1m\mathrm{S}$ to $1\mu \mathrm{S}$
		  - 范围：$1\ \mathrm{ms}$ 到 $1\ \mu \mathrm{s}$
		- Architecture; frequency difference
		  依赖于架构和频率差
	- Spurious signals and noise
		- Amplitude normally leveled to a high degree
		  振幅通常被调到很高的电平
		- Primary output noise is phase noise
		  主要输出噪声是相位噪声
		- Coherent spurious signals: due to nonlinear operations such as mixing
		  相干杂散信号：由于混频等非线性操作引起
		- Noncoherent noise: internal circuit noise
		  非相干噪声：内部电路噪声

- Why are frequency synthesizers required?
	- Crowding of the frequency spectrum
		- Channelised communication calls for high degree of accuracy in transmitted frequencies
		- Easy selectability of frequencies for effective use of available channels– minimal operator skill
	- Increasing use of computers and microprocessors
		- Frequency selectability on digital commands
		- Communications
		- Measurements: Automated; low cost
	- Advanced systems that are impractical without programmability and rapid switching

- What are the applications of frequency synthesizers?
	- Communications
		- Mobile communications: Cellular
			- Frequency bands: 900 MHz; 1.9 GHz
			- Channel spacing: 30 kHz--AMPS, IS-54; 200 kHz--GSM
			- Phase noise: $-100\mathrm{dBc/Hz}$ at $\Delta f=10\mathrm{kHz}$ from carrier
			- Spurious emission in adjacent channels: $-80$ to $–100 \mathrm{dBc}$
			- Automatic frequency control
			- Frequency-hopping CDMA
		- HF communications
			- Elimination of guard band; single sideband without a tracking carrier; quick adaptation to varying conditions
			- Resolution: 1-1000Hz; accuracy: 0.1 ppm
		- Broadcasting
			- Radio: Different stations
			- Carriers at the same frequency, within $\approx 1\mathrm{HZ}$; interference from multitone heterodyning eliminated
			- TV: Different transmitters using the same Channel; reception improved if carriers offset by 1/3, 2/3 or 4/3 of the line frequency
	- Measurements
		- Frequency selective and broadband device characterization
			- Dynamic range and accuracy limited by the synthesizer’s spurious/noise emissions
		- Automated System Testing
			- Synthesizer switching speed; self checking
			- Testing of airborne phased-array microwave modules:
				- 1648 solid-state transmit-receive modules, S- and X-band
				- Each module: 700 measurements, 800 limit comparisons
			- Bridge measurements
				- Microwave spectroscopy
				- Radar cross-section
			- Frequency measurements
	- Advanced systems
		- Frequency-hopping communication systems
			- General technique for fading, dispersive channels
		- Frequency-Agile radars
			- Reduces interference due to multipath
			- Reduces target cross-section fluctuations
			- Difficult to jam
		- Electronic warfare

## Phase Noise

![[Pasted image 20250416010810.png#pic_75center|]]
![[Pasted image 20250416011241.png#pic_75center|]]
- Usual method of specification:
	- Maximum power within a specified bandwidth, at a few specified frequency offsets from the carrier:
	  指定带宽内的最大功率，以及距离载波几个指定频率偏移处的最大功率：
- Typical performance:
	- $-80\mathrm{dBc}$ in a $25\mathrm{kHz}$ bandwidth at an offset of $50\mathrm{kHz}$
- Requirements vary with application
	- X-band Doppler radar: $-150\mathrm{dBc}/\mathrm{Hz}$ at $\Delta f=65\mathrm{kHz}$
- Short-Term stability:
	- Fluctuations in output frequency over 1s or less

# Direct Frequency Synthesizers

![[Pasted image 20250416012316.png#pic_75center|]]

- Direct Frequency Synthesizers
	- Generation of new frequencies from one or more frequencies using a combination of multipliers, dividers, switches, mixers, and bandpass filters
	  使用倍频器、分频器、开关、混频器和带通滤波器的组合，从一个或多个频率生成新频率
	- Advantages:
		- Fast frequency switching
		  快速的频率切换
		- Arbitrarily fine frequency resolution
		  任意精细的频率分辨率
		- Low phase noise
		  低相位噪声
		- Highest frequency of operation among various methods of synthesis
		  在各种合成方法中具有最高的工作频率
	- Disadvantages:
		- More hardware $\implies$ larger, more expensive
		  更多硬件 $\implies$ 体积更大，成本更高
		- Appearance of spurious signals in the output
		  输出中出现杂散信号

## Circuits Used in Direct Frequency Synthesizers

### Mixers

- Sum or difference of two signals at different frequencies
  两个不同频率信号的和或差：$$f_o = nf_l \pm mf_r$$where: 
	- $f_l$ is the higher power input signal (LO)
	  高功率输入信号（本振信号，LO）
	- $f_r$ is the lower power input signal
	  低功率输入信号
- Output contains, at reduced power levels: 
	- Each input frequency
	  低功率输入信号
	- Noise that accompanies each input
	  每个输入信号伴随的噪声
	- Harmonic intermodulation (IM) products
	  谐波互调（IM）产物
- Frequency translation: 
	- Downconversion; Upconversion
	  下变频；上变频
	- Guidelines available to reduce in-band IM products
	  减少带内交调有成熟的指导

![[Pasted image 20250416020247.png#pic_75center|]]
- Rejection of in-band mixer generated harmonics
  减少带内的谐波
	- Upconvertor: $f_o > f_l$ and $f_o >> f_r$ (Fig. 3.7)
	- Downconvertor: $f_o << f_l$ and $f_o << f_r$

### Multipliers

- Signal frequency applied to a nonlinear device
  信号频率应用于非线性器件
	- Resistive devices:
		- wideband but lossy
	- Reactive devices:
		- narrowband, low loss, likely to be unstable
	- Step Recovery Diode (SRD):
	  阶跃恢复二极管
		- Large number of harmonics
		  产生大量谐波
	- Electronically tunable filter:
	  可电子调谐滤波器
		- YIG, varactor
		  变容器
			- Drive current/voltage should be ‘clean’
- Spectral purity degrades by a factor $N$ ($20 \mathrm{log} N \mathrm{dBs}$)
  频谱纯净度下降N
- Modulation factor increases by a factor $N$
  调制度变大N

### Dividers

- Normally obtained using digital counters
  使用数字计数器实现
	- Spectral purity improves by a factor $N$ ($20 \mathrm{log} N \mathrm{dBs}$)
	  频谱纯净度提高N
	- Modulation factor decreases by a factor $N$
	  调制度缩小N

### Filters

- Narrow bandpass, or lowpass; always placed at the output of:
  窄带通滤波器或低通滤波器；始终放置在以下设备的输出端：
	- Mixer: contains a wide spectrum of signals
	  混频器：包含宽频谱的信号
	- Divider: has pulsed waveforms or a square wave
	  分频器：具有脉冲波形或方波
	- Multiplier: contains harmonics
	  倍频器：包含谐波
- To minimize time delay, largest possible bandwidth $\implies$ number of sections held to a minimum
  为了尽量减少时间延迟，采用尽可能大的带宽 $\implies$ 节点数量保持在最低水平

## Elementary Synthesizer Designs

### Synthesis with Dividers, Filters and Switches

- Input frequencies: $f_s \text{ to } f_s+\Delta f_s$
- Slower set-on times for lower output frequencies

![[Pasted image 20250416013844.png#pic_75center|]]

![[Pasted image 20250416013956.png#pic_75center|]]
- Single input frequency: BPFs to reduce harmonics
- Switching time: Propagation time through the selected divider and the following filter
![[Pasted image 20250416014252.png#pic_75center|]]
- For $f_s/N$ to be an integer, limited values of $N$

### Synthesis with Multipliers, Filters and Switches

![[Pasted image 20250416014459.png#pic_75center|]]

### Arithmetic Iteration Technique

#### Base 10 Technique
![[Pasted image 20250416014613.png#pic_75center|]]
- Iterative circuit, or, modular approach
	- Base $10$: Fig. 3.5 (amplifiers, filters not shown)
	- RF switch $S_i$ 1P10T: one output out of 10 inputs $9 + N_i f_o,\ (f_o = 0.1)$ (normalized)
- Operation
	- $\text{Output Frequency}=10+N_3f_o+N_2 f_o/10+N_1 f_o /10^2+N_0f_o /10^3$
- Tuning increment:
	- Determined by the number of dividers
	- Can be increased arbitrarily by adding identical modules
- Typical switching time:
	- a few $\mu\mathrm{S}$ (for large increments)
	- 30 $\mu\mathrm{S}$ (for very fine increments)
![[Pasted image 20250416015659.png#pic_75center|]]
- Delay for tuning increment of multiples of $10^{-3} f_o$: $$(S_0)=3\left(\tau_b+\tau_d+\tau_l\right)+\tau_b$$
- Spurious rejection due to switch isolation: Switches farthest from the output can have the least amount of isolation
  由于开关隔离导致的杂散抑制：距离输出最远的开关能具有最小程度的隔离。
- Filters farthest from the output can be less complex
  距离输出最远的滤波器可以设计得较为简单。

#### Base 8 Technique

![[Pasted image 20250416021407.png#pic_50center|]]

![[Pasted image 20250416021132.png#pic_50center|]]
- Very similar to base-10: Fig. 3.8
- Advantages: Better compatibility with binary logic
	- Division by 8 is simpler
	- Implementation of 1P8T is simpler 9 reference frequencies (vs. 11 for base-10)

##### 一个例子

![[Pasted image 20250416021616.png#pic_50center|]]

- Fig. 3.10: Conversion of normalized approach to a specific frequency band
	- Let the largest tuning increment be in multiples of 8MHz$$f_o = 8 \mathrm{MHz}$$
	- Let the lowest frequency output be 1024MHz$$\text{input} = 1024/8 = 128 \mathrm{MHz}$$
	- Switch inputs: $$7 \times 128 = 896 \mathrm{MHz}$$ $$896 + 8 = 904$$ $$896 + 7 \times 8 = 952$$
	- $\text{Let number of discrete frequencies}=8^3$
	- $\text{Minimum tuning increment} = 8\mathrm{MHz}/8^2$
	- $\text{Output tunable from } 1024 \text{ to } 1087\frac{7}{8}$

#### Base 2

![[Pasted image 20250416022430.png#pic_50center|]]

- Advantages:
	- Less complicated switches (1P2T vs. 1P10T)
	- Least number of fixed frequency references (5)
	- Each divide-by-2 reduces spurious by 6dB
	  每次二分频可将杂散信号降低 6dB
	- Highest output frequency capability
	  输出频率的能力最好
- Disadvantages:
	- Highest number of parts to achieve a certain number of discrete frequencies ($2^N$ for N mixers)
	  为实现特定数量的离散频率所需的零件数量最多（对于 N 个混频器，需要 $2^N$ 个）
	- an amplifier required for each pair of mixers
	  每对混频器需要一个放大器

- Greatest potential for minimum switching time
	- Divide-by-2 circuits can operate at $>4\mathrm{GHz}$
	  二分频电路可在 $>4\mathrm{GHz}$ 下运行
- Operation:
	- Increasing the inputs to mixer M1 causes the output to increase
	  增加混频器 M1 的输入会导致输出增加
	- Decreasing the right-side input to M2 causes the output to increase
	  减少混频器 M2 右侧的输入会导致输出增加
	- Choice of frequencies:
		- At M1 (an upconverter), the LO input frequency >> signal input frequency
		- At M2 (a downconverter), the LO and signal input frequencies must be >> output frequency
- Reason for having 2 mixers per divider:
	- To prevent excessive spurious at the mixer output
	  防止混频器输出出现过多的杂散信号
	- Input will cause many mixer-generated spurious responses in (or near) the desired output band
	  输入会在目标输出带内（或附近）产生许多由混频器生成的杂散响应

![[Pasted image 20250416022842.png#pic_50center|]]
![[Pasted image 20250416023025.png#pic_50center|]]
![[Pasted image 20250416023144.png#pic_50center|]]

#### Base 4

![[Pasted image 20250416023420.png#pic_50center|]]
![[Pasted image 20250416023611.png#pic_50center|]]
![[Pasted image 20250416023622.png#pic_75center|]]
- Normalised base-4 circuit
	- The number of discrete frequencies = $4^N$
	  离散频率的数量 = $4^N$
- Main advantage:
	- For the same number of selectable frequencies, half the number of parts compared to base-2
	  在相同的可选频率数量下，与以2为底相比所需部件数量减半

#### Summary

- Comparison of complexity
	- $X = B^N$
	  where
		- X = number of selectable frequencies
		- B = base number
		- N = number of switch mixer combinations = number of iterative stages (mixer, filter, amplifier)
- For X = 1 million

| Base | N = No. of Mixers | S = No. of Sources | Sum = N+S |
| ---- | ----------------- | ------------------ | --------- |
| 10   | 6                 | 11                 | 17        |
| 8    | 7                 | 9                  | 16        |
| 4    | 10                | 9                  | 19        |
| 2    | 20                | 5                  | 25        |
- Base-8 has the least complexity; delay time is also close to best.
- For small X, base-2 approach may be the best

# Indirect Frequency Synthesizers

![[Pasted image 20250416012511.png#pic_75center|]]

- PLL Components:
	- VCO
	- Phase Detector
	- Loop Filter
	- Divider
- Operation
	- Under conditions of lock, the phase difference is constant and the input to the VCO is constant $\implies$ $$f_{\text{OUT}}=N f_{\text{REF}}$$
## Loop Filter

- Suppresses undesired signal components in the phase detector output. Also has an effect on noise, acquisition of lock, response speed, and loop stability
  抑制PD输出中不需要的信号成分。同时对噪声、锁定的获取、响应速度和环路稳定性产生影响。

## VCO

- An ideal VCO is a circuit that generates a periodic output whose frequency is a linear function of a control voltage, $V_{\text{control}}$:$$\omega_{\text{OUT}}=\omega_{\text{FR}}+K_{\text{{VCO}}}V_{\text{control}}$$where:
	- $\omega_{\text{FR}}$: free-running frequency
	- $K_{\text{VCO}}$: gain of the VCO in $\mathrm{rad}/s/V$
	- The output of a sinusoidal VCO can be expressed as $$y(t)=A\mathrm{cos}\left(\omega_{\text{FR}}t+K_{\text{VCO}}\int_{-\infty}^{t}V_{\text{control}}\mathrm{d}t\right)$$Thus, for constant $V_{\text{control}}$, frequency shifted by $K_{\text{VCO}}V_{\text{control}}$
- For $$V_{\text{control}}=V_m\mathrm{cos}\omega_m t$$ $$y(t)=A\mathrm{cos}\left(\omega_{\text{FR}}+\frac{K_{\text{VCO}}}{\omega_m}V_m\mathrm{sin}\omega_mt\right)$$i.e., a VCO acts like a frequency modulator, and also like a low-pass filter.
- Since the excess phase $$\varphi(t)=K_{\text{VCO}}\int_{-\infty}^{t}V_{\text{control}}\mathrm{d}t$$the input-output transfer function is $$\frac{\varphi_{\text{out}}}{V_{\text{control}}}(s)=\frac{K_{\text{VCO}}}{s}$$

![[Pasted image 20250416025527.png#pic_50center|]]
- The integration in VCO implies that to change phase, one must first change the frequency (i.q., control voltage) and let the integration take place.
	- $t < t_0$ , VCO output same as reference frequency, but phase error (say, VCO phase lags)
	- To reduce phase error, $V_{\text{control}}$ stepped up by $+\Delta V$ at $t=t_0$ VCO frequency increases;
	- VCO output phase accumulates faster than reference
	- At $t = t_1$ , phase error $\rightarrow 0$, $V_{\text{control}}$ returns to its initial value
- The output phase depends on the history of $V_{\text{control}}$

## Phase Detectors
![[Pasted image 20250416030311.png#pic_75center|]]
- An ideal phase detector (PD) produces an output signal which has its dc (or average) value linearly proportional to the difference between the phases of two periodic inputs (Fig. below):$$\overline{v}_{\text{out}}=K_{\text{PD}}\Delta\varphi$$where:
	- $K_{\text{PD}}$: gain of the phase detector ($V/\text{rad}$)
	- $\Delta \varphi$: input phase difference

### Multiplier

- A commonly used type; also called a mixer or a sinusoidal PD.
- For two input signals $x_1(t)$ and $x_2(t)$, $$x_1(t)=A_1\mathrm{cos}\omega_1t$$ $$x_2(t)=A_2\mathrm{cos}\omega_2 t$$the multiplier generates$$y(t)=\frac{\alpha A_1 A_2}{2}\mathrm{cos}\left[\left(\omega_1+\omega_2\right)t+\Delta \varphi\right]+\frac{\alpha A_1A_2}{2}\mathrm{cos}\left[\left(\omega_1-\omega_2\right)t-\Delta \varphi\right]$$for $\omega_1=\omega_2$, the phase-voltage characteristic is given by$$\overline{y}(t)=\frac{\alpha A_1A_2}{2}\mathrm{cos}\Delta\varphi$$ $$\mathrm{cos}\Delta\varphi\left\{\begin{align}= 0,&\quad \text{ for }\Delta\varphi=\pi/2 \\ \approx  \pi/2-\Delta\varphi,&\quad \text{ for  }\Delta \varphi \text{ in the vicinity of }\pi/2\end{align}\right.$$yielding $$K_{\text{PD}}=-\frac{\alpha A_1A_2}{2}$$
- Note: $$\overline{y}(t)=0\text{, for }\omega_1\neq\omega_2$$

### Exclusive-OR

![[Pasted image 20250416031422.png#pic_75center|]]

- Equivalent of a balanced mixer, to a certain degree $$\text{output:}\pm V_{\text{ss}}$$
- For unsymmetrical input waveforms, the average output voltage may be same for two different errors $\implies$ use of pulse stretchers

## Digital PLL

![[Pasted image 20250416031701.png#pic_50center|]]
- Employs: phase/frequency comparator built using digital components;
- frequency divider in the loop

- Frequency multiplication
	- It is often required that the output frequency of a PLL be a multiple of the input frequency. This requires insertion of a frequency divider in the feedback loop: Fig. 4.17. The divide ratio $M$ is called the modulus.
	- The loop ‘gain’ (for phase) is divided by $M$; all the previous analyses can be directly applied if $K$ (loop gain, Eq. 4.13) is replaced by $K/M$.
	- Frequency multiplication also amplifies the input phase noise. The magnitude of phase noise within the 3-dB bandwidth of the PLL is multiplied by a factor of $M$.

## Integer-N

![[Pasted image 20250416031855.png#pic_50center|]]

- Requirement: $$f_{\text{out}}=f_o+kf_{\text{ch}},\ 0\leq k \leq Q$$
- in steps of 1:$$f_{\text{out}}=Mf_{\text{ref}},\ M_L\leq M \leq M_H \implies f_{\text{ref}}=f_{\text{ch}},\ f_{\text{out}}=M_L f_{\text{ref}}+kf_{\text{ref}}$$
- Example:
	- IS-54 receive-band (869 – 894 MHz)
		- $f_o = 869 \text{MHz}$, $k = 0,1,\cdots,833$
		- $f_{\text{ch}}=30\mathrm{kHz}$, $M\approx 30,000$
	- For GSM, $f_{\text{ch}} = 200 \mathrm{kHz}$

# Direct Digital Frequency Synthesizers

![[Pasted image 20250416012850.png#pic_50center|]]

- Basic idea: Generate the signal in the digital domain, utilize D/A conversion and filtering to reconstruct the waveform in the analog domain.
- Principle of operation: Fig. 5.1
	- A counter counts from $0$ to $N$ in steps of unity, generating a digital ramp waveform. Each number generated by the counter is then used to select a value from the ROM that corresponds to a sample of a sinusoid.
	- This is followed by D/A conversion and filtering.
	- If the counter addresses fewer (evenly spaced) points of one cycle of the sinusoid, the output frequency is higher, and vice-versa.
	- This is possible if the counter increments its output by a programmable step $P$

## Use of an Accumulator

![[Pasted image 20250416032630.png#pic_75center|]]
- A parallel-in, parallel-out M-bit register drives an adder in a feedback loop.
- On every clock cycle, a value equal to P is added to YR , and the result is applied to the register, i.e.,$$X_{\text{R}}(k)=Y_{\text{R}}(k-1)+P$$
- This relation holds until the register overflows, at which point part of P appears as an increment in the new value of XR , i.e.,$$X_{\text{R}}(k)=\left\{Y_{\text{R}}(k-1)+P\right\}\text{ module }2^M$$

## Example

![[Pasted image 20250416032827.png#pic_75center|]]

- $P=1$: As the register output goes from 000 to 111, one complete cycle of a sinewave is extracted from the ROM; each clock period increments the output phase by $2\pi/8$ radians
- $P=2$: The accumulator overflows after 110; every alternate sample of the sinwave is read from the ROM; each clock period increments the output phase by $2\pi/4$

![[Pasted image 20250416033105.png#pic_70center|]]
- $P=3$: The accumulator output overflows at 110, 111, and 101 in the first, second and third cycle, respectively; three cycle of a sinusoid are produced by 8 uniformly spaced samples
- $P=4$: Four cycles of the sinusoid are generated by Nyquist rate sampling.

## Frequency of the sinewave

![[Pasted image 20250416033233.png#pic_75center|]]
- Frequency of the sinewave generated (in FIG. 5.2) is$$f_{\text{out}}=P\frac{F_{\text{CK}}}{2^M},\ P=1,2,\cdots,2^M\cdots\cdots (5.2)$$ $2^M/P$ need not be an integer
- Eq. (5.2) suggests that increasing $M$ yields arbitrarily small steps in the output frequency

## Number of bits in the ROM

![[Pasted image 20250416033233.png#pic_75center|]]

- The M-bit word applied to the ROM selects a value for the amplitude of the sinusoid. Since the ROM o/p approximates the amplitude, the number of bits (k) determines the quantization error in the reconstructed sinewave.
- The quantization error appears as a periodic additive term rather than random noise. The resulting error waveform and its harmonics appear as spurs in the o/p spectrum. It can be shown that the worst-case power of these spurs relative to the signal power is close to 5.3 where it is assumed that fCK = 2 fout. For k = 12 bits, the spurs are about 71dBc.
- The number of bits M in the accumulator is kept at 16 to permit fine frequency steps. If the number of bits in the ROM output are limited to 10, the ROM requires 216x10  6.55x105 cells.
- To reduce ROM size, only the most significant bits may be passed on from the accumulator to the ROM.
- However, if the ROM phase steps are not as small as those in the accumulator, a ‘phase truncation error’ corrupts the o/p sinusoid. This error is also periodic, resulting in spurs.
- ROM size can also be reduced by storing only one-quarter period of the sinusoid; the other three quarters can be obtained by virtue of vertical and horizontal symmetry.

## Summary

- Advantages of direct digital synthesis:
	- Avoiding the use of an analog VCO, DDS achieves a low phase noise: roughly equal to that of the clock. The clock frequency can be fixed and can be derived from a crystal oscillator using a wideband PLL.
	- Fine frequency steps can be achieved using longer word length in the accumulator.
	- Much faster switching than PLLs because there is no feedback loop.
	- Can provide continuous-phase channel switching at the o/p, an important requirement in some modulation schemes.
	- Allows direct modulation of the o/p signal in the digital domain.
- Drawbacks of direct digital synthesis:
	- The clock speed must be at least twice the desired o/p frequency. This requirement is difficult to meet at RF frequencies; particularly the DAC remains the speed bottleneck.
- Applications of direct digital synthesizers:
	- As low frequency generator in the multi-loop architectures, replacing the slower PLL.

# Wideband Microwave Frequency Synthesizers

![[Pasted image 20250416033636.png#pic_50center|]]

- Frequency synthesis with YIG devices:
	- A high frequency reference $f_h$ drives an **SRD** circuit that outputs many harmonics in the microwave frequency band. One of these, $nf_h$ , is selected using a programmable YIG-tuned filter. The selected harmonic is mixed with $f_o$ and divided by 10 in order to lower the IF for digital phase-frequency detector. Under conditions of phase-lock $$\frac{f_o-nf_h}{10}=N_2f_l$$and the TIG-tunes oscillator's frequency is given by$$f_o=10N_2f_l+nf_h$$

## Example

- Requirement: Microwave synthesizer tunable in $100\mathrm{kHz}$ steps, from 4 to 5.9999 GHz
- Let $f_l = 10 \text{kHz}$, $N_2 = 2000\text{ to }2999$ in steps of unity
- $10N_2f_l=200\text{MHz to }299\text{Mhz}$ in steps of 10-, 1-, and 0.1- MHz.
- Let $f_h = 100 \text{MHz}$, $nf_h = 3800- to 5700-\text{MHz}$ in steps of $100\text{MHz}$.
- For each $100\text{MHz}$ step, $N_2$ can vary over its range.

## Summary

- Advantages and disadvantages:
	- Excellent spectral purity due to YIG devices which have a high Q
	- Frequency set-on time is slow compared to varactor-tuned devices
	- Highly stable components are required in the YIG drivers to maintain the desired harmonic level; periodic calibration of the YIG devices may be required.

# Frequency Synthesizers Combining Direct and Indirect Techniques

![[Pasted image 20250416034517.png#pic_75center|]]
- The reference frequencies required in the fast-switching direct-type synthesizers can be obtained from a single reference frequency using techniques of indirect-type synthesizers.
- Further, where moderate switching speeds (a few hundred microseconds) are acceptable, the direct-type designs can be simplified by incorporating indirect-type techniques.

- Fig. 7.1: Synthesized references for base-8 synthesizer
- The base-8 direct synthesizer technique (Fig. 3.10) needs nine sources derived from a single standard.
- This can be accomplished by using a 128MHz crystal oscillator to ‘feed’ eight similar (fixed) PLL oscillators. The scheme is illustrated in Fig. 7.1 (showing 4 of the 8 oscillators). The remaining 4 frequencies can be generated in a similar fashion.

![[Pasted image 20250416034639.png#pic_75center|]]
- Fig. 7.3: Base-8 synthesizer with agile phaselocked Loops
- For the base-8 synthesizer (Fig. 3.10), when the switching speed is not very demanding, each 1P8T switch is replaced with a single VTO and a programmable divider, with division from $112\times 2$ to $119\times 2$, to make an agile synthesized LO for each mixer.
- Reduction of parts:
	1. Phase-locked VTOs, from 8 to 3
	2. 1P8T RF switches, from 3 to 0
	3. Isolation devices: not needed because each mixer LO is derived from a single agile source. 
- Settling time: For the 4 MHz loops, the bandwidth $\approx400 \text{kHz}$  ($=4\text{MHz}/10$); phase-lock occurs in a time$\approx 2.5\mu S$ ($=1/400\mathrm{kHz}$); additional 10 to 30 $\mu S$ for the phase transient to settle to the steady-state value

# Reference Frequency Isolation

- Whenever we have the condition where a fixed reference is applied to two or more mixers where the other inputs to the mixers are not at equal frequencies, all of the harmonic modulation products present in one mixer may be coupled to all other mixers through the paths provided by the fixed-frequency inputs.
- To reduce this effect, the output from each source is initially RFpower-divided, and it is ensured that the o/p lines from the RF power divider are isolated from each other.

![[Pasted image 20250416035216.png#pic_75center|]]

- These isolation techniques usually include isolators, or a series of attenuators + amplifiers, as shown in Fig. 7.2. (a)& (b): Isolation between switches (c) Isolation between mixer and switch
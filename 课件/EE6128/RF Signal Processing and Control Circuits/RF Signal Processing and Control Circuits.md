# pn and Schottky-Barrier Junctions

![[Pasted image 20250507235617.png#pic_50center|]]
- Formed in semiconductor crystals when the conductivity type changes from n-type to p-type
  在半导体晶体中形成，当导电类型从 n 型变为 p 型时
- Diffusion of free charge carriers shown Fig. 2.1
  自由电荷载流子的扩散如图2.1所示

## Equivalent ac circuit model of a diode

![[Pasted image 20250507235657.png#pic_50center|]]
- Equivalent ac circuit model (Fig. 2.5), including
  等效交流电路模型（图 2.5），包括
	- the junction resistance & capacitance
	  结电阻和电容
	- parasitic reactances due to packaging
	  由于封装导致的寄生电抗
- The series resistor $R_S$ accounts for contact and current spreading resistance.
  串联电阻 $R_S$ 用于考虑接触电阻和电流扩展电阻

## Schottky-barrier diode applications

- Limitations of $\mathrm{Si}$ pn diodes at high frequencies
	- Large junction capacitance due to large minority carrier life-time (can be as high as hundreds of ms)
	  由于少数载流子寿命较长（可高达数百毫秒），导致较大的结电容
	- Low mobility of the charges
	  载流子迁移率较低
	- Useful only up to tens of MHz
	  仅适用于最高几十兆赫的频率范围

![[Pasted image 20250507235959.png#pic_75center|]]
- The Schottky-barrier diode may be a
	- High-barrier type: metal/ntype; require dc bias for max sensitivity
	  **高势垒型**：金属/n 型；需要直流偏置以实现最大灵敏度
	- Low-barrier type: metal/ptype; higher power sensitivity (as low as – 70 dBm)
	  **低势垒型**：金属/p 型；具有更高的功率灵敏度（可低至 –70 dBm）
	- Detection, demodulation and mixing as in Figure.
	  **检测、解调和混频**，如图所示

# Detection and mixing: General considerations

![[Pasted image 20250508000309.png#pic_75center|]]
- Detector and mixer diodes use the nonlinear I-V characteristic of a pn junction or Schottky-barrier junction.
  检波器和混频器二极管利用 pn 结或肖特基势垒结的非线性 I-V 特性
- Desirable device properties
	- Variable nonlinear resistance
	  可变的非线性电阻
	- High cutoff frequency$$f_{CO}=\frac{1}{2\pi R_S C_{j}}$$normally, the operating frequency is one-tenth the cutoff frequency.
	  通常工作频率为截止频率的十分之一
	- Low barrier height: less LO power
	  低势垒高度：较低的 LO 功率
	- High breakdown voltage: Higher RF power and burnout level
	  高击穿电压：更高的射频功率和抗烧毁能力
	- Quick recovery after saturation, requires no minority carrier storage
	  饱和后快速恢复，不需要少数载流子存储
- Most of these requirements are fulfilled by Schottky-barrier diodes. Further, GaAs diodes offer higher operating frequencies compared to Si.
  肖特基势垒二极管满足大部分这些要求。此外，GaAs 二极管相比于 Si 具有更高的工作频率

## Detector sensitivity

- Typical circuit representation: Fig. 3.5
- Typical signal levels: -60 to -30dBm
  典型信号电平：-60 至 -30 dBm
- Typical forward bias for highest detector sensitivity: $10$ to $100\mathrm{\mu A}$
  最高检测灵敏度所需的典型正向偏置：$10$ 至 $100\mathrm{\mu A}$
- Current sensitivity of a detector:
  检波器的电流灵敏度：$$\beta_i=\frac{i_{DC}}{P_a}$$ (generally expressed in $\mathrm{\mu A/\mu W}$), where is the input power absorbed by the diode and is the dc output current.
  （通常以 $\mathrm{\mu A/\mu W}$ 表示），其中 $P_a$ 是二极管所吸收的输入功率，$i_{DC}$ 是直流输出电流。
- From Fig. 3.5, one can prove that $$\displaylines{\beta_i=\frac{q}{2\eta kT}}\frac{1}{\left(1+\frac{R_S}{R_J}\right)^2}\frac{1}{1+\frac{\omega^2C_J^2R_SR_J^2}{R_S+R_J}}$$The loss in input signal power delivered to $R_J$ is given by 
  输入信号功率在传输至 $R_J$ 时的损耗为：$$\mathrm{L(dB)}=10\log \left(1+\frac{R_S}{R_J}+\omega^2C_J^2R_SR_J\right)$$

# Mixer operating theory

![[Pasted image 20250508020533.png#pic_50center|]]
- Noise spectrum for a typical detector diode: Fig. 3.6. At low modulation frequencies, the sensitivity is limited by the 1/f noise. The sensitivity of a microwave receiver can be improved significantly by using the heterodyne scheme, using a mixer: Fig. 3.7. The forward bias is typically achieved by the LO pump power, which is rectified by the diode. IF frequency is selected to be much higher than 1 MHz. Much better sensitivity at the cost of more complicated circuit.
  典型检波二极管的噪声谱（图 3.6）。在低调制频率下，灵敏度受到 1/f 噪声的限制。微波接收机的灵敏度可以通过采用外差方案（heterodyne scheme）并使用混频器（图 3.7）显著提高。正向偏置通常由本振（LO）泵浦功率提供，并由二极管整流。中频（IF）频率选定远高于 1MHz。提高灵敏度的同时，电路变得更加复杂。

- 设$$v=v_{RF}\sin\omega_{RF}t+v_{LO}\sin\omega_{LO}t$$其中$v_{RF}$和$v_{LO}$时信号的幅度，所以电流为：$$\displaylines{i\approx a_1v+a_2v^2=a_1\left(v_{RF}\sin\omega_{RF}t+v_{LO}\sin\omega_{LO}t\right)+a_2\left(v_{RF}\sin\omega_{RF}t+v_{LO}\sin\omega_{LO}t\right)^2+\cdots \\ =a_1\left(v_{RF}\sin\omega_{RF}t+v_{LO}\sin\omega_{LO}t\right)+ \\ a_2\left\{\frac{1}{2}v_{RF}^2\left(1-\cos 2\omega_{RF}t\right)+v_{LO}v_{RF}\left[\cos \left(\omega_{RF}-\omega_{LO}\right)t-\cos\left(\omega_{RF}+\omega_{LO}\right)t\right]+\frac{1}{2}v_{LO}^2\left(1-\cos 2\omega_{LO}t\right)\right\}+ \\ \cdots}$$可以使用一个低通滤波器提取$$\omega_{RF}-\omega_{LO}$$其他的频率被耗散掉
- 混频器的转换损失为：$$L_c\mathrm{(dB)}=10\log\frac{P_{RF}}{P_{IF}}$$
- Typical performance:
	- Conversion loss 4 to 5 dB @ 10 GHz; 5 to 6 dB @ 45 GHz; 7 to 9 dB @ 94 GHz

# Varactor diode and applications

![[Pasted image 20250508021908.png#pic_50center|]]
- Construction and operation
	- Most varactors are fabricated on n-type semiconductors with p+ type diffusion to form junctions.
	  大多数变容二极管采用 n 型半导体制造，并通过 p+ 型扩散形成结
	- Normally operated under reverse bias as a voltage-variable capacitor (depletion capacitance).
	  通常在反向偏置下工作，作为电压可变电容（耗尽电容）
	- Applications in frequency tuning, frequency multiplication, harmonic generation, and parametric amplification.
	  应用于频率调谐、频率倍增、谐波产生以及参量放大
- Junction capacitance (depletion):$$C_j(V)=\frac{C_{j0}}{\left(1-\frac{V}{V_{bi}}\right)^\gamma}$$where $\gamma$: 
	- $1/2$ for an abrupt junction
	  突变结
	- $1/3$ for a graded junction
	  渐变结
	- $1-2$ for hyperabrupt junctions
	  超突变结

# Tunable oscillator and filter

- A microwave oscillator can be tuned electronically by incorporating a varactor; compared to bias tuning, this results in a fairly constant o/p power. This is a very important application of varactor diodes.
  通过集成变容二极管，微波振荡器可以进行电子调谐；相比于偏置调谐，这种方式能保持较为稳定的输出功率。这是变容二极管的一个重要应用
- VCOs have applications in FM systems and frequency-agile systems commonly used in radar and communications.
  压控振荡器（VCO） 广泛应用于 调频（FM）系统 以及 频率自适应系统，后者常用于 雷达 和 通信 领域
- Example application of a VCO:
  VCO 的典型应用：
	- Synthesizers; very useful in Cellular communication system
	  频率合成器（Synthesizer），在蜂窝通信系统中非常实用
- Synthesizers are also used widely in instrumentation, electronic warfare (EW), and electronic countermeasure systems (ECM).
  频率合成器 也被广泛应用于 仪器设备、电子战（EW）以及电子对抗系统（ECM）

![[Pasted image 20250508022516.png#pic_50center|]]
- A possible oscillator circuit, using varactor tuning, is shown schematically in Fig 3.9
  一种可能的振荡器电路，采用变容二极管调谐，在图 3.9 中以原理图展示
- Without the varactor, the oscillation frequency is
  在没有变容二极管的情况下，振荡频率为 $$f_O=f_r=\frac{1}{2\pi \sqrt{L_L C_D}}$$where $C_D$ depends on the bias voltage. This may be used for bias tuning.
  其中，CDC_D 依赖于偏置电压，可用于偏置调谐
- With the varavtor included 
  加入变容二极管后，振荡频率变为$$f_O=f_r=\frac{1}{2\pi\sqrt{L_LC_T}}$$where $$C_T=\frac{C_j(V)C_D}{C_j(V)+C_D}$$
- Effectiveness of varactor tuning depends on the varactor, coupling circuit, load, and the active device.
  变容二极管调谐的有效性 取决于 变容二极管本身、耦合电路、负载以及有源器件。

---

![[Pasted image 20250508022747.png#pic_50center|]]
- Electronically tunable filters Fig. 3.10
- The resonant frequency is $$f_r=\frac{1}{L_OC_T}$$where $$C_T=C_j(V)+C_O$$

# Multiplier and harmonic generator

- A varactor can be used for frequency multiplication or harmonic generation ($n \leq 4$) due to its nonlinear characteristics
  变容二极管可用于频率倍增或谐波产生（$n \leq 4$），其非线性特性可表示为$$i=a_1v+a_2v^2+a_3v^3\cdots$$with low phase noise. This is useful to generate high millimeter-wave frequencies where fundamental sources are difficult to obtain.
  且具有低相位噪声。这在高毫米波频率的生成中非常有用，因为基波信号源较难获得。

![[Pasted image 20250508022947.png#pic_50center|]]
- Multiplier circuit block-diagram:
	- Low-pass filter: Passes only the fundamental
	  低通滤波器：仅允许基波通过
	- Bandpass filter: Passes only the desired harmonic
	  带通滤波器：仅允许所需的谐波通过
	- Input and output circuits conjugately matched to the varactor at their respective frequencies.
	  输入和输出电路：在各自的频率下与变容二极管进行共轭匹配
	- The multiplier should be open-circuited at all harmonics other than the input and output frequencies.
	  倍频器在除输入和输出频率外的所有谐波处应开路

![[Pasted image 20250508023805.png#pic_50center|]]
- Conversion efficiency $$\eta=\frac{P_{\text{out}}(\text{output power of the desired harmonic})}{P_{\text{in}}(\text{input power of the fundamental})}$$
- Estimated maximum efficiency for a doubler: Fig. 3.12

# PIN diode and applications

- Similar to pn-junction diode but with a smaller junction capacitance and high reverse breakdown voltage.
  类似于 pn 结二极管，但具有较小的结电容和较高的反向击穿电压
- This type of diodes are very useful for high frequency, high power applications.
  这种二极管非常适用于高频、高功率应用
- Extensively used in microwave circuits for switching, phase shifting, attenuation, leveling and limiting.
  在微波电路中被广泛用于开关、移相、衰减、功率均衡和限幅

![[Pasted image 20250508024159.png#pic_50center|]]
- Construction and operation
	- lightly doped intrinsic region sandwiched between two heavily doped p and n regions: Fig. 3.14.
	  轻掺杂的本征区夹在两个高度掺杂的 p 和 n 区之间（图 3.14）
	- If the i-region consists of n-type impurities, $\nu$-type p-i-n
	  如果本征区含有 **n 型** 杂质，则称为 $\nu$-型 p-i-n 结构
	- If the i-region consists of p-type impurities, $\pi$-type p-i-n
	  如果本征区含有 **p 型** 杂质，则称为 $\pi$-型 p-i-n 结构
	- The depletion region extends throughout the i-region, with little extension into both p+ and n+ regions.
	  耗尽区贯穿整个本征区，仅在 p+ 和 n+ 区域略微扩展
	- A wider depletion region considerably reduces the depletion capacitance, making the diode a better ‘open circuit’ under reverse bias. The reverse breakdown voltage also increases.
	  更宽的耗尽区 可显著减少耗尽电容，使二极管在反向偏置时更接近“开路”，同时增加反向击穿电压。
	- When forward biased, high level of injected charges fills the intrinsic region; at higher frequencies, there is not enough time to remove the charge, so the diode never turns off, and it behaves as a low resistance; diffusion capacitance is small.
	  在正向偏置时，大量注入的载流子填充本征区；在高频工作时，载流子无法及时移除，使得二极管始终导通，表现为低电阻，且 扩散电容较小

![[Pasted image 20250508024429.png#pic_50center|]]
- The I-V characteristics: Fig. 3.15
- Equivalent circuit: Fig. 3.16
- Arrow connected to $R_j$ for forward bias, and to $C_j$ , for reverse bias.
  箭头连接到 $R_j$ 以表示正向偏置，连接到 $C_j$ 以表示反向偏置
	- Typical parasitics:
		- $R_s=0.3\mathrm{\Omega}$
		- $L_s=0.1\mathrm{nH}$
		- $C_p=0.3\mathrm{pF}$
- Under forward bias (point $A$ in Fig. 3.15)
  在正向偏置下（图 3.15 中的点 $A$）
	- $C_j (V) \approx 1 \mathrm{pF}$
	- $R_j (V) = \frac{\mathrm{d}V}{\mathrm{d}I} = 0.5 \mathrm{\Omega}$
	- $Z_c=-\frac{j}{\omega C_j}=-j160\mathrm{\Omega}$ and $\left|Z_C\right|\gg R_j$ at $1\mathrm{GHz}$

![[Pasted image 20250508024808.png#pic_33center|]]
- Neglecting package effects, the equivlent circuit, as shown in Fig. 3.17a, is almost a short circuit
  忽略封装效应，等效电路（如图 3.17a 所示）几乎是短路
- Under reverse bias (point B in Fig. 3.15)
  在反向偏置下（图 3.15 中的点 B）
	- $C_j(V)\approx0.2\mathrm{pF}$
	- $R_j(V)\approx 20\mathrm{k\Omega}$
	- $Z_C=-\frac{j}{\omega C_j}=-j796\mathrm{\Omega}$ and $\left|Z_C\right|\ll R_j$ at $1\mathrm{GHz}$
- Neglecting package effects, the equivlent circuit, as shown in Fig. 3.17b, is almost an open circuit
  忽略封装效应，等效电路（如图 3.17b 所示）几乎是开路

## Switches

![[Pasted image 20250508025950.png#pic_50center|]]
- The use of a p-i-n diode as a switch is based on the impedance difference between the diode’s reverse- and forward-biased characteristics.
  p-i-n 二极管作为开关的使用基于其在反向偏置和正向偏置状态下的阻抗差异
- Switches have a number of applications in radar and communication systems, and microwave instrumentation.
  开关在雷达、通信系统和微波仪器中有多种应用
- Important specifications:
	- Insertion loss
	  插入损耗
	- isolation
	  隔离度
	- switching speed
	  切换速度
	- power-handling capability
	  功率处理能力

![[Pasted image 20250508025605.png#pic_50center|]]
- 插入损耗：
	- 串联：$$\text{Insertion Loss}=-20\log\left|\frac{2Z_0}{2Z_0+Z_d}\right|$$
	- 并联：$$\text{Insertion Loss}=-20\log\left|\frac{2Z_d}{2Z_d+Z_0}\right|$$
- 串联衰减：$$\alpha=10\log\left[\left(1+\frac{R}{2Z_0}\right)^2+\left(\frac{X}{2Z_0}\right)^2\right]$$其中：
	- $Z_D=R+jX$
- 串联散射参数：$$S_{21}=\frac{2Z_0}{R+jX+2Z_0}$$

## Phase Shifters

- Major application in phased arrays: phased-array radars; beam-forming networks
- Usually designed for ‘digital’ phase shifts of $\Delta\varphi=180\degree, 90\degree, 45\degree, \text{etc.}$
- Three basic types of p-i-n diode phase shifters
	- Switched-line phase shifter
	- Loaded-line phase shifter
	- Reflection (hybrid-coupler) type phase shifter

### Switched-line phase shifter

![[Pasted image 20250508030134.png#pic_50center|]]
- Most straightforward type; 2 SPDT switches;
  最简单的类型；2 个 SPDT 开关； $$\Delta\varphi=\beta(l_2-l_1)$$
- Features:
	- For TEM transmission-lines, phase shift is a linear function of frequency
	  对于 TEM 传输线，相移是频率的线性函数
	- true time delay; little distortion
	  真正的时延；畸变很小
	- Inherently reciprocal
	  本质上是互易的
	- Maximum number of diodes (4) per bit
	  每位最多 4 个二极管
	- Resonances may occur in the OFF line
	  在断开线路中可能出现谐振
	- High insertion loss at mm-wave frequencies
	  在毫米波频率下插入损耗较高

### Loaded-line phase shifter

![[Pasted image 20250508030145.png#pic_75center|]]
- 通过在传输线上并联电抗器件，起到移相的作用。
- 相移：$$\Delta\varphi=\tan^{-1}\frac{b}{2}$$

### Reflection (hybrid-coupler) type phase shifter

![[Pasted image 20250508032541.png#pic_50center|]]
- Principle:
	- An SPST switch controls the path length of a reflected signal.
	  SPST 开关控制反射信号的路径长度
	- Usually a quadrature hybrid is used to provide a 2-port circuit, although other types of hybrids, or even a circulator could be used for this purpose.
	  通常使用正交混合器来提供一个双端口电路，尽管其他类型的混合器，甚至环行器也可以用于此目的
- Operation:
	- An input signal is divided equally, but $90\degree$ out-of-phase, among the two right-hand ports of the hybrid.
	  输入信号被均等分配，但在混合器的两个右侧端口之间相差 $90\degree$ 的相位
	- Both diodes are biased in the same state; the waves reflected from the two terminations, add in-phase at the port marked ‘out’.
	  两个二极管处于相同的偏置状态；从两个终端反射的波在标有“输出”的端口处同相叠加
	- Turning the diodes on or off changes the total path length for both reflected waves by , producing a phase shift of at the output.
	  通过开关二极管的状态，改变两个反射波的总路径长度，从而在输出处产生相移

- Features:
	- Two diodes per bit
	  每位两个二极管
	- Any phase shift increment possible in principle
	  原理上可实现任意的相移增量
	- Above 40 GHz, difficult to achieve low-loss in the hybrid
	  在 40 GHz 以上的频率下，难以在混合器中实现低损耗

# Step-recovery diode and applications

- Also called snap-back diodes
- Very high harmonic multiplication, with high power levels, good efficiency, and bandwidth.
  具有极高的谐波倍增能力，具备高功率水平、良好的效率和带宽
- A few hundred MHz $\to$ several GHz
  频率范围从几百 MHz 到数 GHz
- Harmonic generation with an efficiency approaching 1/n (compared to 1/n2 for varactors)
  谐波产生效率接近 1/n（相比之下，变容二极管的效率为 1/n²）
- Does not require an idler circuit

## Operation and basic considerations

![[Pasted image 20250508032938.png#pic_50center|]]
- Uses capacitance variation to generate harmonics.
  通过电容变化来产生谐波
- This is achieved through charge storage under forward bias and switching very rapidly to high impedance state under reverse bias.
  这是通过正向偏置下的电荷存储，并在反向偏置时迅速切换到高阻抗状态来实现的
- The circuit is adjusted so that the diode switches at the instant the reverse current is maximum (Fig. 3.28), thus generating a large and sharp voltage pulse each excitation cycle.
  电路调整使二极管在反向电流达到最大值的瞬间切换（图 3.28），从而在每个激励周期产生一个大而尖锐的电压脉冲
- The resulting pulse train is rich in harmonic content
  由此产生的脉冲序列富含谐波成分

- Requirements/Reasons/Implications
	- High charge storage in the forward direction
	  正向方向具有高电荷存储
		- So that there is conduction even when reverse cycle begins: Long charge-storage time. Therefore silicon is used instead of GaAs
		  使得在反向周期开始时仍有导通：长电荷存储时间。因此，使用硅而不是 GaAs
	- Quick discharge during reverse cycle
	  反向周期中快速放电
		- So that high impedance state is achieved in a short time. This is the basic mechanism for generating a sharp voltage pulse: Charge injected during the forward cycle must not travel too far
		  使得在短时间内达到高阻抗状态。这是产生尖锐电压脉冲的基本机制：正向周期注入的电荷不应传播过远
	- Low capacitance in the reverse direction: Wide depletion width
	  反向方向低电容：宽耗尽区
	- Low series resistance: For low-loss, high efficiency
	  低串联电阻：低损耗、高效率
	- High reverse breakdown voltage: For high power applications
	  高反向击穿电压：适用于高功率应用
	- Short switching time: Establishes high frequency limit of operation
	  短开关时间：确立高频工作的上限
	- Not too wide depletion region: Otherwise, transit-time effects will reduce efficiency at high frequencies
	  耗尽区不宜过宽：否则，在高频下渡越时间效应会降低效率

## Construction and equivalent circuit

![[Pasted image 20250508033133.png#pic_50center|]]
- p-i-n structure, with intrinsic or lightly doped i-region (Fig. 3.29)
  p-i-n 结构，具有本征或轻掺杂的 i 区（图 3.29）

- During forward conduction, charge carriers injected into iregion where they recombine slowly
  在正向导通期间，电荷载流子被注入 i 区，并在其中缓慢复合
- During reverse-bias, i-region is fully depleted
  在反向偏置期间，i 区完全耗尽
- Reverse capacitance is low
  反向电容较低

![[Pasted image 20250508033319.png#pic_50center|]]
- p and n regions have a steep doping profile
  p 区和 n 区具有陡峭的掺杂分布
- Little extension of the depletion region into the p and n regions
  耗尽区向 p 区和 n 区的扩展较少
- Strong built-in electric field which opposes the diffusion of charge into the junction
  强大的内建电场，阻止电荷向结区域扩散

![[Pasted image 20250508033414.png#pic_50center|]]
- Equivalent circuit
- Forward bias: Relatively large diffusion capacitance $C_f$ in shunt with a resistance $R_f$
  较大的扩散电容 $C_f$ 与电阻 $R_f$ 并联
- Reverse bias:
	- Depletion-layer capacitance $C_r$
	  耗尽层电容 $C_r$
	- Series resistance Rs : Accounts for the voltage drop across the bulk material
	  串联电阻 $R_s$：用于计算衬底材料上的电压降
- The switch $S_i$ is closed under forward bias and remains closed initially during reverse bias until the time at which all the charge is extracted from the capacitor $C_f$
  开关 $S_i$ 在正向偏置时闭合，并在反向偏置初始阶段保持闭合，直到电容 $C_f$ 中的所有电荷被提取完毕

- Frequency limits:
	- Lower limit: Time period should be of the order of charge lifetime 
	  下限：周期应与电荷寿命数量级相当$$f_{\text{low}}=\frac{1}{2\pi\tau}$$
	- Upper limit: Transition time $T_t$ should be much less than time period 
	  上限：渡越时间 $T_t$ 应远小于周期$$f_{\text{high}}=\frac{1}{2\pi T_t}$$

- Applications
	- Generation of high order selective harmonics, by using a high Q resonant circuit
	  通过高 Q 谐振电路生成高阶选择性谐波
	- Comb generators, by a low-Q circuit
	  通过低 Q 电路实现梳状发生器
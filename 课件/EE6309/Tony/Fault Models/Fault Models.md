# 基础知识

## Test Process

- The testing problem
  测试问题
	- Given a set of faults in the circuit under test (or device under test), how do we obtain a certain (small) number of test patterns which guarantees a certain (high) fault coverage?
	  在被测电路（或被测设备）中给定一组故障，我们如何获得一定（较少）数量的测试模式，以保证一定（较高）的故障覆盖率？
- Test process
	- What faults to test?
	  测试哪些故障？
		- fault modeling
		  故障建模
	- How are test pattern obtained? 
	  如何获得测试向量？
		- test pattern generation
		  生成测试向量
	- How is test quality (fault coverage) measured?
	  如何衡量测试质量（故障覆盖率）？
		- (fault simulation)
		  故障仿真
	- How are test vectors applied and results evaluated?
	  如何应用测试向量并评估结果
		- ATE/BIST

## Defect Categories

- Defect categories
  缺陷类别
	- Random defects, which are independent of designs and processes
	  随机缺陷，与设计和工艺无关
	- Systematic defects, which depend on designs and processes used for manufacturing
	  系统性缺陷，取决于用于制造的设计和工艺
- For example, random defects might be caused by random particles scattered on a wafer during manufacturing
  例如，随机缺陷可能是由于制造过程中晶圆上散落的随机颗粒造成的

## Logical Fault Models

- Systematic defects might be caused by process variations, signal integrity, and design integrity issues
  系统性缺陷可能由工艺变化、信号完整性和设计完整性问题引起
- It is possible both random and systematic defects could happen on a single die
  在单个Die上，随机缺陷和系统性缺陷都有可能发生
- With the continuous shrinking of feature sizes, somewhere below the 180nm technology node, system defects have a larger impact on yield than random defects
  随着特征尺寸的持续缩小，在 180nm 技术节点以下，系统性缺陷对良率的影响比随机缺陷更大
- Logical faults
  逻辑故障
	- Logical faults represent the physical defects on the behaviors of the systems
	  逻辑故障表示物理缺陷对系统行为的影响

## Why Model Faults

- I/O function tests inadequate for manufacturing (functionality versus component and interconnection testing)
  功能测试对于制造而言不足（功能测试 vs 组件及互连测试）
- Real defects (often mechanical) too numerous and often not analyzable
  真实缺陷（通常是机械性的）数量过多，且往往无法分析
- A fault model identifies targets for testing
  故障模型用于确定测试目标
- A fault model makes analysis possible
  故障模型使分析成为可能
- Effectiveness measurable by experiments
  有效性可通过实验进行衡量

## Fault Nature

- Logical fault
  逻辑故障
	- One that causes the logic function of a circuit element to be changed to some other function
	  使电路元件的逻辑函数改变为其他函数
- Parametric fault
  参数故障
	- One that alters the magnitude of a circuit parameter, causing a change in some factor such as resistance, capacitance, current, etc.
	  改变电路参数大小，导致电阻、电容、电流等因素变化
- Delay fault
  延迟故障
	- One that relates to circuit delays such as slow gates, usually affecting the timing of the circuit, which may cause hazards, or performance degradation, etc
	  一种与电路延迟有关的延迟，如慢门，通常会影响电路的时序，这可能会导致冒险或性能下降等

## Fault Duration

- Permanent fault
	- A lasting fault that is continuous and stable, whose nature does not change before, during, and after testing. E.g., a broken wire, an incorrect bonding, etc.
	- A.k.a hard fault or solid fault
- Temporary fault
	- A fault that is present only part of the time, occurring at random moments and affecting the system for finite, but unknown, intervals of time
	- Transition fault
		- Caused by environmental conditions, e.g., cosmic rays, alpha particle, etc. A.k.a. soft error in RAMs
	- Intermittent fault
		- Caused by non-environmental conditions, e.g., marginal values of component parameters, wear-out, or critical timing
- Permanent fault
  永久性故障
    - A lasting fault that is continuous and stable, whose nature does not change before, during, and after testing. E.g., a broken wire, an incorrect bonding, etc.
      一种持续稳定的故障，其性质在测试前、测试期间和测试后都不会改变。例如，断线、连接错误等。
    - A.k.a hard fault or solid fault
      亦称硬故障或稳定故障
- Temporary fault
  临时性故障
    - A fault that is present only part of the time, occurring at random moments and affecting the system for finite, but unknown, intervals of time
      仅在部分时间内存在的故障，随机发生，并在有限但未知的时间间隔内影响系统
    - Transition fault
      瞬态故障
        - Caused by environmental conditions, e.g., cosmic rays, alpha particle, etc. A.k.a. soft error in RAMs
          由环境条件引起，例如宇宙射线、α粒子等。亦称RAM中的软错误
    - Intermittent fault
      间歇性故障
        - Caused by non-environmental conditions, e.g., marginal values of component parameters, wear-out, or critical timing
          由非环境条件引起，例如元件参数的边缘值、老化或关键时序

## Levels of abstraction in circuits
![[Pasted image 20250430235826.png#pic_50center|]]
- Behavioral description
	- VHDL or Verilog
- Functional description
	- register-transfer level (RTL)
- Structural description
	- Logic level (NAND, NOR, XOR, etc)
- Switch-level description
	- transistor-level details
- Geometric description
	- Layout level

## Fault models at different abstraction

- Fault modeling
  故障建模
    - Process of modeling defects at higher levels of abstraction in the design hierarchy
      在设计层次结构中，以较高抽象层次对缺陷进行建模的过程。
    - Typically the number of faults becomes smaller as we go up in the level of abstraction
      通常，随着抽象层次的提高，故障的数量会减少。
    - A fault at a higher level models many faults at a lower level
      较高层次的故障可以涵盖多个较低层次的故障。
    - Many lower-level faults may remain undetected by this higher-level test set
      许多较低层次的故障可能无法被这一较高层次的测试集合检测到。
    - **A good strategy may be to first derive tests for fault models at higher levels, and then determine what percentage of faults at the lower levels are covered by these tests.**
      **一个较好的策略可能是先为较高层次的故障模型设计测试，然后再确定这些测试能够覆盖多少较低层次的故障。**

## Single Stuck-At Fault

- Single (line) stuck-at fault 单一（线路）固定故障
    - The given line has a constant value (0/1) independent of other signal values in the circuit
      给定线路具有恒定值（0/1），不受电路中其他信号值的影响。
- Properties 性质
    - Only one line is faulty
      仅有一条线路出现故障。
    - The faulty line is permanently set to 0 or 1
      故障线路被永久固定为 0 或 1。
    - The fault can be at an input or output of a gate
      故障可以发生在门电路的输入或输出端。
    - Simple logical model is independent of technology details
      简单的逻辑模型不依赖于技术细节。
    - It reduces the complexity of fault-detection algorithms
      该模型降低了故障检测算法的复杂性。
- One stuck-at fault can model more than one kind of defect
  单一固定故障可以模拟多种缺陷。

![[Pasted image 20250501000337.png#pic_50center|一个例子]]

### Number of Single Stuck-At Faults

- Number of fault sites in a Boolean gate circuit
  布尔逻辑门中故障现场（Fault Site）的个数  $$\# \mathrm{(Fault\ Sites)}=\# \mathrm{PI(Primary\ Input)} + \# \mathrm{Gates} + \# \mathrm{(Fanout\ Branches)}$$
![[Pasted image 20250501000702.png#pic_75center|]]
- Example: XOR circuit has 12 fault sites (•) and 24 single stuck-at faults $$2 + 4 + 6 = 12$$

## Multiple Stuck-At Faults

- Multiple stuck-at fault
  多个固定故障
	- Several single stuck-at faults occur at the same time
	  同时发生多个固定故障
- Multiple stuck-at faults are usually not considered in practice because of two reasons
  由于两个原因，实践中通常不考虑多个固定故障
	- The number of multiple stuck-at faults in a circuit with $k$ lines is $3^k-1$, which is too large a number even for circuits of moderate size
	  在拥有$k$条线路的电路中，多个固定故障的可能性有$3^k-1$，即使对于中等规模的集成电路，这个数字也太大了
	- Tests for single stuck-at faults are known to cover a very high percentage (greater than 99.6%) of multiple stuck-at faults when the circuit is large and has several outputs
	  当电路较大且有多个输出时，单个固定故障的测试覆盖了绝大部分多个固定故障

## Switch-level fault models

- Faults in transistors in a switch-level description of a circuit. This fault model has mostly been used with MOS technologies, specifically CMOS technology. The most prominent members in this category are the stuck-open and stuck-on fault models.

### Stuck-open fault model (SOpF)

![[Pasted image 20250501001351.png#pic_50center]]
- Transistor permanently non-conducting due to some defect
- Assume following sequence: $(x_1 , x_2 ; z) = {(0, 0; 1), (0, 1; 0), (1,0; 0), (1, 1; 0)}$ (z denotes the fault-free value)
  假设以下序列：$(x_1 , x_2 ; z) = {(0, 0; 1), (0, 1; 0), (1,0; 0), (1, 1; 0)}$（z表示无故障值）
- Defect $d_1$ causes an open connection in the gate: SOpF in Q1
  缺陷$d_1$导致门电路出现断开连接：Q1中的SOpF
- When $(x_1 , x_2 ) = (1, 0)$ is applied, no conduction path from z to ${V_{SS}}$ because of the SOpF in Q1. $z$ retains previous value (= 0).
  当施加$(x_1 , x_2 ) = (1, 0)$时，由于Q1中的SOpF，z与${V_{SS}}$之间没有导通路径。$z$保持之前的值（= 0）。
- SOpF test needs a sequence of vectors
  SOpF测试需要一系列向量

### Stuck-on fault model (SOnF)

![[Pasted image 20250501001833.png#pic_50center|]]
- Transistor permanently conducting due to some defect
  晶体管因某些缺陷而永久性导通
- Defect $d_2$ causes an close connection in the gate: SOnF in Q4
  SOnF in Q4 缺陷$d_2$导致门电路出现短路连接：Q4中的SOnF
- The only vector to apply to the NAND gate is $(1, 1; 0)$.
  只有一个向量作用于NAND门：$(1, 1; 0)$
- In the presence of the fault, transistors Q1, Q2 and Q4 will conduct, resulting in some intermediate voltage at the output
  在故障存在的情况下，晶体管Q1、Q2和Q4将导通，导致输出端出现某种中间电压。
- Logic monitoring: output logic value, fast
  监测输出逻辑值，速度快
- Current monitoring: SOnFs, slow
  用于检测SOnF，速度慢

#### 使用电流检测SOnF

- Major problem: may result in unacceptable yield loss
  主要问题：可能导致不可接受的产量损失
![[Pasted image 20250501001939.png#pic_50center|使用电流检测SOnF]]
![[Pasted image 20250501002027.png#pic_75center|]]

## Geometric Fault Model

![[Pasted image 20250501002206.png#pic_75center|]]
- Derived directly from the layout of the circuit
  直接源自电路的Layout
- Exploit the knowledge of line widths, inter-line and intercomponent distances, and device geometries to determine what defects are most likely
  利用对线宽、线间及器件间距以及器件几何结构的了解，以确定最可能出现的缺陷。
- Bridging faults (BFs): percentage of defects causing shorts
  引发短路的缺陷比例
- Wired-AND: two lines result in an AND function
  两根线最终形成一个等效的AND门
- Wired-OR: two lines result in an OR function
  两根线最终形成一个等效的OR门

### 例子

![[Pasted image 20250501002405.png#pic_75center|]]
- Example: consider the short between $C_1$ and $C_2$ .
	- For $(x_1 , x_2 ,x_3) = (1, 1, 0)$ there is a path from $V_{DD}$ to $V_{SS}$
	- This will result in an intermediate voltage at the shorted nodes.
	- This can be easily detected by current monitoring
  示例：考虑$C_1$和$C_2$之间的短路。
	- 当$(x_1 , x_2 ,x_3) = (1, 1, 0)$时，存在一条从$V_{DD}$到$V_{SS}$的路径。
	- 这将在短路节点处产生某种中间电压。
	- 该故障可以通过电流监测轻松检测到。

## Bridging Faults


- Bridging fault
	- Two or more normally distinct points (lines) are shorted together
	  两个或多个通常相互独立的点（线路）被短接在一起

![[Pasted image 20250501002636.png#pic_75center|]]
![[Pasted image 20250501002814.png#pic_75center|]]
- Two types of bridging faults
	- Input bridging
		- Can form wired logic or voting model
		  可形成有线逻辑或投票模型
	- Feedback (input-to-output) bridging
		- Can introduce feedback
		  可引入反馈
		- Can cause oscillation or latching (additional memory)
		  可能导致振荡或锁存（额外的存储器）

## Pattern-Sensitive Faults

![[Pasted image 20250501002912.png#pic_50center|]]

- Pattern-sensitive fault
	- The presence of a faulty signal depends on signal values of nearby points
	  故障信号的存在取决于附近点的信号值
	- Most common in DRAM (dynamic random access memory)
- Coupling fault
	- Pattern sensitivity between a pair of cells
	  在一对存储单元之间存在图案的敏感性

## Single Cell Fault

![[Pasted image 20250501003109.png#pic_50center|]]
- Cells can have any implementation
  单元可以采用任何实现方式
- All possible (combinational) cell faults are allowed; truth table can change in any way
  所有可能的（组合）单元故障都被允许；真值表可以以任何方式变化
- C-testability: constant number of test patterns, independent of circuit size (Ripple-carry adder needs only 8 test patterns for all single stuck-at faults)
  C-可测试性：测试模式数量恒定，与电路规模无关（对于所有单一固定故障，波纹进位加法器仅需要8个测试模式）

## Delay Fault Model

![[Pasted image 20250501003843.png#pic_75center|]]

- Delay fault
	- Propagation delays along a path (gate) fall outside the desired limits.
	  沿着一条路径（门）的传播延时高于预期限制
	- Two types of delay faults:
		- path delay fault
		- gate delay fault

- Instead of affecting the logical behavior of the circuit, a fault may affect its temporal behavior only
  并非影响电路的逻辑行为，故障可能仅影响其时间行为
- Gate delay fault (GDF): an input or output of the gate has a lumped DF manifested as a slow $0 \rightarrow 1$ or $1 \rightarrow 0$ transition
  门延迟故障（GDF）：门电路的输入或输出发生集中故障，表现为缓慢的$0 \rightarrow 1$或$1 \rightarrow 0$跳变
	- Gross gate delay fault (G-GDF): delay defect > clock period, catastrophic
	  严重门延迟故障（G-GDF）：延迟缺陷大于时钟周期，影响严重
	- Small gate delay fault (S-GDF): delay defect < clock period, a temporal failure in at least one path, two tests for each path for detection
	  轻微门延迟故障（S-GDF）：延迟缺陷小于时钟周期，至少影响一条路径，需要针对每条路径进行两次测试以检测故障。
- Path delay fault (PDF): there exists a path which is slow to propagate a $0 \rightarrow 1$ or $1 \rightarrow 0$ transition
  路径延迟故障（PDF）：存在一条路径，其传播$0 \rightarrow 1$或$1 \rightarrow 0$跳变的速度较慢

- Hazard-free robust test (HFRT): no hazard can occur on the tested path regardless of the gate delay values
  无论门延迟值如何，测试路径上都不会发生冒险
- Non-hazard-free robust test: hazards along the tested path
  冒险沿着测试路径
- Multiple-path propagating (MPP): a DF test propagates the transition through more than one path to the output
  DF测试通过多条路径将跳变传播到输出
- Single-path propagating (SPP): the transition propagation is done through a single path
  过渡传播是通过单路径完成的
- Single-input change (SIC): from the initialization vector to the test vector, only one input changes
  从初始化向量到测试向量，只有一个输入更改
- Multi-input change (MIC): from the initialization vector to the test vector, multiple inputs change
  从初始化向量到测试向量，多输入变化

### Transition delay fault

- A gate output may be slow-to-rise or slow-to-fall and that this time is longer than a predefined level
  逻辑门输出可能上升缓慢或下降缓慢，并且这段时间长于预期的水平
- If the delay fault is large enough, the transition delay fault behaves as a SAF and can be modelled using that method
  如果延迟故障足够大，则转换延迟故障表现为SAF（Stuck-At Fault），可以使用该方法进行建模
- The primary weakness of transition delay fault
	- Two pattern sequences for initialization and transition detection are needed
	  需要两个测试向量用于初始化和转换检测
	- The minimum achievable delay fault size is difficult to determine because of timing hazards. Consequently, a whole mission clock cycle is usually used
	  由于时序冒险，很难确定可实现的最小延迟故障大小。因此，通常使用整个任务时钟周期

## Crosstalk Defects

![[Pasted image 20250501004147.png#pic_75center|]]
- Wire aspect scaling with technology
  利用技术实现导线尺寸缩放
- Capacitive crosstalk noise results from parasitic coupling between two signal nets
  电容串扰噪声是由两个信号网络之间的寄生耦合引起的

### Maximal Aggressor Fault Model

![[Pasted image 20250501004243.png#pic_75center|]]

# Test & Test Set

- A test for a fault $\alpha$ in a circuit $C$ is an input combination for which the output(s) of $C$ is different when $\alpha$ is present than when it is not.
  测试电路 $C$ 中的故障 $\alpha$ ：用一个输入组合，使得当 $\alpha$ 存在时，$C$ 的输出与 $\alpha$ 不存在时不同。
	- A.k.a. test pattern or test vector
	  亦称测试模式或测试向量
	- $X$ detect $\alpha$ then $$f(X)\oplus f_{\alpha}(X)=1$$
- A test set for a class of faults $A$ is a set of tests $T$ such that
  对于一类故障 $A$，其测试集 $T$ 是一组测试，使得$$\forall\alpha\in A,\ \exists t \in T$$and $T$ detects $\alpha$
  并且$T$能够检测$\alpha$
	- The test set for a fault $\alpha$ is $T_{\alpha}=f\oplus f_\alpha$ (Boolean Difference)

# Testing & Diagnosis

- Testing is a process which includes test pattern generation, test pattern application, and output evaluation.
  测试是一个过程，包括测试模式生成、测试模式应用和输出评估
- Fault detection tells whether a circuit is fault-free or not
  故障检测用于判断电路是否无故障
- Fault location provides the location of the detected fault
  故障定位提供检测到的故障的位置
- Fault diagnosis provides the location and the type of the detected fault
  故障诊断提供检测到的故障的位置和类型

## 例子

![[Pasted image 20250501005144.png#pic_75center|]]
- $C_{a/0}$ and $C_{c/0}$ are detected by the test pattern $(1,0)$
  通过测试模式 $(1,0)$ 可以检测到故障 ${a/0}$ 和 ${c/0}$
- If we apply two test patterns: $(1,0)$ & $(0, 1)$
  如果应用两个测试向量 $(1,0)$ 和 $(0,1)$
	- Two corresponding outputs are faulty→${c/0}$
	  两个对应的输出均出现故障 → ${c/0}$
	- Only the output with respect to the input $(1,0)$ is faulty→${a/0}$
	  仅与输入 $(1,0)$ 相关的输出出现故障 → ${a/0}$

## 练习
#TODO
![[Pasted image 20250501005548.png#pic_75center|]]
1. List the faults of this circuit without the equivalence and dominance collapsing techniques
   $\# \mathrm{PI}=5$, $\# \mathrm{Gate}=5$, $\# \mathrm{Fanout Branches}=2$, 所以总共的Fault Site有12个，总共24种故障（见图）
2. Derive a test set for detecting S/0 at F.
   正常的输出布尔表达式为：$$Z=A\cdot B+C+D+\overline{C+D}\cdot E$$存在$F_{S/0}$时的输出表达式为：$$Z_{F/0}=A\cdot B+E$$用后面的知识生成测试向量：

# Fault Collapsing

- To generate tests for digital circuits, the test tools are provided with a circuit description, a netlist. The tool then creates a list of all faults (fault list) to be detected
  为了为数字电路生成测试，测试工具需要提供电路描述，即网表。然后，该工具会创建需要检测的所有故障列表（故障列表）
- For large circuits, the list can be quite long. It is thus beneficial to minimize the list whenever possible
  对于大型电路，该列表可能会非常长，因此尽可能缩短列表是有益的
- Some faults may be detected by the same test patterns. Therefore, only one of these faults needs to be included in the fault list
  一些故障可能可以通过相同的测试模式检测到，因此故障列表中只需要包含其中一个故障
- Fault collapsing can reduce the size of fault list with two concepts: equivalence and dominance
  故障折叠可以通过两个概念来减少故障列表的大小：**等价**和**支配**

## Equivalent Fault Collapsing

![[Pasted image 20250501022748.png#pic_75center|]]
- Definition
	- Two faults are called equivalent if every pattern that detects one of the faults also detects the other. That is, their test sets, T1 and T2, are identical:
	  两个故障称为等价故障，如果检测其中一个故障的每个测试模式也能够检测另一个故障。换句话说，它们的测试集 $T_1$ 和 $T_2$ 是相同的
	- Summary
		- AND gate: all s/0 faults are equivalent
		  对于 **AND** 门，所有 **s/0** 故障都是等价的
		- OR gate: all s/1 faults are equivalent
		  对于 **OR** 门，所有 **s/1** 故障都是等价的
		- For an n-input gate, only n+2 faults need to be considered with equivalence fault collapsing
		  对于 **n 输入门**，在进行等价故障压缩时，仅需考虑 **n+2** 个故障

![[Pasted image 20250501023620.png#pic_75center|]]
- 从《数字系统测试和可测试性设计》总结：
	- 逻辑门的等价故障被称为一个浮动故障。那么故障中总共包含了$(n+1)+1$种故障，其中$(n+1)$表示输入有$n$个SA故障，输出有1个SA故障。而等效故障中的浮动故障能够位于任意一个端口上。
	- 对于与门或者或门来说，这个浮动故障（等效故障）在任何端口都是一致的（比如与门都是SA0，或门都是SA1），但对于或非门或者与非门来说，由于输出带有非，所以这个浮动故障（等效故障）在输入与输出端口的行为并不一致，简单来说就是如果在输出端口，那么就相对正常的与门或者或门反一下。

![[Pasted image 20250501023520.png#pic_75center|]]
- Fault equivalent diagrams for primitive logic gates
  从中也能看到等效故障（浮动故障）在NOR门与OR门中不同的行为（输出故障类型相反）

![[Pasted image 20250501023716.png#pic_75center|一个例子]]

## Dominance Fault Collapsing

- Definition
	- A fault, $f_1$, dominates another fault, $f_2$, if the test set of the latter, $T_2$, is a subset of the test set of the former, $T_1$; that is, $T_2 \subseteq T_1$. Any test pattern that detects $f_2$ will also detect $f_1$. Therefore, $f_2$ implies $f_1$ and it is sufficient to include $f_2$ in the fault list
	  如果故障 $f_1$ **支配** 另一个故障 $f_2$，则后者的测试集 $T_2$ 是前者的测试集 $T_1$ 的子集，即 $T_2 \subseteq T_1$。任何能够检测到故障 $f_2$ 的测试模式也会检测到故障 $f_1$。因此，故障 $f_2$ **隐含** 故障 $f_1$，只需在故障列表中包含 $f_2$ 即可。
	  互相包含的两个测试集只需要取小的那个就能完成一样的工作
	- Consider a two-input (A and B) AND gate, a test pattern for the S/1 fault on any of the inputs detects S/1 fault on the output (C). Then C/1 can be dropped from the fault list. Therefore, the fault list is reduced to {A/0,A/1,B/1}
	  在一个具有两个输入（A 和 B）的 **AND** 门中，针对任一输入上的 **S/1** 故障的测试模式同样能够检测到输出（C）上的 **S/1** 故障。因此，**C/1** 可以从故障列表中移除。最终，故障列表被简化为 **{A/0, A/1, B/1}**。
- Summary
	- For an n-input AND gate, $I_{n+1}/1$ dominates $I_{i}/1\forall i$
	- For an n-input OR gate, $I_{n+1}/0$ dominates $I_i/0\forall i$
- 例子，假设一个与门$C=AB$：
	- 要检测$A/1$故障，测试向量集合$T_1$为：$$\left\{\binom{A}{B}\right\}=\left\{\binom{0}{1}\right\}$$
	- 要检测$C/1$故障，测试向量集合$T_2$为：$$\left\{\binom{A}{B}\right\}=\left\{\binom{0}{0}，\binom{0}{1}，\binom{1}{0}\right\}$$
	- 所以我们仅需使用$T_1$就能同时检测到$A/1$和$C/1$故障，但这二者并不等价，这意味着我们无法使用测试集$T_2$来检测$A/1$故障（有两个向量不能用）


![[Pasted image 20250501025050.png#pic_75center|]]
- Add directed arcs from the dominating faults toward the dominated faults

![[Pasted image 20250501025131.png#pic_75center|]]
- For fanouts, view the stem and branch as a separate line. Direction of dominance is opposite that of the gates
  对于扇出结构，可以将干线和分支视为独立的线路。支配关系的方向与门电路的方向相反。
	- 这一块烧脑袋一点，因为扇出后故障的传递可能被后续电路屏蔽，所以是输入支配输出。
	- 感性理解：分支的故障由于被屏蔽了，所以测试向量要更刁钻，所以测试向量数量会更少，自然是没被屏蔽的干线故障测试向量更多。
	- 一个例子：假设输入$S$被扇出为$(A,B)$，后续的逻辑功能可以表示为$$Z=AX+B$$那么要检测$S/1$故障，测试向量集合为：$$\left\{\binom{S}{X}\right\}=\left\{\binom{0}{0},\binom{0}{1}\right\}$$要检测$A/1$故障，测试向量集合为：$$\left\{\binom{S}{X}\right\}=\left\{\binom{0}{1}\right\}$$所以$S/1$支配了$A/1$

# Test Compaction

- Equivalence fault collapsing + dominance fault collapsing
	- Only $n+1$ faults on any n-input gate need be considered
	  对于 n 输入门，仅需考虑 n+1 个故障
- Definition
	- Test compaction refers to the process of reducing the number of test patterns in a test set without reducing its fault coverage
	  测试压缩指在不减少故障覆盖率的情况下减少测试集中的测试模式数量。
	- Equivalence fault collapsing and dominance fault collapsing can be used to aid test compaction
	  等价故障折叠和支配故障折叠可用于帮助测试压缩。
- Theorem
	- In a fanout-free combinational circuit, any test set which detects all stuck faults on primary inputs will detect all stuck at faults
	  在无扇出组合电路中，任何能检测所有Primary Inputs（PI）上的SA故障的测试集，也能检测所有SA故障

---

![[Pasted image 20250501032708.png#pic_75center|]]
- The set of all primary inputs and all fanout branches are called checkpoints of the circuit
  所有主输入和所有扇出分支的集合称为电路的检查点
- Theorem
	- In a combinational circuit, any test set which detects all single (multiple) stuck faults on checkpoints will detect all single (multiple) stuck faults.
	  在组合电路中，任何能够检测所有检查点上的单个（或多个）SA故障的测试集，也能够检测所有单个（或多个）SA故障。

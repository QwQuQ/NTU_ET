
- A fault is testable if there exists a well-specified procedure to expose it, which is implementable with a reasonable cost using current technologies. A circuit is testable with respect to a fault set when each and every fault in this set is testable.
  如果存在一种明确定义的程序可以暴露故障，并且能够以当前技术在合理成本范围内实现，则该故障是可测试的。一个电路在给定的故障集合下是可测试的，当且仅当该集合中的每一个故障都是可测试的。
- Design for testability (DFT) refers to those design techniques that make test generation and test application cost-effective.
  可测试性设计（DFT）指的是使测试生成和测试应用成本有效的那些设计技术
- Electronic systems contain three types of components:
  电子系统包含三种类型的组件
	- digital logic
	  数字逻辑
	- memory blocks
	  存储块
	- analog or mixedsignal circuits.
	  模拟或混合信号电路  

# Important Factors of Testability

- Controllability: Measure the ease of controlling a line.
  可控性：衡量控制一条线路的难易程度
- Observability: Measure the ease of observing a line at a PO
  可观察性：衡量在输出端观察一条线路的难易程度
- In general, DFT deals with ways for improving controllability and observability
  通常，DFT涉及提高可控性和可观察性的方法

# Cost Associated with DFT

- Pins
- Area/Yield
- Performance
- Design Time

# Ad Hoc DFT

## Ad Hoc DFT Guidelines
*特定点测试*

![[Pasted image 20250501220109.png#pic_50center|]]
![[Pasted image 20250501220209.png#pic_50center|]]
- Partition large circuits into smaller subcircuits to reduce test generation cost (using MUXed and/or scan chains)
  将大型电路划分为较小的子电路，以降低测试生成成本（使用多路复用和/或扫描链）
- Insert test points to enhance controllability & observability
  插入测试点以增强可控性和可观察性
	- Test points: control points & observation points
	  测试点：控制点和观察点

- Design circuits to be easily initializable
  设计电路以便于初始化
- Provide logic to break global feedback paths
  提供逻辑以打破全局反馈路径
- Partition large counter into smaller ones
  将大型计数器划分为较小的计数器
- Avoid the use of redundant logic
  避免使用冗余逻辑
- Keep analog and digital circuits physically apart
  使模拟电路和数字电路在物理上保持分离
- Avoid the use of asynchronous logic
  避免使用异步逻辑
- Consider tester requirements (pin limitation, etc)
  考虑测试设备的要求（引脚限制等）

## Problems in Ad Hoc DFT

- Large number of I/O pins
  大量 I/O 引脚
	- Add MUX’s to reduce number of I/O pins
	  添加 MUX 以减少 I/O 引脚数量
	- Serially shifts control point values
	  串行移位控制点值
- Long testing time
  测试时间长

# Scan Design Approaches

- They are effective for circuit partitioning
  它们对于电路分区非常有效
- They provide controllability and observability of internal state variables for testing
  它们为测试提供了对内部状态变量的可控性和可观察性
- They turn the sequential test problem into a combinational one
  它们将顺序测试问题转化为组合测试问题
- Four major approaches
	- Shift-register modification
	  移位寄存器修改
	- Scan path
	  扫描路径
	- Level-sensitive scan design (LSSD)
	  电平敏感扫描设计（LSSD）
	- Random access
	  随机访问
- Circuit is designed using pre-specified design rules.
  电路是按照预先指定的设计规则进行设计的

![[Pasted image 20250502021653.png#pic_75center|]]
- Consider a representation of sequential circuits
  考虑如图的时序电路表示

![[Pasted image 20250502021725.png#pic_75center|]]
- To make elements of state vector controllable and observable, we add
  为了使状态向量的元素可控和可观察，我们添加
	- A TEST mode pin (T)
	  一个测试模式引脚
	- A SCAN-IN pin (SI)
	  一个扫描输入引脚
	- A SCAN-OUT pin (SO)
	  一个扫描输出引脚
	- A MUX (switch) in front of each FF (M)
	  每个触发器（FF）前的多路复用器

# Scan Test Generation & Design Rules

- Test pattern generation
  测试模式生成
	- Use combinational ATPG to obtain tests for all testable faults in the combinational logic
	  使用组合 ATPG 以获取组合逻辑中所有可测试故障的测试
	- Add shift register tests and convert ATPG tests into scan sequences for use in manufacturing test
	  添加移位寄存器测试，并将 ATPG 测试转换为扫描序列，以用于制造测试
- Scan design rules
  扫描设计规则
	- Use only clocked D-type of flip-flops for all state variables
	  所有状态变量仅使用时钟驱动的 D 触发器
	- At least one PI pin must be available for test; more pins, if available, can be used
	  至少需要一个 PI 引脚可用于测试；如果有更多可用引脚，则可以使用
	- All clocks must be controlled from PIs![[Pasted image 20250502022058.png#pic_33center|All clocks must be controlled from PIs]]
	  所有时钟必须由 PI 控制
	- Clocks must not feed data inputs of flip-flops
	  时钟不得为触发器的数据输入提供信号

## Correcting a Rule Violation

- Adding a scan FF and a mux allows a feedback loop to be opened for testing![[Pasted image 20250502022307.png#pic_50center|]]
  添加扫描触发器（FF）和多路复用器（MUX）允许打开反馈回路进行测试
- Testing derived clocks requires the use of a mux to bypass the division stages![[Pasted image 20250502022327.png#pic_50center|]]
  测试派生时钟需要使用多路复用器绕过分频阶段（测试用时钟可能很低，不需要额外分频）
- The AND gates keep the bus drivers from being activated by the normal logic during testing![[Pasted image 20250502022421.png#pic_50center|]]
  AND 门在测试过程中防止总线驱动器被正常逻辑激活

# Scan Test Procedure

- Step 1: Switch to the shift-register mode and check the SR operation by shifting in an alternating sequence of 1s and 0s, e.g., 00110 (functional test)
  步骤 1：切换到移位寄存器（SR）模式，并通过移入交替序列的 1 和 0（例如 00110）检查 SR 操作（功能测试）
- Step 2: Initialize the SR---load the first pattern
  步骤 2：初始化 SR——加载第一个模式
- Step 3: Return to the normal mode and apply the test pattern
  步骤 3：返回正常模式并应用测试模式
- Step 4: Switch to the SR mode and shift out the final state while setting the starting state for the next test. Go to Step 3
  步骤 4：切换到 SR 模式，移出最终状态，同时设置下一次测试的起始状态。然后返回步骤 3

# Combining Test Vectors

![[Pasted image 20250502022622.png#pic_50center|]]
![[Pasted image 20250502022646.png#pic_50center|]]
- 时序逻辑电路中，组合逻辑的输入可能有PI和状态输入，测试时需要产生PI和状态输入。状态输入由于是寄存器，所以通过移位输入

# Testing Scan Register

- Scan register must be tested prior to application of scan test sequences
  在应用扫描测试序列之前，必须先测试扫描寄存器
- A shift sequence 00110011 . . . of length $n_{sff}+4$ in scan mode (TC=0) produces 00, 01, 11 and 10 transitions in all flip-flops and observes the result at SCAN-OUT output
  在扫描模式（TC=0）下，长度为 $n_{sff}+4$ 的移位序列 00110011… 在所有触发器中产生 00、01、11 和 10 变化，并在 SCAN-OUT 输出端观察结果
- Example: 2,000 scan flip-flops, 500 comb. vectors, total scan test length ~ $10^6$ clocks
  示例：2,000 个扫描触发器，500 个组合向量，总扫描测试长度约为 $10^6$ 个时钟周期
- Multiple scan registers reduce test length
  多个扫描寄存器可减少测试长度

## Multiple Scan Registers

![[Pasted image 20250502023817.png#pic_50center|]]
- Scan flip-flops can be distributed among any number of shift registers, each having a separate SCAN-IN and SCAN-OUT pin
  扫描触发器可以分布在任意数量的移位寄存器中，每个寄存器都有单独的 SCAN-IN 和 SCAN-OUT 引脚
- Test sequence length is determined by the longest scan shift register
  测试序列长度由最长的扫描移位寄存器决定
- Just one test control (TC) pin is essential
  只需要一个测试控制（TC）引脚

# Hierarchical Scan

![[Pasted image 20250502023917.png#pic_75center|]]
- Scan flip-flops are chained within subnetworks before chaining subnetworks
  扫描触发器在子网络内部进行串联，然后再串联子网络
- Advantages:
	- Automatic scan insertion in netlist
	  在网表中自动插入扫描
	- Circuit hierarchy preserved – helps in debugging and design changes
	  保持电路层次结构，有助于调试和设计更改
- Disadvantage:
	- Non-optimum chip layout
	  芯片布局非最优

## Optimum Scan Layout

![[Pasted image 20250502024007.png#pic_75center|]]

# Automated Scan Design

![[Pasted image 20250502024430.png#pic_75center|]]

# An Example of DFT Compiler Flow

![[Pasted image 20250502024539.png#pic_75center|]]

# Shift Registers

![[Pasted image 20250502024556.png#pic_75center|]]
- 直接加入扫描触发器容易造成冗余电路，所以可以改良以消除冗余电路

# Random Access Scan

![[Pasted image 20250502024907.png#pic_75center|]]
- Uses addressable latches
  用可以寻址的触发器
- Provides random access to FFs via multiplexin
  通过多路复用器实现对触发器（FF）的随机访问
	- address selection

- Random access scan cell
  随机访问扫描单元 *不要记* ![[Pasted image 20250502025120.png#pic_50center|]]
- Advantages
	- Fast; minimal impact on normal path
	  快速；对正常路径影响最小
	- Fast for testing—random access
	  测试速度快——随机访问
	- Ability to ‘watch’ a node in normal operation mode
	  能够在正常运行模式下“观察”节点
- Disadvantages
	- Hardware cost is large; more pins added
	  能够在正常运行模式下“观察”节点

## Random Access Architecture

*需要增加很多额外的电路，结构有点像DRAM*
![[Pasted image 20250502025520.png#pic_75center|]]
- During normal operation the storage cells operate in their parallel-load mode
  在正常运行期间，存储单元以并行加载模式运行
- To scan in a bit, the appropriate cell is addressed, the data are applied to $s_{\text{in}}$
  要扫描一个位，需要寻址相应的存储单元，并将数据应用到 $s_{\text{in}}$

### Test Procedure

- Set test input to all test points
  将测试输入设置为所有测试点
- Apply the master reset signal to initialize all memory elements
  施加主复位信号以初始化所有存储单元
- Set scan-in address and data, and then apply the scan clock
  设置扫描输入地址和数据，然后施加扫描时钟
- Repeat step 3 until all internal test inputs are scanned in
  重复步骤 3，直到所有内部测试输入都被扫描
- Clock once for normal operation
  正常运行一个时钟周期
- Check states of the output points
  检查输出点的状态
- Read the scan-out states of all memory elements by applying appropriate X-Y signals
  通过施加适当的 X-Y 信号读取所有存储单元的扫描输出状态

#  Scan-Hold FFs (SHFFs)

![[Pasted image 20250502025741.png#pic_50center|]]
- $\text{HOLD}=0 \to Q \& Q^\prime$ are fixed
- The control input HOLD keeps the output steady at previous state of flip-flop
  控制输入 HOLD 使输出保持在触发器的先前状态
- Applications
	- Reduce power dissipation during scan, etc.
	  在扫描过程中降低功耗等

# Scan Enters the Nanometer Era

![[Pasted image 20250502025905.png#pic_33center|]]
- Trend in flip flop count with design size
  触发器数量随设计规模的趋势
- Adaptive scan architecture is required
  需要自适应扫描架构

# Problems with Full Scan

- Area overhead
  面积开销
	- Due to larger flip-flops
	  由于较大的触发器
	- Due to extra routing
	  由于额外的布线
- Possible performance degradation
  可能的性能下降
	- Extra gate delay due to the multiplexer
	  由于多路复用器造成的额外门延迟
	- Extra capacitive loading delay due to scan wiring at the flip-flop output
	  由于触发器输出端的扫描布线造成的额外电容负载延迟
- Long test application time
  测试应用时间长
- Not applicable to all designs (e.g. asynchronous designs, designs violating scan design rules)
  并非适用于所有设计（例如异步设计、违反扫描设计规则的设计）
- High power dissipation during testing
  测试过程中功耗高

# Issues for Multiple-Clock Design

- Clock skew might occur between different domains
  在不同的时钟域之间可能会发生时钟偏移
- To minimize skew during scan shift, scan chains should be ordered.
  为了在扫描移位过程中最小化时钟偏移，应对扫描链进行排序
- All FFs in same clock domain are grouped together
  归类相同时钟域中的所有触发器（FF）
	- minimizing locations where clock skew can occur
	  以最小化时钟偏移可能发生的位置
- To completely avoid skew where the scan/clock domains cross, a lockup latch can be inserted.
  为了完全避免扫描/时钟域交叉处的时钟偏移，可以插入锁存锁

# General Issues of Scan Design

- Scan chain ordering
  扫描链排序
	- To prevent skew during shift
	  防止移位过程中出现时钟偏移
	- To minimize routing overhead
	  最小化布线开销
	- Use placement info to determine a good ordering
	  使用布局信息来确定最佳排序
- Balancing scan chains
	- To minimize total test time
	  以最小化总测试时间
	- $\text{Total scan cycles} = (\text{Scan patterns} +1)\times (\text{Length of longest scan chains})$
	  $\text{总扫描周期} = (\text{测试向量} +1) \times (\text{最长扫描链的长度})$
	- Number of scan chains is normally limited by the package (pins available to borrow or dedicate for scan) as well as the tester (channels available with memory depth that can handle scan vectors).
	  扫描链的数量通常受封装限制（可用于扫描的引脚数量）以及测试设备限制（具有足够内存深度以处理扫描向量的可用通道）

# Partial Scan

- Basic idea
	- Select a subset of flip-flops for scan
	  选择一部分触发器进行扫描
	- Lower overhead (area and speed)
	  降低开销（面积和速度）
	- Relaxed design rules
	  放宽设计规则
- Cycle-breaking technique
  断环技术
	- Cheng & Agrawal, IEEE Trans. on Computers, 1990
	- Select scan flip-flops to simplify sequential ATPG
	  选择扫描触发器以简化顺序 ATPG
- Timing-driven partial scan
  以时间驱动的部分扫描
	- Jou & Cheng, ICCAD, Nov. 1991
	- Allow optimization of area, timing and testability simultaneously
	  允许同时优化面积、时序和可测试性

# Practice: Scan Chain Reordering

![[Pasted image 20250502031012.png#pic_50center|]]

# Practice: Scan Test

- Convert the circuit by adding scan to the three flip-flops. Create a complete scan test for the indicated faults ($\alpha$, $\beta$, $\gamma$). Show the sequence of test vectors that are applied to this circuit in order to detect the faults, and show the sequence required to scan out and observe the results.
  转换电路，通过向三个触发器添加扫描功能。为所指示的故障 ($\alpha$, $\beta$, $\gamma$) 创建完整的扫描测试。展示应用于该电路的测试向量序列，以检测故障，并展示扫描输出和观察结果所需的序列。
![[Pasted image 20250502031241.png#pic_75center|]]

# Syndrome-Testable Design

我们只检查输出的关键特征
- Definition
	- The syndrome of a Boolean function is
	  布尔函数的特征值定义为（输出值中1的比例）： $$S(f)\equiv \frac{k(f)}{2^n}$$where
		- $k$ is the number of 1s (minterms) in $f$
		  $k$ 是函数 $f$ 中 1（最小项）的数量
		- $n$ is the number of independent input variables
		  $n$ 是独立输入变量的数量
	- A typical syndrome testing set-up![[Pasted image 20250502031640.png#pic_50center|]]
	  一个典型的特征值测试设置
		- $0\leq S(f)\leq 1$
		- A circuit is syndrome testable iff $\forall \text{fault} \alpha,\ S(f)\neq S(f_\alpha)$
		  当且仅当对于所有故障 $\alpha$，$S(f)\neq S(f_\alpha)$ 时，电路是特征值可测试的
		- Syndromes of logic gates![[Pasted image 20250502031837.png]]
		  逻辑门的特征值

## Syndrome Computation

- Consider a circuit having 2 blocks, $f$ and $g$, with unshared inputs![[Pasted image 20250502031943.png]]
  一个电路有两个模块，输入互不共享，特征值如图
- Example
	- Calculate the syndrome of the following circuit![[Pasted image 20250502031949.png]]
	  电路的输出特征值

## Syndrome-Testable Design

- Consider the function $f = xz + yz^\prime$. The circuit is syndrome untestablez $$S(f) = 1/2$$
	- If the circuit has a fault $\alpha \equiv z/0$, then the corresponding syndrome of the faulty circuit is 
	  如果电路存在故障 $\alpha \equiv z/0$，则故障电路的特征值为$$S^\prime(f)=1/2$$
	- Thus the circuit is syndrome untestable
	  因此，该电路在不可测试特征值
- A realization $C$ of a function $f$ is said to be syndrome-testable if no single stuck-at fault causes the circuit to have the same syndrome as the faultfree circuit
  如果没有单一的“固定故障”（stuck-at fault）会导致电路的特征值与无故障电路的特征值相同，这个实现 $C$ 被称为可测试特征值的
- Syndrome is a property of function, not of implementation
  特征值是函数的属性，而不是具体实现的属性

- **Unate** Definition
	- A logic function is unate in a variable $x_i$ if it can be represented as an SOP or POS expression in which the variable $x_i$ appears either only in an uncomplemented form or only in a complemented form
	  如果一个逻辑函数在变量$x_i$上是单调的，则它可以表示为与或表达式（SOP）或或与表达式（POS），其中变量$x_i$仅以未补形式或仅以补形式出现。
- For example:![[Pasted image 20250502032620.png#pic_75center|]]
- Theorem
	- A 2-level irredundant circuit realizing a unate function in all its variables is syndrome testable
	  一个实现单调函数且所有变量均无冗余的两级电路是特征值可测试的 *要证明这玩意极其困难，不学，后面略*

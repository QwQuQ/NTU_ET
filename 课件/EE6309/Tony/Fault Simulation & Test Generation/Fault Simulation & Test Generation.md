# 建议自己阅读的部分（上课跳过了）
## Simulation

- Definition
	- Simulation refers to modeling of a design, its function and performance.
	  仿真指的是对设计、其功能和性能进行建模。
- A software simulator is a computer program; an emulator is a hardware simulator
  软件模拟器是计算机程序，仿真器是硬件模拟器。
- Simulator is used for design verification
  模拟器用于设计验证
	- Validate assumptions
	  验证假设
	- Verify logic
	  验证逻辑
	- Verify performance (timing)
	  验证性能（时序）

## Level of Simulation

![[Pasted image 20250501034657.png#pic_50center|]]

- System level
- Architecture level
- Functional level/RTL level
- Gate/structural level
- Switch/transistor/circuit level
- Mixed level

## Simulation Process

![[Pasted image 20250501034708.png#pic_50center|]]

## Modeling

- Modules, blocks or components described by
  模块、块或组件的描述包括
	- Input/output (I/O) function
	  输入/输出（I/O）功能
	- Delays associated with I/O signals
	  与 I/O 信号相关的延迟
	- Examples: binary adder, Boolean gate, etc.
	  示例：二进制加法器、布尔门等
- Interconnects represent
  互连表示
	- Ideal signal carriers or ideal electrical conductors
	  理想信号载体或理想电导体
- Netlist
  网表
	- A format (or language) that describes a design as an interconnection of modules. Netlist may use hierarchy
	  一种用于描述设计的格式（或语言），表示模块之间的互连关系。网表可以使用层次结构。

### Example: Full-Adder Netlists

![[Pasted image 20250501034728.png#pic_75center|]]

## Types of Simulation

- Compiled simulation
  编译仿真
	- Applicable to zero-delay combinational logic
	  适用于零延迟的组合逻辑
	- Also used for cycle-accurate synchronous sequential circuits for logic verification
	  也用于周期精确的同步时序电路逻辑验证
	- Efficient for highly active circuits, but inefficient for low-activity circuits
	  对于高活动电路效率高，但对于低活动电路效率低
	- High-level (e.g., C language) models can be used
	  可使用高级（例如 C 语言）模型
- Event-driven simulation
  事件驱动仿真
	- Only gates or modules with input events are evaluated (event means a signal change)
	  仅评估具有输入事件的门或模块（事件指信号变化）
	- Delays can be accurately simulated for timing verification
	  可精确模拟延迟以进行时序验证
	- Efficient for low-activity circuits
	  对于低活动电路效率高
	- Can be extended for fault simulation
	  可扩展用于故障仿真

## Compiled Simulation

- Step 1:
	- Levelize combinational logic and encode in a compilable programming language
	  对组合逻辑进行分级，并使用可编译的编程语言进行编码
- Step 2:
	- Initialize internal state variables (flip-flops)
	  初始化内部状态变量（触发器）
- Step 3:
	- For each input vector
	  对每个输入向量执行以下操作
	- Set primary input variables
	  设置主输入（PI）变量
	- Repeat (until steady-state or max. iterations)
	  重复执行（直到达到稳态或最大迭代次数）
		- Execute compiled code
		  执行编译后的代码
	- Report or save computed variables
	  记录或保存计算出的变量

## Event-Driven Simulation

![[Pasted image 20250501034757.png#pic_75center|]]
- 这张图中考虑了延时导致的影响

### Efficiency of Event-Driven Simulator

![[Pasted image 20250501034814.png#pic_75center|]]

- Simulates events (value changes) only
  仅模拟事件（值变化）
- Speed up over compiled-code can be ten times or more; in large logic circuits about 0.1 to 10% gates become active for an input change
  相较于编译代码，速度可提升10倍或更多；在大型逻辑电路中，每次输入变化约0.1% 至 10%的门会变为活动状态

# Fault simulation

![[Pasted image 20250501034841.png#pic_50center|]]
- Fault simulation: simulating a circuit in the presence of faults
  故障仿真：在故障存在的情况下对电路进行仿真
- Objective of fault simulation:
	- determination of the quality of given tests
	  确定给定测试的质量
	- generation of information required for fault diagnosis (i.e., location of faults in a chip)
	  生成故障诊断所需的信息（即芯片中的故障位置）
- $\mathrm{Total\ number\ of\ lines} (L) = \mathrm{primary\ inputs} (n) + \mathrm{internal\ lines} (k) + \mathrm{primary\ outputs} (m)$
  总线路数 $L = \text{主输入} (n) + \text{内部线路} (k) + \text{主输出} (m)$
- $\mathrm{Input\ vector} (P) = (p_1 , p_2 , \cdots , p_n )$, where $p_j \in \{0, 1\},\ 1 \leq j \leq n$

## Elements of Fault Simulation

- The fault simulation process is illustrated as below
![[Pasted image 20250501034854.png#pic_50center|]]
- The fault simulator affects the speed of overall fault simulation
  故障模拟器会影响整体故障仿真的速度。

## Test Vector Example

![[Pasted image 20250501034919.png#pic_75center|]]

## Fault Simulation Essentials

- Since the number of single SAFs (Stuck-At Fault) is proportional to $L$, the number of lines in a circuit, the complexity of the above fault simulation approach is $\Theta(L^2)$.
  由于单个 SAF（固定故障）的数量与电路中的线路数 $L$ 成正比，上述故障仿真方法的复杂度为 $\Theta(L^2)$。
- Harel and Krishnamurthy (1987) conclude that there is little hope of finding a fault simulation algorithm with linear complexity.
  Harel 和 Krishnamurthy（1987）得出结论，几乎不可能找到线性复杂度的故障仿真算法
- **Fault collapsing** and **fault dropping** are two approaches that are commonly used to reduce the complexity of fault simulation.
  两种常用于降低故障仿真复杂度的方法

## Fault Collapsing
*兄啊你怎么又讲一遍*

- The number of faulty versions of a circuit that need to be simulated can be decreased by exploiting two relations between two faults: fault equivalence and fault dominance.
  通过利用两种故障关系：故障等价性和故障支配性，可以减少需要仿真的故障电路版本数量。
- Two faults $f_i$ and $f_j$ are said to be equivalent if the corresponding faulty versions of the circuit, $C^{f_i}$ and $C^{f_j}$, have identical input–output logic behavior.
  若两个故障 $f_i$ 和 $f_j$ 对应的故障电路 $C^{f_i}$ 和 $C^{f_j}$ 具有相同的输入-输出逻辑行为，则称它们为等价故障。
- Fault $f_i$ is said to dominate fault $f_j$ if
  若故障 $f_i$ 支配 故障 $f_j$，则满足以下条件：
	- $V^{f_i}\supseteq V^{f_j}$
	- each vector that detects $f_j$ implies identical values at the corresponding outputs of $C^{f_i}$ and $C^{f_j}$.
	  能检测到 $f_j$ 的每个向量在电路 $C^{f_i}$ 和 $C^{f_j}$ 的对应输出上产生相同的值。

## Fault Dropping

![[Pasted image 20250501034954.png#pic_50center|]]

- When fault simulation is performed to only compute the fault coverage, fault simulation can be further accelerated via fault dropping.
  当故障仿真的目标仅为计算故障覆盖率时，可以通过故障删除进一步加速仿真过程。
- Fault dropping is the practice in which faults detected by a vector are deleted from the fault list prior to the simulation of any subsequent vector. The decrease in complexity of fault simulation is due to the decrease in the average number of faults that are simulated for each vector
  故障删除指的是在仿真任何后续向量之前，将已被某个向量检测到的故障从故障列表中移除。故障仿真复杂度的降低是由于每个向量所需仿真的故障数量减少所导致的。

## Fault Simulation Scenario

- Circuit model: mixed-level
	- Mostly logic with some switch-level for high-impedance $(Z)$ and bidirectional signals
	  主要是逻辑模型，同时包含一些用于高阻抗 $(Z)$ 和双向信号的开关级模型
- Signal states: logic
	- Two states $(0, 1)$, three states $(0, 1, X)$, four states $(0, 1, X, Z)$, etc.
	  两种状态 $(0, 1)$，三种状态 $(0, 1, X)$，四种状态 $(0, 1, X, Z)$ 等
- Timing:
	- Zero-delay
		- For combinational circuits with no feedback
		  适用于无反馈的组合电路
	- Unit-delay
		- It can maintain the proper sequencing of signal changes
		  可以保持信号变化的正确顺序
	- Multiple-delay
- Faults
	- Mostly single stuck-at faults
	  主要为单个固定故障
	- Sometimes stuck-open, transition, and path-delay faults; analog circuit fault simulators are not yet in common use
	  有时包括固定开路故障、跳变故障和路径延迟故障；模拟电路故障仿真器尚未被广泛使用
- Equivalence fault collapsing of single stuck-at faults
	- Fault dropping: a fault once detected is dropped from consideration as more vectors are simulated; fault-dropping may be suppressed for diagnosis
	  故障删除：一旦某个故障被检测到，就会从故障列表中移除，随后不再进行仿真；故障删除可能会被抑制以用于诊断
	- Fault sampling: a random sample of faults is simulated when the circuit is large
	  故障抽样：当电路规模较大时，仅对随机选取的故障进行仿真

## Fault Simulation Paradigms

- Fault simulation
	- In general, simulating a circuit in the presence of faults is known as fault simulation
	  一般来说，在故障存在的情况下对电路进行仿真称为故障仿真
- The main goals of fault simulation
	- Measuring the effectiveness of the test patterns
	  评估测试模式的有效性
	- Guiding the test pattern generator program
	  指导测试模式生成程序
	- Generating fault dictionaries
	  生成故障字典
- Outputs of fault simulation
	- Fault coverage: fraction (or percentage) of modeled faults detected by test vectors
	  故障覆盖率：测试向量检测到的建模故障的比例（或百分比）
	- Set of undetected faults
	  未检测故障的集合

- In this section, we will discuss main fault simulation paradigms for combinational circuits. They are
	- Serial fault simulation
	  串行故障仿真
	- Parallel fault simulation
	  并行故障仿真
	- Deductive fault simulation
	  演绎故障仿真
	- Concurrent fault simulation
	  并发故障仿真

## Serial Fault Simulation

![[Pasted image 20250501132230.png#pic_50center|]]
- Serial fault simulation algorithm
	- Simulate fault-free circuit and save responses. Repeat following steps for each fault in the fault list
	  先对无故障电路进行仿真并保存响应。然后对故障列表中的每个故障重复以下步骤
		- Modify netlist by injecting one fault
		  通过注入一个故障修改网表
		- Simulate modified netlist, vector by vector, comparing responses with saved responses
		  逐个向量仿真修改后的网表，并与保存的响应进行比较
		- If response differs, report fault detection and suspend simulation of remaining vectors
		  如果响应不同，则报告故障检测，并暂停对剩余向量的仿真
- Advantages
	- Easy to implement; needs only a true-value simulator
	  实现简单，仅需要一个真值仿真器
	- Less memory is required
	  需要的内存少
- Disadvantages
	- Much repeated computation; CPU time prohibitive for VLSI circuits
	  计算重复度高，在超大规模集成电路（VLSI）中计算时间过长
- Alternative
	- Simulate many faults together
	  一次仿真多个故障

## Parallel Fault Simulation

![[Pasted image 20250501133006.png#pic_75center|]]
- Assumptions
	- The simulated circuit consists of only logic gates and all gates have the same delays
	  被仿真的电路仅由逻辑门组成，且所有门的延迟相同
	- Signals take only binary (0 and 1) values
	  信号仅采用二进制值（0 和 1）
- Main idea
	- Take advantage of the bit-parallelism of logical operations in a digital computer
	  利用数字计算机中逻辑运算的位并行性
		- For a 32-bit machine word, an integer consists of a 32-bit binary vector
		  在 32 位机器字中，一个整数由 32 位二进制向量组成
		- A logic AND or OR operation involving two words performs simultaneous AND or OR operations on all respective pairs of bits
		  逻辑 AND 或 OR 运算涉及两个字时，会对所有对应位同时执行 AND 或 OR 操作
- Storage requirement
	- One word per line for two-state simulation
	  对于两态仿真，每条线路需要一个机器字
- If the computer word size is $N$, then $N-1$ copies of faulty circuit are also generated
  如果计算机字长为 $N$，则会生成 $N-1$ 份故障电路副本
	- For a total $M$ faults in the circuit, $\left\lceil{ M /(N −1)}\right\rceil$ simulation runs are then necessary
	  对于电路中的总故障数 $M$，需要进行 $\left\lceil{ M /(N −1)}\right\rceil$ 次仿真运行
	- Speedup over serial fault simulation about N-1
	  相较于串行故障仿真，速度提升约为 $N-1$
- Disadvantages
	- Lacking the capability to simulate accurate rise and fall delays of signals
	  无法模拟信号的准确上升和下降延迟
	- Not suitable for circuits with non-Boolean logic
	  不适用于具有非布尔逻辑的电路

## Deductive Fault Simulation

*不改变的那个取补集后取并集，两个都改变取并集*
![[Pasted image 20250501133316.png#pic_75center|]]
![[Pasted image 20250501133324.png#pic_75center|]]
- Simulating only the behavior of the fault-free logic circuits
  仅仿真无故障逻辑电路的行为
- Need only one pass for each test pattern
  每个测试模式仅需执行一次仿真
- All signal values in each faulty circuit are deduced from the fault-free circuit values and the circuit structure
  每个故障电路中的所有信号值均可根据无故障电路的值及电路结构推导得出
- For each test pattern, a deductive procedure is applied to all lines in a level-order (for combinational logic) from inputs to outputs
  对于每个测试模式，采用推导过程按照层级顺序（针对组合逻辑）从输入到输出应用于所有线路
- Definition
	- The fault list $L_A$ is defined as the set containing the name or index of every fault that produces an error on line $A$ when the circuit is in its current logic state
	  故障列表 $L_A$ 被定义为包含所有会在当前逻辑状态下使线路 $A$ 产生错误的故障名称或索引的集合
- Fault lists are to be propagated from PIs to the POs
  故障列表需从主输入（PI）传播到主输出（PO）
- A fault list is generated for each signal lines, and updated as necessary with every change in the logic state of the circuit
  每条信号线都会生成一个故障列表，并在电路逻辑状态发生变化时进行必要的更新
- List events occur when a fault list changes
  当故障列表发生变化时，就会触发列表事件

## Concurrent Fault Simulation

![[Pasted image 20250501133707.png#pic_75center|]]
- Event-driven simulation of fault-free circuit and only those parts of the faulty circuit that differ in signal states from the fault-free circuit.
  仅针对无故障电路以及仅部分与无故障电路不同的故障电路进行事件驱动仿真
- A list per gate containing copies of the gate from all faulty circuits in which this gate differs. List element contains fault ID, gate input and output values and internal states, if any.
  每个门对应一个列表，其中包含该门在所有故障电路中的副本，且这些故障电路的该门与无故障电路不同。列表元素包括故障 ID、门的输入和输出值，以及可能存在的内部状态。
- All events of fault-free and all faulty circuits are implicitly simulated
  所有无故障电路和故障电路的事件均被隐式仿真。
- Faster than other methods, but uses most memory.
  速度快于其他方法，但占用内存最多

# Functional vs. Structural Test

- Functional test
	- Generate complete set of tests for circuit input-output combinations
	- 129 inputs & 65 outputs
	- $2^{129}=680,564,733,841,876,926,926,749,214,863,536,422,912$ test patterns are required
	- Using 1 GHz ATE, would take $2.15 \times 10^{22}$ years
- Structural test
	- 64 bit slices and each slice has 27 faults (using fault collapsing)
	- At most $64\times27=1728$ faults, thus only 1728 test patterns are required
	- Takes 0.000001728 seconds on 1 GHz ATE

# Circuit & Binary Decision Tree

![[Pasted image 20250501134012.png#pic_75center|]]
- All ATPG programs need a data structure describing the search space for test patterns
  所有 ATPG（自动测试模式生成）程序都需要一种数据结构来描述测试模式的搜索空间
- Binary decision tree
  二进制决策树（深度优先搜索，雾）

# Boolean Difference

- Shannon’s Expansion Theorem
  香农展开定理
	- An arbitrary Boolean function $f(x_1 ,x_2 ,\dots,x_n )$ can be expanded about any variable
	  任意布尔函数 $f(x_1 ,x_2 ,\dots,x_n )$ 都可以关于任意变量展开
	- For example, if we expand the function with respect to x2 , then the function can be expressed as below$$f(x_1 ,x_2 ,\cdots,x_n )=x_2 \cdot f(x_1 ,1,\cdots,x_n )+\overline{x_2}\cdot f(x_1 ,0,\cdots,x_n )$$
- Boolean Difference
  布尔差分
	- Let $f(x)=f(x_1 ,x_2 ,\cdots,x_n )$ be the normal (fault-free) output function realized by network $N$, and $f_a (x_1 ,x_2 ,\cdots,x_n )$ be the faulty output function resulting from a fault a in $N$.
	  设 $f(x)=f(x_1 ,x_2 ,\dots,x_n )$ 为网络 $N$ 所实现的正常（无故障）输出函数，$f_a (x_1 ,x_2 ,\dots,x_n )$ 为因故障 $a$ 而产生的故障输出函数。
		- The test set for a fault a is $T_a=f(x)\oplus f_a(x)$
		  故障 $a$ 的测试集为 $T_a=f(x)\oplus f_a(x)$

- 布尔差分定义2：$$\displaylines{\frac{\mathrm{d}f(X)}{\mathrm{d}x_i}\equiv f_i(0)\oplus f_i(1)\equiv f(x_1\cdots,x_i,\cdots,x_n)\oplus f(x_1\cdots,\overline{x_i},\cdots,x_n) \\ \frac{\mathrm{d}f(X)}{\mathrm{d}x_i}=0\implies f_i(0)=f_i(1) \\ \frac{\mathrm{d}f(X)}{\mathrm{d}x_i}=1\implies f_i(0)\neq f_i(1)}$$

## 例子1

$$\displaylines{f(X)=x_1\overline{x_2}+x_2x_3+x_1x_3 \\ f_{{x_1}/0}(X)=x_2x_3 \\ f(X)\oplus f_{x_1/0}(X)=\left(x_1\overline{x_2}+x_2x_3+x_1x_3\right)\oplus \left(x_2x_3\right) = x_1\overline{x_2}}$$

测试向量：$$T_{x_1/0}=\{10\mathrm{x}\}=\{100,101\}$$

## 例子2

有两个故障$\alpha=x_i/0$，$\beta=x_i/1$，他们俩对应的测试向量为：
- $\alpha=x_i/0$：$$\displaylines{T_{\alpha}=f(X)\oplus f_{\alpha}(X)=\left(\overline{x_i}f_i(0)+x_if_i(1)\right)\oplus f_i(0)\text{ 香农展开} \\ =x_i\overline{f_i}(1)f_i(0)+x_if_i(1)\overline{f_i}(0)=x_i\left(f_i(1)\oplus f_i(0)\right) \\ =x_i\frac{\mathrm{d}f(X)}{\mathrm{d}x_i}} $$
- $\beta=x_i/1$：$$\displaylines{T_{\beta}=f(X)\oplus f_{\beta}(X)=\left(\overline{x_i}f_i(0)+x_if_i(1)\right)\oplus f_i(1)\text{ 香农展开} \\ =\overline{x_i}\overline{f_i}(0)f_i(1)+\overline{x_i}f_i(0)\overline{f_i}(1)=\overline{x_i}\left(f_i(1)\oplus f_i(0)\right) \\ =\overline{x_i}\frac{\mathrm{d}f(X)}{\mathrm{d}x_i}} $$

## 例子3

![[Pasted image 20250501135917.png#pic_75center|]]

# Single-Path Sensitization
*必考*

- Definition
	- We say a test $t$ activates a fault $\alpha$ if it generates an error (or a fault effect) by creating different $v(l)$ and $v_\alpha (l)$ values at the fault site $l$. We say $t$ propagates the error (fault effect) to a PO $z$ if it results in different $v(z)$ and $v_\alpha (z)$ values
	  如果测试 $t$ 通过在故障位置 $l$ 处产生不同的 $v(l)$ 和 $v_\alpha (l)$ 值，从而生成错误（或故障效应），则称 $t$ 激活了故障 $\alpha$。如果 $t$ 将错误（故障效应）传播到主输出（PO）$z$，导致 $v(z)$ 和 $v_\alpha (z)$ 的值不同，则称 $t$ 传播了错误（故障效应）。
- Definition
	- A line whose value in the test $t$ changes in the presence of the fault $\alpha$ is said to be sensitized to $\alpha$ by $t$. A path composed of sensitized lines is called a sensitized path.
	  如果在测试 $t$ 下，某条线路的值在故障 $\alpha$ 作用下发生变化，则称该线路被 $t$ 敏化到故障 $\alpha$。由敏化线路组成的路径称为敏化路径
- Fault activation or excitation
  故障激活或激励
	- Specify inputs so as to generate the appropriate value at the fault site, i.e., 0 for s/1 and 1 for s/0
	  设定输入值，以在故障位置生成适当的值，例如对于 s/1 设定 0，对于 s/0 设定 1
- Fault propagation
  故障传播
	- Select a path from the fault site to an output and specify other signal values to propagate the fault (error signal) along the path to the output
	  从故障位置选择一条路径至输出，并设定其他信号值，以沿路径传播故障（错误信号）至输出
- Line justification
  线路合理性检查
	- Specify input values so as to produce the signal values specified in fault activation and fault propagation, i.e., perform consistency check
	  设定输入值，以生成符合故障激活和故障传播指定的信号值，即执行一致性检查

## 例子

![[Pasted image 20250501140421.png#pic_75center|]]
- Generate a appropriate value $a=0\rightarrow A=B=C=1$
- Choose a path via $G5\rightarrow b=1 \rightarrow A=D=0$. Contradiction!
- Try another path via $G6\rightarrow c=1 \rightarrow C=1$ and $E=0$. OK!
- Therefore, $T=ABC\overline{E}$

# Problems of Sequential Circuit Testing

![[Pasted image 20250501143756.png#pic_50center|]]

- A sequential circuit has memory in addition to combinational logic
  时序电路除了包含组合逻辑外，还具有存储单元
- Test for a fault in a sequential circuit is a sequence of vectors, which
  对时序电路中的故障进行测试时，需要使用一系列测试向量，流程如下：
	- Initializes the circuit to a known state
	  初始化电路至已知状态
	- Activates the fault, and
	  激活故障
	- Propagates the fault effect to a primary output
	  传播故障效应至主输出
- Methods of sequential circuit ATPG
  时序电路 ATPG 的方法包括：
	- Time-frame expansion methods
	  时间帧扩展方法
	- Simulation-based methods
	  基于仿真的方法

## Time-Frame Expansion

![[Pasted image 20250501144721.png#pic_75center|]]
- Iterative Array Conversion
  迭代阵列转换
	- Sequence of inputs in time: $x(1), x(2),\cdots, x(n)$
	- Sequence of outputs in time: $z(1), Z(2),\cdots,z(n)$
	- Sequence of internal states in time: $y(0),y(1),\cdots, y(n)$
> **Pseudo Flip-Flop**（伪触发器）通常指的是一种在测试或仿真环境中使用的存储单元，它模拟传统触发器的行为，但可能不具有完整的硬件实现。例如，它可能用于故障仿真或自动测试向量生成（ATPG），以模拟时序电路的状态变化，而无需真正的时钟控制或严格的电气特性。

![[Pasted image 20250501145203.png#pic_75center|]]
- When a single stuck-at fault is present in the real sequential circuit, it will appear as a multiple fault, existing in each unfolded iteration (time frame)
  当真实的时序电路中存在单个卡故障时，它将在每个展开的迭代（时间帧）中表现为多个故障

![[Pasted image 20250501150105.png#pic_75center|]]
- Test pattern generation with D-Algorithm.
	- $t_0$: initial state $y_1=y_2=0$; and $a/1→a=D^\prime$
		- Set $x(0)=1\to y_2 (1)=D^\prime$ and $z(0)=1$
		- $z \neq D \text{ or } D^\prime \to \text{ Continue!}$
	- $t_1$: set $x(1)=1\to y_1(2)=y_2(2)=D^\prime$ and $z(1)=1$
		- z !=D or D’→Continue!
	- $t_2$: on G5, let $x(2)=1$
		- $y_1(2)=D^\prime\to z(2)=D$
	- Test sequence $X=111$
- Termination rules
	- If $z=D \text{ or } D^\prime$ then a test sequence is found
	  如果 $z=D$ 或 $D^\prime$，则找到一个测试序列
	- If $k>4^n$, where $n$ is the number of FFs of the original circuit, then the circuit is redundant
	  如果 $k>4^n$，其中 $n$ 是原始电路中的触发器数量，则该电路是冗余的
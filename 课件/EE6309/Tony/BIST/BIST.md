---
aliases: 
tags:
---
- Built-in self-test (BIST):
  内建自测试（BIST）
	- The capability of a circuit to test itself
	  电路具备自行测试的能力
- Advantages of BIST
  BIST 的优势
	- Test patterns generated on-chip: controllability increased
	  在芯片上生成测试模式：提高可控性
	- (Compressed) response evaluated on-chip: observability increased
	  （压缩的）响应在芯片上评估：提高可观察性
	- Test can be on-line (concurrent) or off-line
	  测试可以是在线（并行）或离线模式
	- Test can run at circuit speed: more realistic; shorter test time; easier delay testing
	  测试可以以电路速度运行：更真实；测试时间更短；更易进行延迟测试
	- External test equipment greatly simplified, or even totally eliminated
	  外部测试设备大幅简化，甚至可能完全省略
	- Easily adopting to engineering changes
	  便于适应工程变更

# Introduction to Built-In Self-Test

- On-line BIST
  在线 BIST
	- Concurrent (EDAC, NMR, totally self-checking checkers, etc.):
	  并行（EDAC、NMR、完全自检校验器等）：
		- Coding or modular redundancy techniques (fault tolerance)![[Pasted image 20250502033705.png#pic_50center|]]
		  采用编码或模块冗余技术（容错）
		- Instantaneous correction of errors caused by temporary or permanent faults
		  对临时或永久故障引起的错误进行即时校正
	- Nonconcurrent (diagnostic routines):
	  非并行（诊断程序）
		- Carried out while a system is in an idle state
		  在系统处于空闲状态时执行

- Off-line BIST
	- A typical BIST architecture![[Pasted image 20250502033823.png#pic_50center|]]
	  典型的 BIST 架构
- Test generation
	- Prestored TPG, e.g., ROM or shift register
	  预存 TPG，例如 ROM 或移位寄存器
	- Exhaustive TPG, e.g., binary counter
	  穷尽 TPG，例如二进制计数器
	- Pseudo-exhaustive TPG, e.g., constant-weight counter, combined LFSR and SR
	  伪穷尽 TPG，例如定权计数器、组合 LFSR 和 SR
	- Pseudo-random pattern generator, e.g., LFSR
	  伪随机模式生成器，例如 LFSR

- Response analysis
	- Check-sum
	- Ones counting
	- Transition counting
	- Parity checking
	- Syndrome analysis
	- Etc.
- Linear feedback shift register (LFSR) can be both the test generator and response analyzer
  线性反馈移位寄存器（LFSR）既可以作为测试生成器，也可以作为响应分析器
- We need a gold unit to generate the good signature or a simulator
  需要一个黄金单元来生成正确的签名，或使用模拟器
  > **Gold Unit:** 经过测试验证的good chip，可用于环境调试时验证环境是否正常。
  
# Signature Analysis

- A compression technique based on the concept of cyclic redundancy checking (CRC) and realized in hardware using linear feedback shift registers
  一种基于循环冗余校验（CRC）概念的压缩技术，并在硬件中通过线性反馈移位寄存器实现
- Definition
	- A function $f(x_1 ,x_2 ,\cdots,x_n)$ is said to be linear if it can be expressed in the form 
	  如果函数$f(x_1 ,x_2 ,\cdots,x_n)$为线性函数，则可以表示为$$f = a_0 + a_1 x_1 + a_2 x_2 + \cdots + a_n x_n$$
	  where $a_i \in \{0, 1\},\ \forall i = 0, 1,\cdots,n$
	- There are $2n+1$ linear functions of $n$ variables
	  $n$个变量的线性函数共有$2n+1$个
	- Linear operations: modulo addition, module scalar multiplication, & delay
	  线性运算：模加法、模数标量乘法和延迟
	- Nonlinear operations: AND, OR, NAND, NOR, etc.
	  非线性运算：AND、OR、NAND、NOR等

# Linear Feedback Shift Register
*在CRC中也出现过*

![[Pasted image 20250502034538.png#pic_75center|Structures of LFSR]]

- Definition
	- A linear feedback shift register is a shift register with feedback paths which consist only of unit delays and XOR operators
	  线性反馈移位寄存器是一个移位寄存器，其反馈路径仅由单位延迟和异或（XOR）运算符组成
	- Let $M=\text{fault-free circuit response}$, $B=\text{faulty circuit response}$, and $E=\text{error syndrome (Hamming)}$, where $E=M + B$, thus $M=B + E$ and $B=M + E$
	  设$M=\text{无故障电路响应}$，$B=\text{故障电路响应}$，$E=\text{错误特征值（汉明）}$，其中$E=M + B$，因此$M=B + E$且$B=M + E$
		- We need a circuit to take $B$ as input and compact it but still be able to tell if $M!=B$
		  需要一个电路将$B$作为输入并进行压缩，但仍然能够判断$M\neq B$
	- LFSR is considered as a popular approach for test response compaction
	  - LFSR被认为是测试响应压缩的一种常见方法

## LFSR for Signature Analysis
*和CRC很像*

- Let $m(X)$ be the input polynomial of degree $k-1$, $q(X)$ the quotient, and $s(X)$ the signature (remainder).
  设$m(X)$为次数为$k-1$的输入多项式，$q(X)$为商，$s(X)$为签名（余数）
- Then $$m(X)=q(X)c(X)+s(X)$$
- The error syndrome can be represented as a polynomial $e(X)$
  错误特征值可以表示为多项式$e(X)$
	- E.g., let $m(X)=X^4+X^3+1(11001)$, and an erroneous input $b(X)=X^3+X+1(01011)$, then the error syndrome is $11001\oplus 01011=10010$, and is represented by $e(X)=X^4+X$
	  例如，设$m(X)=X^4+X^3+1(11001)$，错误输入$b(X)=X^3+X+1(01011)$，则错误特征值为$11001\oplus 01011=10010$，表示为$e(X)=X^4+X$。
- In general, an erroneous input polynomial can be represented by
  一般来说，错误的输入多项式可以表示为 $$B(X)=m(X)\oplus e(X)$$

- Theorem1: Input streams $m(X)$ and $b(X)$ have the same signature if $e(X)$ is a multiple of $c(X)$
  定理1：当$e(X)$是$c(X)$的倍数时，输入流$m(X)$和$b(X)$具有相同的签名
	- Proof: an error is not detected when $m(X)$ and $b(X)$ have the same signature, i.e., $b(x)=q’(X)c(X)+s(X)$. Since $m(X)=q(X)c(X)+s(X)$, we obtain
	  证明：当$m(X)$和$b(X)$具有相同的签名时，错误不会被检测到，即$b(X)=q’(X)c(X)+s(X)$。由于$m(X)=q(X)c(X)+s(X)$，因此可以得到 $$e(X)=m(X)+b(X)=c(X)(q^\prime(X)-q(X))$$
- Theorem2: Undetected errors correspond to error patterns which are multiples of $c(X)$
  定理2：未检测到的错误对应于$c(X)$的倍数形式的错误模式
- Theorem3: If $c(X)$ has $2$ or more nonzero coefficients i.e., at least 1 feedback term-then it can detect all single-bit errors
  定理3：如果$c(X)$具有2个或更多非零系数，即至少包含1个反馈项，则它可以检测所有单比特错误
	- Proof: all nonzero multiples of $c(X)$ must have at least 2 nonzero coefficients. Therefore, any error with only 1 nonzero coefficient cannot be a multiple of $c(X)$ and must be detectable.
	  证明：所有$c(X)$的非零倍数必须至少具有2个非零系数。因此，任何仅包含1个非零系数的错误都不能是$c(X)$的倍数，并且必须是可检测的。
- Theorem4: for a $k$-bit response sequence, if all possible error patterns are equally likely, then the probability of failing to detect an error (i.e., the aliasing probability) by the LFSR of length $r$ is 
  定理4：对于$k$位响应序列，如果所有可能的错误模式出现的概率相等，则LFSR长度为$r$时未能检测到错误（即别名概率）的概率为$$P_{\mathrm{al}}=\frac{2^{k-r}-1}{2^k-1}$$
	- Proof: For a k-bit response, $\mathrm{deg}(m(X))=k-1$, and $\mathrm{deg}(e(X))\leq k-1$. Therefore, the number of possible error polynomial is represented by $e(X)=c(X)p(X)$ for some nonzero $p(X)$. Since $\mathrm{deg}(c(X))=r$, the number of possible p(X)’s is $2^{k-r} -1$. Thus For a long sequence, $k\gg r\to P_{\mathrm{al}}\approx 1/2^r$
	  对于$k$位响应，有$\mathrm{deg}(m(X))=k-1$，且$\mathrm{deg}(e(X))\leq k-1$。因此，可能的错误多项式可以表示为$e(X)=c(X)p(X)$，其中$p(X)$为非零多项式。由于$\mathrm{deg}(c(X))=r$，则可能的$p(X)$数量为$2^{k-r} -1$。因此，对于一个较长的序列，当$k\gg r$时，$P_{\mathrm{al}}\approx 1/2^r$。

# Response Compaction

- Usually, we think of data compression as a process that preserves data integrity. This is why we give more attention here to data compaction, which may result in some losses
  通常，我们认为数据压缩是一种保持数据完整性的过程。因此，我们更关注数据压缩（Compaction），尽管它可能会导致一些损失
- There are several compaction testing techniques
	- Parity testing
	- One counting
	- Transition counting
	- Syndrome calculation
	- Signature analysis

## Parity Testing

- This is the simplest of all techniques but also the most lossy
  这是所有技术中最简单但也是损失最严重的
- The parity of responses to the test patterns is calculated as 
  对测试模式的响应的校验计算为$$P=\Sigma^{i=L}_{i=1}r_i$$ where $L$ is the length of the test and $r_i$ is the response for the $\mathrm{i}^{\mathrm{th}}$ test pattern
  其中$L$为测试长度，$r_i$为第$i$个测试模式的响应
- The response of the circuit under test (CUT) to pattern $i$ and the partial product $P_{i-1}$ is illustrated as below![[Pasted image 20250502041007.png#pic_50center|]]
  被测电路（CUT）对模式$i$的响应及其部分乘积$P_{i-1}$如下所示

## One Counting

- The number of 1’s in the response stream is calculated and compared to the number of 1’s in the fault-free responses
  响应流中1的数量被计算并与无故障响应中的1的数量进行比较
- Consider the circuit shown below![[Pasted image 20250502041204.png#pic_50center|]]
- If we have a test of length $L$ and the fault-free count is $m$, the possibility of aliasing is $[C(L,m)-1]$ patterns out of a total number of possible strings of length $L$, $(2L -1)$
  如果测试长度为$L$，无故障计数为$m$，则其他现象发生的可能性是$[C(L,m)-1]$种模式，在所有可能的长度为$L$的字符串中，总数为$(2L -1)$。

## Transition Counting

- In transition counting compaction, it is only the number of transition 0→1 and 1→0 that are counted. Thus the signature is given by
  在跳变计数压缩中，仅计算从0→1和1→0的跳变次数。因此，签名由以下方式给出： $$\Sigma_{i=1}^{i=L-1}r_i\oplus r_{i+1}$$where the summation is ordinary addition and $\oplus$ is XOR operation
- The compaction scheme is shown below![[Pasted image 20250502041749.png#pic_50center|]]

# Pseudorandom Pattern Generator

- Logic BIST uses mostly pseudorandom (PR) tests. They are usually much longer than deterministic tests, but are definitely less costly to generate.
  逻辑 BIST 主要使用伪随机（PR）测试。这些测试通常比确定性测试长得多，但生成成本明显较低
- PR tests are generated using a LFSR or cellular automata.
  PR 测试由 LFSR 或元胞自动机生成
- By means of a simple circuit called an autonomous linear feedback shift register (ALFSR).
  通过一种称为自主线性反馈移位寄存器（ALFSR）的简单电路实现
- Definition: an ALFSR is a LFSR with no external inputs.
  定义：ALFSR 是一种没有外部输入的 LFSR
- Faults that are hard to detect with PR tests are called random pattern resistant faults.
  难以使用 PR 测试检测的故障称为随机模式抗性故障

## 例子

The following ALFSR generates the pseudorandom sequence shown in the table below![[Pasted image 20250502042003.png#pic_50center|]]
- The output sequence is 000111101011001, which repeats after $15(2^n -1)$ clocks
  输出序列为 000111101011001，在经过 $15(2^n -1)$ 个时钟周期后重复
- Max period for an n-stage ALFSR=$2^n-1$
  n 级 ALFSR 的最大周期为 $2^n-1$
- All-0 state of the register cannot occur in the max-length cycle
  在最大长度循环中，寄存器的全 0 状态不会出现

# Built-In-Logic-Block-Observer (BILBO)

![[Pasted image 20250502035241.png#pic_50center|]]
- A BILBO is a multi-purpose test module which serves as a test generator or a signature analyzer. It is composed of a row of FFs and some additional gates for shift and feedback operation
  BILBO 是一种多功能测试模块，可用作测试生成器或签名分析器。它由一排触发器（FF）和一些用于移位和反馈操作的额外逻辑门组成。
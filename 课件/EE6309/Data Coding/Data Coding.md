# Self-Checking

- the capability to verify automatically whether there is any fault without the need of externally applied test stimuli.
	能自动检测是否存在故障，不需要额外的外部激励。
- Self-checking design can be achieved by using errordetecting codes
	使用错误检测编码可以实现自检设计
	- During normal fault-free operation, the logic network receives only a subset of input code & produces a subset of output code: valid code word
	  在一个逻辑网络的正常无故障操作中，网络所接收到的输入数据和产生的输出数据都符合预定的编码规则。这些符合编码规则的数据被称为“有效编码字”。有效编码字是输入数据和输出数据的一个子集。
	- A non-code word indicates the presence of a fault
	  没有被编码的字表示存在故障
	- A fault may also result in an (incorrect) code word, rather than a non-code word – undetectable fault
	  错误也可能导致错误的编码字，而不是未编码的字，这是不可检测的错误

## Totally Self-Checking Circuit

- **Fault-Secure circuit**: For any fault from a given set of faults, the circuit never produces an incorrect code word.
对于任何给定的一组错误，电路永远不会产生错误的编码字（不会产生未被编码的输出）
- **Self-Testing circuit**: For every fault from a given set of faults, the circuit produces a non-code word at the output for at least one input code word.
对于给定的一组故障中的每个故障，电路在至少一个输入编码字的情况下会在输出中产生一个非编码字
- A circuit is totally self-checking if it is both fault-secure & self-testing: during normal operation all faults from a given set would cause a detectable, erroneous output.
如果一个电路既是fault-secure的又是self-testing的，那么它就是totally self-checking的：在正常操作期间，给定的一组故障中的所有故障都会导致可检测的错误输出

- Temporary faults and permanent faults are detected
- Faults are immediately detected upon occurrence

### Two-Rail Checker

![[Pasted image 20250211155002.png#pic_center|Two-Rail Checker]]
- 输出永远是互补的，如果不是互补的说明有错误。
- 输入的x与y要求是互补的，会产生一个互补的输出
- 

### Multi-Level Tree Checker

- A two-rail checker for an arbitrary number of input pairs may be designed using two-level AND-OR logic
	对于任意数量的输入对，可以使用两级与-或逻辑设计一个two-rail checker
- A tree checker realized by interconnecting the checker modules with two input pairs is more efficient
	用两对输入的检查器互联成树形检查器更加高效
- A general multi-level tree checker with $m$ input pairs formed by interconnecting two-rail checker modules, requires $m-1$ modules and $\mathrm{log}_2m$ module levels
	$m$输入，要$m-1$个模块，$\mathrm{log}_2m$层

## Parity Checking

| EVEN PARITY   | ODD PARITY    |
| ------------- | ------------- |
| 数据和校验位的1数量是偶数 | 数据和校验位的1数量是奇数 |
$P_{\text{EVEN}}=b_{n-1}\oplus b_{n-2}\oplus \cdots \oplus b_{1} \oplus b_{0}$
$P_{\text{ODD}}=\overline{b_{n-1}\oplus b_{n-2}\oplus \cdots \oplus b_{1} \oplus b_{0}}$

### Error Detection

- An error signal ($E$) is generated from the code-word received, which is defined as:
	- $E_{\text{EVEN}}=b_{n-1}\oplus b_{n-2}\oplus \cdots \oplus b_{1} \oplus b_{0} \oplus P_{\text{EVEN}}$
	- $E_{\text{ODD}}=\overline{b_{n-1}\oplus b_{n-2}\oplus \cdots \oplus b_{1} \oplus b_{0} \oplus P_{\text{ODD}}}$
- $E=0$没有错误，$E=1$有错误

## 2-D Parity Checks

- Form data in 2-D code-words
- Generate both row and column parity bits (Transmitter)
- Execute both row and column parity checks (Receiver)
- Position of a single-bit error can be identified
	- Single-bit error can be corrected
- Position of multi-bit errors cannot be identified
	- Position of multi-bit errors cannot be identified
- Assembling and disassembling of data block is required

# Distance

## Distance

The number of bit(s) to change in one word to be identical to the other word
两个码元之间的不同bit数

## Hamming Distance

The smallest number of bit(s) in which any two words differ in a code
一套编码中任意两个码元之间的距离的最小值

## Minimum Distance Requirements

- 2+：检查1bit错误
- 3+：更正1bit错误
- 4+：检查2bit错误

---

- For $k\text{-bit}$ error detection, $\text{minimum distance}\geq k+1$. Without error correction capability
- For $k\text{-bit}$ error correction, $\text{minimum distance} \geq 2k+1$

---

- 对于这个课件（例如Hamming Code）：Correction能力是$\frac{d-1}{2}$位，Detection能力是$\frac{d}{2}$位
- 如果放弃纠错能力，使用别的编码能够将Detection能力提升到$d-1$位
# Hamming Code

- For an error correction, desirable to detect and locate error(s)
	对于错误更正，理想状态下应该能检测并定位错误
- **HAMMING CODES**: one of the commonly used error correction code
- Creation of special code-words from data string
- Insertion of multiple parity bits in code-word
- Each parity bit checks parity in strategic location
	每个校验位在设计好的位置校验
- Overlapping of bits checked
	指每个位校验位（奇偶校验位）同时检查多个数据位的奇偶性。
- Combination of parity check failures indicates bit(s) for correction
	校验失败的组合能够指示需要更正的bit位

![[Pasted image 20250211173917.png|他奶奶的这PPT不如直接看wiki]]

### 1-bit Correction

- To each group of $m$ **message bits**, $k$ **parity bits** $P_1 P_2 \cdots P_k$ are added to form an $m+k$ code
- Each bit of the code-word is assigned a decimal location number from 1 to $m+k$, starting from LSB
- $k$ parity checks are performed on specific bits of each codeword
	$k$位校验位会给码字的特定位进行校验
- The parity checks allow the development of a position binary number $b_{k-1} \cdots b_1 b_0$, whose value (when an error occurs) will identify the location of the error
	校验会产生一个位置二进制数$b_{k-1} \cdots b_1 b_0$，其值为产生错误的位置
- The number of $k$ parity bits must be large enough to identify any one of the possible $m+k$ single error, and identify "no error" with decimal value zero.
	校验位的数量$k$需要足够大以保证能够检测出$m+k$位编码中任意1bit的错误，并在没有错误时输出0
	$$2^k\geq m+k+1$$
- The parity bits are placed in positions $1, 2, 4 \cdots 2^{k-1}$ of the code-word
	校验位在码字的第$1, 2, 4 \cdots 2^{k-1}$位

---

根据PPT上的流程和wiki上的图，可以发现Hamming Code使用的方式是偶校验（异或过程中并不对最后的结果取反）。
其中校验位的覆盖位置通过wiki图上的X即可推断出：
- 在生成时忽略校验位自身的值，只考虑数据位
- 在收到数据校验时需要与校验位一起计算得到校验值，这个值会反应是否出错和出错的位置

#### Example: BCD

##### 生成

为了进行1bit的更正，需要Hamming Distance大于等于3，所以需要3个校验位，最终会生成7bit数据。根据wiki上的图，三个校验位覆盖的位置为：
- $P_1$：1，3，5，7
- $P_2$：2，3，6，7
- $P_3$：4，5，6，7
在去除校验位位于的位置后，假设原始数据为$M_4M_3M_2M_1$，可以得到校验位的计算为：
- $P_1=M_1\oplus M_2\oplus M_4$
- $P_2=M_1\oplus M_3\oplus M_4$
- $P_3=M_2\oplus M_3\oplus M_4$
最终合成的数据为：$Y_7Y_6Y_5Y_4Y_3Y_2Y_1=P_1P_2M_1P_3M_2M_3M_4$一共7bit数据。

###### 硬件实现

![[Pasted image 20250211175818.png]]

##### 错误检测

还是使用wiki上的图，但是这一次生成的数字需要包含校验位。设需要生成的数为$B_2B_1B_0$，其中：
- $B_0$覆盖1，3，5，7位
- $B_1$覆盖2，3，6，7位
- $B_2$覆盖4，5，6，7位
会发现这与生成校验位的流程几乎完全一样，那么我们就能够得到：
- $B_0=Y_1\oplus Y_3\oplus Y_5 \oplus Y_7$
- $B_1=Y_2\oplus Y_3\oplus Y_6\oplus Y_7$
- $B_2=Y_4\oplus Y_5\oplus Y_6\oplus Y_7$

###### 硬件实现

![[Pasted image 20250211181319.png#pic_75center|没什么好说的]]

##### 错误更正

仍然是根据wiki上的表，可以发现各个位的覆盖情况如下：
- $M_1$由$B_0$，$B_1$覆盖，所以当$M_1$出错时，这两位都应该为1
- $M_2$由$B_0$，$B_2$覆盖，所以当$M_2$出错时，这两位都应该为1
- etc.
总结一下就是，如果这一位出错了，那么被覆盖到的校验位都应该为1. 根据这一特性可以设计更正电路，由于只有数据位需要修正，所以只需要4组更正电路即可。

###### 硬件实现

![[Pasted image 20250211181853.png#pic_75center|]]
可以发现，每个数据位都由覆盖自己的校验位进行更正，没有覆盖自己的校验位进行取反操作。

### Double-bit Error

根据Hamming Distance的原理，如果要检测出2bit的错误，需要的Hamming距离为4。需要额外添加一个校验位$P_4$对Hamming编码后的数据进行校验。
- 如果$P_4$校验失败：
	- 如果$B_2B_1B_0\neq 0$，说明有1bit错误，错误在$B_2B_1B_0$指示的位置上，总共有2bit错误
	- 如果$B_2B_1B_0=0$，说明$P_4$有错误
- 如果$P_4$校验成功：
	- 如果$B_2B_1B_0\neq 0$，说明有2bit错误，错误的地方不知道
	- 如果$B_2B_1B_0=0$，说明没有错误

### Code Efficiency & Redundancy

For a code-word with $(m, k)$ bits,
$$\text{Code Efficiency}= \frac{m}{m+k}$$
$$\text{Code Redundancy} = \frac{k}{m+k}$$

# Cyclic Redundancy Check

## Polynomial Representation

二进制数可以用多项式表示，一个数$$B=b_{n-1}b_{n-2}\cdots b_2b_1b_0$$可以用多项式表示为：$$B=b_{n-1}x^{n-1}+b_{n-2}x^{n-2}\cdots b_2x^2+b_1x+b_0$$

## Modulo-2 Arithmetic

### 加减法

$$A+B=A-B=A\oplus B$$

### 除法

使用多项式除法可以做出来。对于被除数是$B(x)$，除数是$G(x)$的多项式除法，规定商为$Q(x)$，余数为$R(x)$，可以得到：$$\frac{B(x)}{G(x)}=Q(x)+\frac{R(x)}{G(x)}$$两边同时乘$G(x)$，可以得到：$$B(x)=Q(x)\cdot G(x)+R(x)$$由于在Module-2算法中加减法一样，所以有$$B(x)+R(x)=Q(x)\cdot G(x)$$

## Principles of CRC Code

发送端发送的数据为$T(x)$，接收端接收到的数据为$T^\prime(x)$

发送端的数据生成为$$T(x)=B(x)+R(x)=Q(x)\cdot G(x)$$这个数据显然能够被$G(x)$整除，所以如果接收到的数据不能被整除，说明接收的数据有错误

接收端接收到的数据为$$T^\prime(x)=T(x)+E(x)$$其中$E(x)$指示通讯过程中可能发生的错误。

---

校验过程为$$\displaylines{\frac{T^\prime(x)}{G(x)}=\frac{B(x)}{G(x)}+\frac{R(x)}{G(x)}+\frac{E(x)}{G(x)} \\ =Q(x)+\frac{R(x)}{G(x)}+\frac{R(x)}{G(x)}+\frac{E(x)}{G(x)} \\ =Q(x)+\frac{E(x)}{G(x)}}$$所以如果$E(x)\neq 0$，即在校验过程中就会发现余数不为0，校验失败。

## 编码CRC

**第1步**：对于一个次数为r的Generation Polynomial$$G(x)=g_rx^r+g_{r-1}x^{r-1}+\cdots+g_1x+g_0$$
需要在原始的数据$B(x)$后加上$r$个0形成$B^\prime(x)$，这一步也就是$$B^\prime(x)=B(x)x^r$$
作用是防止余数与原始的数据冲突，因为$T(x)=B^\prime(x)+R^\prime(x)$

---

**第2步**：用$G(x)$去除$B^\prime(x)$：$$\frac{B^\prime(x)}{G(x)}=Q^\prime(x)+\frac{R^\prime(x)}{G(x)}$$

---

**第3步**：用于传输的数据为$$T(x)=B^\prime(x)+R^\prime(x)=Q^\prime(x)\cdot G(x)$$显然$T(x)$可以被$G(x)$整除，将$T(x)$传输出去

$T(x)=b_{k-1}b_{k-2}\cdots b_1b_0r_{r-1}r_{r-2}\cdots r_1r_0$，由k bit的数据位和r bit的校验位组成

## Analysis of CRC

略

## Selection of G(x)

略

## Cyclic Code Generation

### Polynomial Divisor Circuit

![[Pasted image 20250212014607.png#pic_75center|]]
如图，用这样的环形移位寄存器能够实现Modulo-2算法下的除法操作。

---

以$G(x)=x^4+x^3+1$为例，可以知道$g_0=1$，$g_1=0$，$g_2=0$，$g_3=1$，$g_4=1$，所以环形寄存器长这样：![[Pasted image 20250212020148.png#pic_75center|]]
对于$T(x)=11000001010=x^{10} + x^9 + x^3 + x$，除法过程为：![[DADKKWPOGJKA.png#pic_center|]]
$x^2+1$与$0101b$一样，所以这一切工作良好

####  Reducing the Number of Shifting Cycles

通过重新调整输入的位置，可以得到更加简化的形式。
![[Pasted image 20250212022706.png#pic_75center|]]
- The incoming bit string (MSB first) will be available at the output when the shifting starts, which is useful when working as a CRC encoding circuit.
- The above circuit works provided: $g_0=1$ and $g_r=1$

## CRC Encoding: Using (n-k) Stage Shift Register

至此，已经有用环形寄存器生成余数的例子。对于一个完整的CRC输出，需要有$k$ bit的数据位和$n-k$ bit的校验位，所以完整的结构很容易想到：![[Pasted image 20250212023739.png]]
在需要输出数据位的时候，开关被打到实线位置，此时$k$ bit的数据位被慢慢移位输出，同时也进入移位寄存器进行除法操作。$k$ bit后，开关被打到虚线位置，剩余的$n-k$ bit从移位寄存器中输出，即输出余数部分。
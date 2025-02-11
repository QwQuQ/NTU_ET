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
- 输入的x与y要求是互补的，会产生一个互补的输出。

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

#TODO 

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

# Hamming Code

- For an error correction, desirable to detect and locate error(s)
- 
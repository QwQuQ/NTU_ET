---
aliases: 
tags:
  - eda_tools
  - digital
  - testing
---
- Why test?
	- A correct design does not guarantee that the manufactured circuit will be operational
	- Manufacturing defects can occur during
		- impurities in the silicon crystal
		- misalignment
		- etching accuracy
	- Faults may be introduced during the **stress tests**
	- The later a fault is detected, the higher the cost
	- It is always cheaper to find a fault in a component than to find it in a system

# Defect Level

- Product quality is measured by Defect Level
- Defect Level is the number of defective parts in one million parts (ppm)
  百万分之一

# Design for Testability

- During the design phase, the designer has unlimited access to all the nodes in the circuit. Observation can be done at any desired node. This is not the case once the circuit is fabricated
  设计时，设计师能够无限制地掌握电路中的所有节点。可以检查任何希望的节点。但这并不是电路制造出来后的情况。
- A complex circuit such as a $\mathrm{\mu P}$ contains millions of transistors and uncountable states
  类似微处理器的复杂电路有数百万个晶体管和无数的状态
- It is impossible to go into a particular node and observe the circuit response
  不可能进入每个特定的节点来测量电路的响应的
- Design For Testability is very important
  为可测试性进行设计非常重要

# Test Categories

- Diagnostic test
	- to identify and locate the offending fault
	  识别和定位故障源
- Functional test (go/no go test)
	- to determine whether or not a manufactured component is functional. This is simpler than the diagnostic test since the only answer expected is YES or NO
	  确认一个部件是否正常工作。这比Diagnostic Test简单，因为只需要输出YES或NO
- Parametric test
	- to check on a number of nondiscrete parameters, such as noise margins, propagation delays, maximum clock frequencies, under a variety of conditions
	  在一系列条件下，确认一系列相关的参数，例如噪声容限、传播延时、最大时钟频率等。

# Test Issues

- Reduce the test time -> increase the throughput of the tester -> reduce test cost
- **Consider testing early in the design phase** will simplify the testing process
- **Exhaustive Testing Impossible**
  状态太多了，穷举是不可能的

# Testing Approach Premises
测试的前提

- Exhaustive testing contains substantial amount of redundancy, i.e. a single fault is covered by a number of test patterns
  穷经测试包含大量冗余，这使得一个故障能够被许多测试例覆盖
- Number of test patterns can be reduced by relaxing the condition that all faults must be detected. e.g. detect the last 1% of possible faults may require much more patterns and hence high cost. The replacement cost may be lower.
- Typical test only attempts a 95-99% coverage


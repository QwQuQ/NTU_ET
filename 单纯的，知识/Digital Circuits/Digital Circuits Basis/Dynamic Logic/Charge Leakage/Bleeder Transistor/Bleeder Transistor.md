---
aliases:
  - 泄漏晶体管
tags:
  - digital_circuits
  - dynamic_logic
---
![[Bleeder Transistor.png]]
在[[Dynamic Logic|动态逻辑]]求值器件，由于输出节点处于高阻状态，因此引起了漏电。漏电问题可以通过降低求值期间输出节点上的输出阻抗来解决。这个泄露晶体管是一个伪NMOS类型的上拉器件，用来补偿下拉路径造成的[[Charge Leakage|电荷泄露]]。
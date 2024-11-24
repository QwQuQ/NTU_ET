---
aliases:
  - 二极管I-V关系
  - Diode Equation
  - p-n junction current equation
tags:
  - semi_conductor
  - analog
  - pn_junction
  - diode
---
$$I=I_S\left(e^{\frac{V_F}{V_T}}-1\right)$$
上式中：
- $I_S$为二极管饱和电流
- $V_T$为[[Thermal Voltage|热电压]]
- $V_F$为施加在pn结上的电压，有的地方也是$V_D$

正偏的时候势垒高度降低，反偏的时候势垒高度增高

如果二极管有串联等效电阻$R_S$，表达式变为：$$I=I_S\left(e^{\frac{V_F-IR_S}{V_T}}-1\right)$$
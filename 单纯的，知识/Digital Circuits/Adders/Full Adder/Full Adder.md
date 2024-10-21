---
aliases:
  - 全加器
tags:
  - Adder
---
# 表达式
$$s=a\oplus b \oplus c_i$$
$$c_o=ab+bc_i+ac_i$$
# 真值表

| $a$ | $b$ | $c_i$ | $s$ | $c_o$ |
| :-: | :-: | :---: | :-: | :---: |
|  0  |  0  |   0   |  0  |   0   |
|  0  |  0  |   1   |  1  |   0   |
|  0  |  1  |   0   |  1  |   0   |
|  0  |  1  |   1   |  0  |   1   |
|  1  |  0  |   0   |  1  |   0   |
|  1  |  0  |   1   |  0  |   1   |
|  1  |  1  |   0   |  0  |   1   |
|  1  |  1  |   1   |  1  |   1   |
# 全加器的反相特性（Inverting Property of Adder Cell）
全加器的输入和输出全部反向并不影响性质。
$$\overline{s}(a,b,c_i)=s(\overline{a},\overline{b},\overline{c_i})$$
$$\overline{c_o}(a,b,c_i)=c_o(\overline{a},\overline{b},\overline{c_i})$$
根据这一性质可以设计[[Complementary Static CMOS Full Adder Cell]]
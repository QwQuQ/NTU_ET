---
aliases:
  - 桶形移位器
tags:
  - shifter
  - digital
  - arthmetic_modules
---
![[Pasted image 20241021204249.png|Barrel Shifter]]

[[Pasted image 20241104071124.png#pic_center|希望这个图更好理解一点]]

- Built from array of transistors
  由晶体管阵列构成
- Number of rows = word length
  行数 = 字长
- Number of columns = maximum shift width
  列数 = 最大移位宽度
- Advantage: Signal passes 1 transmission gate. So delay is constant for any shift
  优点：信号经过 1 个传输门，因此任何移位的延迟是恒定的。
- Decoder usually needed for control signals (n signals)
  解码器通常用于控制信号（n个信号）
- 可以实现符号位的补充

|     | B3  | B2  | B1  | B0  |
| :-: | :-: | :-: | :-: | :-: |
| Sh0 | A3  | A2  | A1  | A0  |
| Sh1 | A3  | A3  | A2  | A1  |
| Sh2 | A3  | A3  | A3  | A2  |
| Sh3 | A3  | A3  | A3  | A3  |

# Layout

![[Pasted image 20241104064335.png]]

# Left-Rotation Linear Barrel Shifter

可以将输入数据的位向左旋转（即将位移出左边界的位重新放入右边界）

![[Pasted image 20241104064847.png|PPT上的抽象图]]

![[Pasted image 20241104071205.png#pic_center|希望这个图更好理解一点]]
---
aliases:
  - 对数移位器
tags:
  - shifter
---
以对数形式运行的移位器，每一级可以移$2^n$位，所以省略了解码器。每一级可以被设置为移位模式和通过模式，级数为$log_2M$，
# 优势
- Control signals are in encoded form, hence, less control signals.
- No decoder is needed
- More effective than barrel shifter for large shift values.
- Smaller in area and faster in speed than barrel shifter.
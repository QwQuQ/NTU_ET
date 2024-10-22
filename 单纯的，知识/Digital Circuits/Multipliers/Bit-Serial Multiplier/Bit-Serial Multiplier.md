---
aliases:
  - 串行乘法器
tags:
  - multiplier
  - digital_circuits
---
![[Bit-Serial Multiplier.png]]

用竖式模拟二进制乘法完成计算。

与门用来产生[[Partial Products|部分积]]：
```verilog
and_out = M & {6{Q[0]}};
```

对于$M$位与$N$位数相乘，最终需要$N$个周期完成计算。

Verilog代码（为了验证手搓的）
```verilog
module multiplier(
input clk,
input n_rst,
input [5:0]M,
input [3:0]N,
output reg [9:0]Q
);

wire [5:0] and_out;
assign and_out = M & {6{Q[0]}};

wire [6:0] adder_out;
assign adder_out = Q[9:4] + and_out;

always@(posedge clk) begin
	if(n_rst==0) begin
		Q <= {6'd0, N};
	end else begin
		Q <= {adder_out, Q[3:1]};
	end
end
endmodule
```
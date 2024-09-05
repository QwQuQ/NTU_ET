# 平行板传输线/TEM小室/GTEM小室

## 平行板传输线

<div align=center>
<img src="平行板.bmp" width=70%>
<br>
<div>平行板传输线</div>
<br>
</div>

平行板传输线中电磁波传播的模式是TEM波，与远场中电磁波的传输模式相同。

通常Stripline地层最大是信号层的3倍宽，在末端会用与特性阻抗相同大小的电阻连接以消除反射（传输线阻抗匹配）。在锥形部分时，信号层的宽度和高度始终维持 $\frac{w}{h}=2$ 的关系。

### 平行板传输线相关公式

#### 传输线单位长度的电容和电感：

$$C_l=\frac{\epsilon_r \epsilon_0 w}{h}\left(F/m\right)$$

$$L_l=\frac{\mu_r \mu_0 h}{w}\left(H/m\right)$$

（空气近似于自由空间， $\epsilon \approx 1$ ）

#### 相速度

$$v_p=\frac{1}{\sqrt{C_l L_l}}=\frac{1}{\sqrt{\epsilon_r \epsilon_0 \mu_r \mu_0}}$$

#### 特征阻抗

$$\eta=\sqrt{\frac{\mu_r \mu_0}{\epsilon_r \epsilon_0}}$$

自由空间下的特征阻抗（空气或者真空）：

$$Z_0=\eta_0\frac{h}{w}\left(\Omega\right)$$
对于带状线：

$$Z_0 \approx \frac{\eta_0}{\frac{w}{h}+2}$$

如果其中的电介质是不色散的，那么传输线的特征阻抗和频率无关。

#### 插入损耗

插入损耗可以用匹配网络前后的电压值计算。

$$\mathrm{Insertion\ Loss}=20log\frac{V_1}{V_2}$$

如果使用电阻分压网络，只需要计算前后电阻的分压值即可获得插入损耗。（其实就是前后功率的损耗）

#### 电阻匹配网络的电阻计算

<div align="center">
<img src="电阻匹配网络.bmp" width=40%>
<br>
<div>电阻匹配网络</div>
<br>
</div>

针对这种类型的电阻匹配网络，只需要保证

$$
\begin{cases}
    Z_{in}=R_2 || \left(R_1+Z_0\right) \\
    Z_0=R1+Z_{in} || R_2
\end{cases}
$$

解这个二元方程组就能够得到 $R_1$ 、 $R_2$ 的值。

如果引入一个辅助值

$$Z^{'}=1-\frac{Z_{in}}{Z_0}$$

那么可以计算得到

$$
\begin{cases}
    R_1=Z_0\sqrt{Z_{'}} \\
    R_2=\frac{Z_{in}}{\sqrt{Z_{'}}}
\end{cases}
$$

### 平行板传输线的优势与劣势

#### 优势

架设容易

成本低

没有频率限制

#### 劣势

自身的电场容易被周围的物体或者电磁传输干扰

如果产生高电场可能会对周围的设备产生干扰

## TEM CELL（TEM小室）

这玩意长得像个放大版的同轴线，然后把待测物体放到这个同轴线里面。内部是个平行板，外部被屏蔽壳包裹，平行板与外壳用介电系数尽可能接近于1的电介质隔开。电磁波传播模式也是TEM模。

<div align=center>
<img src="TEMCELL.png" width=70%>
<br>
<div>TEM CELL</div>
<br>
</div>

### TEM CELL相关公式

<div align=center>
<img src="TEMCELL2.png" width=70%>
<br>
<div>TEM CELL的横截面</div>
<br>
</div>

#### 特征阻抗

$$Z_0 \approx \frac{\eta_0}{4\left\{\frac{a}{b}-\frac{2}{\pi}ln\left[sinh\left(\frac{\pi g}{b}\right)\right]\right\}}\ \left(\Omega\right)$$

其中

#### 

# 开放地带

# 电波暗室

#

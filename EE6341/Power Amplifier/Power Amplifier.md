# Q Point
在$\beta$比较大时，$I_C \approx I_E$，$V_{CE}=V_{CC}-I_C\left(R_C+R_E\right)$
![[Power Amplifier Fig1.png|400]]
DC Load Line的两个端点分别为：$V_{CE}=0$，$I_C=\frac{V_{CC}}{\left(R_C+R_E\right)}$；$I_C=0$，$V_{CE}=V_{CC}$
为了让输出摆率取到最大，偏置点需要取在DC Load Line的中点。

# Q Point的计（估）算：

为了让Q-Point尽可能位于直流负载线的中心，可以让
$$V_{CEQ}=\frac{V_{CC}}{2}$$
这样在三极管饱和区足够小的时候，可以认为此时的Q-Point位于直流负载线的中心。

根据$V_{CE}=V_{CC}-I_C\left(R_C+R_E\right)$可以求解得到：
$$I_{CQ}=\frac{1}{2}\times\frac{V_{CC}}{\left(R_C+R_E\right)}$$

$I_{BQ}=\frac{I_{CQ}}{\beta}=\frac{V_{CC}}{2\beta\left(R_C+R_E\right)}$
$V_{th}=V_{CC}\frac{R_2}{R_1+R_2}=I_{BQ}R_{th}+V_{BE}+\left(\beta+1\right)I_{BQ}R_E$


考虑麦克斯韦方程组的时谐形式：
$$
\begin{cases}
    &\nabla\times \mathbf{E}= -j\omega \mathbf{B} \\
    &\nabla\times \mathbf{H}= j\omega \mathbf{D}+\mathbf{J} \\
    &\nabla \cdot \mathbf{B}= 0 \\
    &\nabla \cdot \mathbf{D}= \rho \\
    &\nabla \cdot \mathbf{J}= j \omega \rho
\end{cases}
$$

物质的本构关系：
$$
\begin{cases}
    &\mathbf{D}=\epsilon\mathbf{E}\\
    &\mathbf{B}=\mu\mathbf{H}\\
    &\mathbf{J}=\sigma\mathbf{E}
\end{cases}
$$

$$\nabla \times \nabla \times \mathbf{E}=\nabla\left(\nabla \cdot \mathbf{E}\right)-\nabla^2\mathbf{E}$$

由于导体中场的特性为：无散、无旋、无源， $\nabla\left(\nabla \cdot \mathbf{E}\right)=0$ ，可以得到：
$$\nabla \times \nabla \times \mathbf{E}=-\nabla^2\mathbf{E}$$

根据麦克斯韦方程组 $\nabla\times \mathbf{E}= -j\omega \mathbf{B}$ 有：
$$\nabla \times \nabla \times \mathbf{E}=\nabla \times \left(-j\omega\mathbf{B}\right)$$

代入物质的本构关系 $\mathbf{B}=\mu\mathbf{H}$ 和麦克斯韦方程组 $\nabla\times \mathbf{H}= j\omega \mathbf{D}+\mathbf{J}$ ：
$$\nabla \times \nabla \times \mathbf{E}=-j\omega\mu\nabla \times \mathbf{H}=-j\omega\mu\left(j\omega\mathbf{D}+\mathbf{J}\right)$$

由于是在导体中，所以 $j\omega\mathbf{D}=0$ ，代入本构关系 $\mathbf{J}=\sigma\mathbf{E}$ 从而得到：
$$\nabla \times \nabla \times \mathbf{E}=-j\omega\mu\sigma \mathbf{E}$$

所以可以得到：
$$\nabla^2\mathbf{E}=j\omega\mu\sigma \mathbf{E}$$

此时就得到了亥姆霍兹方程（在后面EMI的部分也大量出现）

亥姆霍兹方程的解为电磁波的传播方程，对于电场，它的形式为：$$\mathbf{E}=\mathbf{E_0}e^{-\mathbf{k}\cdot r}$$

令指数上的 $\mathbf{k}$ 为电磁场的复传播系数，规定其**一般形式**为
$$\gamma=\alpha+j\beta=\sqrt{j\omega\mu\left(\sigma+j\omega\epsilon\right)}$$

其中的 $\alpha$ 为衰减系数， $\beta$ 为相位系数（ $\beta$ 是与波数 $k$ 相关的，在无耗介质（真空、空气）中是老印提到的 $\beta_0=\frac{2\pi}{\lambda}$ ）

在导体中，省略介电项，可以得到在导体中的电磁场传播系数为：
$$\gamma=\sqrt{j\omega\mu\sigma}$$

根据趋肤效应的定义，场强减小到 $\left|\mathbf{E_0}\right|$ 的 $e^{-1}$ 时，此时的距离规定为趋肤深度：
$$\left|\mathbf{E_0}e^{-\mathbf{\gamma\cdot}r}\right|=\left|\mathbf{E_0}e^{-1}\right|$$

解得： 
$$r=\left|\sqrt{\frac{2}{\gamma}}\right|=\sqrt{\frac{2}{\omega\mu\sigma}}=\sqrt{\frac{1}{\pi f \mu\sigma}}$$
---
aliases:
  - 漂移电流密度
---
电子漂移电流密度：$$J_{n,drift}=qn\mu_n E$$
空穴漂移电流密度：$$J_{p,drift}=qp\mu_pE$$
式中的$\mu_n$和$\mu_p$为[[Carrier Mobility|载流子迁移率]]，要注意的是$J_{n,drift}$和$J_{p,drift}$都是正的（很好理解，相同电场下空穴和电子的电流方向是一样的）。

推导：
在没有外加电场的时候，载流子的静速度是0（随机运动）
平均自由程Mean free path: $l$，两次碰撞之间的平均距离
平均自由时间Mean free time: $\tau$，两次碰撞之间的平均时间

施加电场$E$，载流子[[Effective Mass|有效质量]]为$m^*$: 
加速度：$a=-\frac{qE}{m^*}$
漂移速度：$v_D=-\frac{qE\tau}{m^*}$

电流密度：$J_{drift}=-qnv_d=\frac{qnq\tau E}{m^*}$
定义$\mu=\frac{q\tau}{m^*}=\frac{v_D}{E}$为[[Carrier Mobility|载流子迁移率]]，有$$J_{drift}=qn\mu E$$

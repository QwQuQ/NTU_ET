# �ź�����IM

����������ģ���Ҫ������Example3��4���������漰����֪ʶ�㡣���Ƚ�һ���շ������ź���·����Ȼ��������������ץϹ��

## Example3���շ������ź���·����

A HF transceiver and a VHF transceiver (both $\mathrm{50\Omega}$) are to operate close to each other. The specifications of the two transceivers are shown in the table. With a separation distance of $100m$, and assuming that the antennas are placed at the same height with maximum coupling, identify the various interference cases and compute the interference margins when the HF is operating at $\mathrm{10MHz}$ and the VHF is operating at $\mathrm{35MHz}$.

��������һ����򻯵ķ�������յ��ź���·������Friss Transfer Function��˳����з���

<center>
<img src="�ź���·.png">
<br>
<div>�ź���·ͼ</div>
<br>
</center>

### ����˷��书��$P_t$

����˾��������ϱ�Ƶ����Ƶ���˳������Ƶ�ʷ�������߿��ǵ�ģ�Ͷ�������Ƶ�ģ�������ͽ�������߹��������߽��з��䡣����Ƿ�����ź��߹���·������Example3��HF���ߵ���������������һ�·���������ԣ���ʱ�������պͷ�һ���ģ�ͣ�̫���ˣ���

<center>
<img src="example3_fig1.png">
</center>

������2-30MHz������ζ����Ƶ���ֵĹ������������ܹ���2-30MHz�������˲��������š����߶��ܹ�֧��2-30MHz�ķ��䡣�����Ƶ�ʷ�Χ��Ե���Ȼ�������Bandwidth=25kHz����һ�����Ƿ������ʵʱ����Ҳ����˵����Ȼ�ز�Ƶ���ܹ���2-30MHz��Χ�ڵ�������ͬһʱ�̵�Ƶ�׿��ֻ��25kHz.

<center>
<img src="�����Ƶ��1.png" width=60%>
<br>
<div>�����Ƶ��</div>
<br>
</center>

##### ���һ���$dB$

Ҫ��ס����ֻ��$dBm$������Ǿ��Թ��ʣ�����������ԵĹ��ʣ�Ҳ��˵$dB$�ǵļ�������$dBm$������$dBm$ȥ���⻰��ô�ֵֹģ���$dBc$�������������Ƶ�ʵĲ�ֵ��$dBi$���������ܹ���ߵ����棬·�����ֱ������$dB$û�к�׺������ֻҪ��ס����$m$�Ķ������ֵ��������һ������ֵ��Ϊ���ղ�����Ϊ���յĽ����

##### ���������ӡ���Ի�·��Spurious Level

������ӡ��˼·����������յ�Spurious Level��ʵ��Ҫ�ֿ����ġ���һ���Ҿ������ǰѷ���ʱ�������׺ͽ���ʱ�±�Ƶ��ĵ�ͨ�˲������ԣ���Ҫ֪�������ͨ�˲�����ô���ĵô��̹ſ���ٵؿ�ʼ˵���ˣ�����һ���ˣ��������ʱ����Ҫ��������շֿ����ǡ�

<center>
<img src="����Spurious.png" width=100%>
<br>
<div>��������յ�Spurious��֮ͬ�����ҵ���⣩</div>
<br>
</center>

��ô�ڷ�������Ǿ��ܸ����ز����书��$5W$���н�ģ����һ����֪��$5W$����$37dBm$����ô���ܹ�����г������ɢ����ֵ��������˲������������Ƶ�ס���ӡ����г���Ľ�ģ������г���������ʾ���ȣ�ʵ�������ǲ��Եġ���֮�����������Ͷ��ˡ�

<center>
<img src="����Ƶ��.png" width=60%>
<br>
<div>�����û�������������������Ƶ��</div>
<br>
</center>

����$-52dBc$��$-32dBc$���ҵĿ����ǲ�Ҫ���Ⱦ��������ǵķ��ţ���ʱ����ῴ������ǰ�沢û�и��ţ����Ⲣ��Ӱ�����ǻ���Ƶ��ͼ����Ϊг���������׵�ֵ�϶���С���ز������ģ�����ֻ��Ҫ֪�������СȻ�����Ӽ����Ϳ����ˡ�

### �������������$G_t$

�����������棬��ӡ�Ľ�ģ˼·�����ߴ��ڵ����治�䣬�����������Ҫ����Ƶ�ʽ��мƣ������㡣�������ֺ��������ˣ�������ô���ģ��Ҵ���ֱ�Ӽ��㡣dipole��һ�µ�PPT���е�����ġ�

��ӡ�Լ��õ�dipole��ʽӦ���������

$$F\left(\theta,\phi\right)=\frac{cos\left(\beta_0 L cos\theta\right)-cos\left(\beta_0 L\right)}{sin\theta}$$

�����ǣ�

$$F\left(\theta,\phi\right)=\frac{sin\left(\beta_0 L cos\theta\right)}{\beta_0 L cos\theta}sin\theta$$



## Example4


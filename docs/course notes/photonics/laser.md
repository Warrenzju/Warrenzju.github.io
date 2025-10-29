# 激光放大器

## 一、激光放大器的增益

光子流密度（单位面积单位时间的光子流）：
$$
\phi(z)=\frac{I(z)}{h\nu}
$$
受激吸收，单位体积单位时间减少的光子数为$N_1W_i$
受激辐射，单位体积单位时间增加的光子数为$N_2W_i$
$$
d\phi=NW_idz
$$

$$
\frac{d\phi}{dz}=NW_i=N\phi(z)\sigma(\nu)=\gamma(\nu)\phi(z)
$$

定义增益系数（每单位介质长度光子流密度净增益）：
$$
\gamma(\nu)=N\sigma(\nu)=N\frac{\lambda^2}{8\pi t_{sp}}\text{g}(\nu)\tag{1-1}
$$
所以位置z处的光子流密度为：
$$
\phi(z)=\phi(0)e^{\gamma(\nu)z}
$$
光强为：
$$
I(z)=I(0)e^{\gamma(\nu)z}
$$
长度为d的激光放大器的总增益为
$$
G(\nu)=\frac{I(d)}{I(0)}=e^{\gamma(\nu)d}
$$
具有洛伦兹线形函数的增益介质的相移系数为：
$$
\phi(\nu)=\frac{\nu-\nu_0}{\Delta \nu}\gamma(\nu)
$$

## 二、速率方程

## （1） 无辐射

能级1和能级2的粒子数密度增加速率如下
$$
\frac{dN_2}{dt}=R_2-\frac{N_2}{\tau_2}
$$

$$
\frac{dN_1}{dt}=-R_1-\frac{N_1}{\tau_1}+\frac{N_2}{\tau_{21}}
$$

稳态时$(N=N_2-N_1)$
$$
N_0 = R_2 \tau_2 \left( 1 - \frac{\tau_1}{\tau_{21}} \right) + R_1 \tau_1\tag{2-1}
$$
$N_0$表示无辐射时的稳态粒子数差
由$(1-1)$可知获得大的增益系数需要大的$N_0$，所以由（2-1）可知要获得大的$N_0$需满足以下条件

- 大的$R_1$和$R_2$
- 长的$\tau_2$
- 小的$\tau_1$

理想情况下，应有$\tau_{21}\approx t_{sp}\ll\tau_{20}$，所以$\tau_2\approx t_{sp}$，$\tau_1\ll t_{sp}$
所以上式可化为
$$
N_0\approx R_2t_{sp}+R_1\tau_1
$$
如果$R_1=0$
$$
N_0\approx R_2t_{sp}
$$


## （2）有辐射

共振频率$\nu_0$附近辐射的存在使得能级1和能级2之间发生受激吸收和辐射等跃迁
$$
\frac{dN_2}{dt}=R_2-\frac{N_2}{\tau_2}-N_2W_i+N_1W_i
$$

$$
\frac{dN_1}{dt}=-R_1-\frac{N_1}{\tau_1}+\frac{N_2}{\tau_{21}}+N_2W_i-N_1W_i
$$

稳态时：
$$
N = \frac{N_0}{1 + \tau_s W_i}
$$

$$
\tau_s = \tau_2 + \tau_1 \left(1 - \frac{\tau_2}{\tau_{21}}\right)
$$

因为$\tau_2\le\tau_{21}$，所以$\tau_s$大于0，所以有辐射时的粒子数差总是比无辐射时的稳态粒子数差小；N随$W_i$的增大单调递减趋于0，在$W_i$为$1/\tau_s$时，稳态粒子数差减为无辐射时的一半

## 三、四能级泵浦机制

在此情况下以速率R将原子从能级0泵浦到能级3，所以有$R_2=R$，$R_1=0$，所以
$$
N_0 = R \tau_2 \left( 1 - \frac{\tau_1}{\tau_{21}} \right)
$$
在大多数四能级系统中，能级2到能级1的非辐射跃迁可以忽略，$(t_{sp} \ll \tau_{nr}) \ \text{and} \ \tau_{20} \gg t_{sp} \gg \tau_1$，so
$$
N_0\approx Rt_{sp}
$$

$$
\tau_s\approx t_{sp}
$$

所以
$$
N \approx \frac{R t_{sp}}{1 + t_{sp} W_i}
$$
考虑泵浦速率和反转粒子数相关，假设总的原子密度为$N_a$。
$$
N_g + N_1 + N_2 + N_3 = N_a \quad \text{and} \quad N_1 ≈ N_3 ≈ 0
$$
（能级1和3是短寿命的）

则处于基态的粒子数密度为，

$$
N_g ≈ N_a - N_2 ≈ N_a - N
$$
泵浦涉及一个从基态到能级3的跃迁，假设其跃迁概率密度为W，则

$$
R ≈ (N_a - N)W
$$
泵浦速率R为随反转粒子数差N线性减少的函数，并不独立于N

代入上式并整理可得

$$
N ≈ \frac{t_{sp} N_a W}{1 + t_{sp} W_i + t_{sp} W}
$$

上式进一步整理可得  

$$
N = \frac{N_0}{1 + \tau_s W_i}
$$

其中 

$$
N_0 \approx \frac{t_{sp} N_a W}{1 + t_{sp} W} \quad \tau_s \approx \frac{t_{sp}}{1 + t_{sp} W}
$$

- 在弱泵浦条件下($W \ll 1/t_{sp}$)，$N_0 \approx t_{sp} N_a W$，正比于$W$（泵浦跃迁概率密度），$\tau_s \approx t_{sp}$，和前面结果相同

- 当泵浦增强时，$N_0$饱和（趋向于$N_a$），$\tau_s$降低

## 四、三级泵浦机制

外部能量源以速率R将原子从能级1泵浦到能级3，能级3快速弛豫到能级2，所以有
$$
R_1=R_2=R \ \ \text{and}\ \ \tau_2=\tau_{21},\tau_1=\infty
$$
代入原始的速率方程可得
$$
0 = R - \frac{N_2}{\tau_{21}} - N_2 W_i + N_1 W_i
$$
令
$$
N_1 + N_2 = N_a 
$$
所以
$$
N_0=2R\tau_{21}-N_{a}
$$

$$
\tau_s=2\tau_{21}
$$

同时因为能级2到能级1得非辐射跃迁速率可以忽略，所以
$$
N_0\approx2Rt_{sp}-N_{a}
$$

$$
\tau_s\approx2t_{sp}
$$

在三能级系统中，基态的高粒子数集聚从本质上成为取得粒子数反转的障碍，而四能级不存在这种障碍

由 $N_1 + N_2 + N_3 = N_a$, $N = N_2 - N_1$, 以及 $N_3 \approx 0$, 可得 $N_1 = \frac{1}{2}(N_a - N)$

从 $R \approx (N_1 - N_3)W$, $N_3 \approx 0$ 可得 $R \approx \frac{1}{2}(N_a - N)W$

代入 
$$
N = (2Rt_{sp} - N_a)/(1 + 2t_{sp}W_i)
$$
可得 
$$
N = \frac{N_0}{1 + \tau_s W_i}
$$
 此时 
$$
N_0 = \frac{N_a(t_{sp}W - 1)}{1 + t_{sp}W}
$$

$$
\tau_s = \frac{2t_{sp}}{1 + t_{sp}W}
$$

## 五、增益系数

将 $$ W_i = \phi\sigma(\nu) $$ 代入粒子数密度公式：

$$
N = \frac{N_0}{1 + \tau_s W_i}
$$

可得：

$$
N = \frac{N_0}{1 + \phi / \phi_s (\nu)}
$$

其中饱和光子流密度定义为：

$$
\frac{1}{\phi_s (\nu)} = \tau_s \sigma(\nu) = \frac{\lambda^2 \tau_s}{8\pi t_{sp}} g(\nu)
$$

代入增益系数表达式：

$$
\gamma(\nu) = N\sigma(\nu) = N \frac{\lambda^2}{8\pi t_{sp}} g(\nu)
$$
最终得到**均匀加宽介质的饱和增益系数**：

$$
\gamma(\nu) = \frac{\gamma_0 (\nu)}{1 + \phi / \phi_s (\nu)}
$$

其中：

- $$\gamma_0 (\nu) = N_0 \sigma(\nu) = N_0 \frac{\lambda^2}{8\pi \tau_{sp}} g(\nu)$$ 为**小信号增益系数**
- $$\phi_s(\nu)$$ 为**饱和光子流密度**
- $$\phi$$ 为实际光子流密度



位置 $z$ 处，单位长度光子流密度的增加量：

$$
d\phi = \gamma \phi dz
$$

代入饱和增益系数 $\gamma(\nu) = \dfrac{\gamma_0 (\nu)}{1 + \phi / \phi_s (\nu)}$，得到：

$$
\frac{d\phi}{dz} = \frac{\gamma_0 \phi}{1 + \phi / \phi_s}
$$

将方程重写为：

$$
\left( \frac{1}{\phi} + \frac{1}{\phi_s} \right) d\phi = \gamma_0 dz
$$

积分可得：

$$
\ln \frac{\phi(z)}{\phi(0)} + \frac{\phi(z) - \phi(0)}{\phi_s} = \gamma_0 z
$$

因此，放大器的输入光子流密度 $\phi(0)$ 和输出 $\phi(d)$ 光子流密度的关系可表示为：

$$
[\ln(Y) + Y] = [\ln(X) + X] + \gamma_0 d
$$

其中：

- $X = \phi(0) / \phi_s$
- $Y = \phi(d) / \phi_s$
- $X$ 和 $Y$ 为归一化到饱和光子流密度的输入和输出光子流密度

**小信号近似情况**

当 $X$ 与 $Y$ 都远小于 1 时（即光子流密度远小于饱和光子流密度），关系式可简化为：

$$
\ln Y = \ln X + \gamma_0 d
$$

即：

$$
Y = X \exp(\gamma_0 d)
$$

此时为线性关系，称为**小信号近似**。

**大信号情况**

当 $X$ 远大于 1 时（即输入光子流密度远大于饱和光子流密度），关系式可简化为：

$$
Y = X + \gamma_0 d
$$

即：

$$
\phi(d) = \phi(0) + \frac{N_0 d }{\tau_s}
$$

此时输出光子流密度随长度线性增长，称为**大信号情况**。

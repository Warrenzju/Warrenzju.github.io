# 半导体

## 1.能量和动量的关系

$$
E = \frac{p^2}{2m_0} = \frac{\hbar^2 k^2}{2m_0}
$$

$$
p=\hbar k
$$

导带中的电子能量不仅取决于该电子动量的大小还取决于该电子在晶体中的运动方向
fig

在导带底部附近，E-k关系可以用抛物线近似表示
$$
E = E_c + \frac{\hbar^2 k^2}{2m_c}
$$

$$
E = E_v - \frac{\hbar^2 k^2}{2m_v}
$$

$m_c,m_v$表示导带中电子和价带中空穴的有效质量，有效质量取决于晶体取向和所考虑的能带

## 2. 态密度

定义：所允许的能级的密度

能量E和K是一一对应的关系
$$
\rho(E)dE=\rho(k)dk
$$

$$
\rho(k)=\frac{k^2}{\pi^2}
$$

所以

$$
\rho_c(E) = \frac{(2m_c)^{3/2}}{2\pi^2\hbar^3}(E-E_c)^{1/2}, E \ge E_c
$$

$$
\rho_v(E) = \frac{(2m_v)^{3/2}}{2\pi^2\hbar^3}(E_v - E)^{1/2}, E \le E_v
$$

态密度在能带边缘处为0，并且随着远离边缘以一定速率增加

电子占据能量E的概率由费米函数决定：
$$
f(E) = \frac{1}{\exp[(E - E_f)/k_B T] + 1}
$$
$E_f$为占据概率为1/2的能级

## 3. 热平衡时载流子浓度

根据态密度和占据概率即可计算
$$
n(E) = \rho_c(E)f(E)
$$

$$
p(E) = \rho_v(E)[1-f(E)]
$$

$$
n = \int_{E_c}^{\infty} n(E)dE
$$

$$
p = \int_{-\infty}^{E_v} p(E)dE
$$

当费米能级位于带隙内且，距离边缘至少有几倍的能量时，采用近似
$$
f(E)=\exp[-(E - E_f)/k_B T
$$

$$
1-f(E)=f(E)=\exp[-(E_f - E)/k_B T
$$

可得
$$
n = N_c \exp(-\frac{E_c - E_f}{k_B T})
$$

$$
p = N_v \exp(-\frac{E_f - E_v}{k_B T})
$$

$$
np = N_c N_v \exp(-\frac{E_g}{k_B T})
$$

其中

$$
N_c = 2(2\pi m_c k_B T / h^2)^{3/2}
$$

$$
N_v = 2(2\pi m_v k_B T / h^2)^{3/2}
$$

## 4. 质量作用定律

$$
np = N_c N_v \exp(-\frac{E_g}{k_B T}) = 4(\frac{2\pi k_B T}{h^2})^3 (m_c m_v)^{3/2} \exp(-\frac{E_g}{k_B T})
$$

$$
n_i \approx (N_c N_v)^{1/2} \exp(-\frac{E_g}{k_B T})
$$

所以
$$
np=n_i^2
$$
其乘积和费米能级在带隙中的位置和半导体的掺杂程度无关，可以用于确定掺杂半导体的浓度
如果费米能级位于导带或价带内部，费米能级的指数近似关系就不适用，所以
$$
np\neq{n_i}^2
$$

## 5.载流子的产生、复合及注入

复合分为辐射复合和非辐射复合
$$
复合速率=\epsilon np
$$
参数$\epsilon$取决于材料特性

热平衡时复合速率等于产生速率，设产生速率为$G_0$
$$
G_0=\epsilon n_0p_0
$$
通过外部注入以速率R产生额外的电子-空穴对，从而建立起新的稳态
$$
G_0+R=\epsilon np
$$
其中
$$
n = n_0 + \Delta n, \quad p = p_0 + \Delta p
$$
可得
$$
\mathrm{R} = \frac{\Delta n}{\tau}
$$

$$
\tau = \frac{1}{\varepsilon [(n_0 + p_0) + \Delta n]}
$$

$\tau$为额外载流子的复合寿命

当注入速率较弱时即$\Delta n<<n_0+p_0$时，
$$
\tau = \frac{1}{\varepsilon (n_0 + p_0) }
$$
在 n 型材料中，当n0>>p0时，复合寿命 τ≈1/εno 与电子浓度成反比。类似地，对于 p 型材料，τ≈1/εp0 。当陷阱在过程中起重要作用时，这种简单的公式并不适用。

注入载流子浓度满足
$$
\frac{d\Delta n}{dt}=R-\Delta n\tau
$$
稳态时$\frac{d\Delta n}{dt}=0$，可得到上述相似结果，如果在$t_0$时撤去注入源，则$\Delta n$将以指数$\tau$衰减

可得
$$
\Delta n(t)=\Delta n(t_0)\exp{[-(t-t_0)/\tau]}
$$
如果在强注入条件下，寿命和$\Delta n$有关，其就不按指数衰减

内部量子效率定义为
$$
\eta_i = \frac{\varepsilon_r}{\varepsilon} = \frac{\varepsilon_r}{\varepsilon_r + \varepsilon_{nr}} = \frac{\tau}{\tau_r} = \frac{\tau_{nr}}{\tau_r + \tau_{nr}}
$$
对于低到中等注入速率，

$$
\tau_r \approx \frac{1}{\varepsilon_r (n_0 + p_0)}
$$

## 6. 带间吸收和发射

只有当光子能量大于带隙能量的时候才能发射
$$
\lambda_g=\frac{hc_0}{eE_g}=\frac{1.24}{E_g}
$$
波长单位为微米，能量单位为eV
吸收和发射要满足能量守恒和动量守恒
$$
E_2-E_1=h\nu
$$

$$
p_2 - p_1 = h v / c = h / \lambda 
$$

$$
k_2 - k_1 = 2\pi / \lambda
$$

代入前面E-k的关系，且因为$h/\lambda$的大小相比动量可以忽略所以要求
$$
k_1\approx k_2
$$
可得
$$
E_2 = E_c + \frac{m_r}{m_c} (h\nu - E_g)
$$

$$
E_1 = E_v - \frac{m_r}{m_v} (h\nu - E_g) = E_2 - h\nu
$$

光学联合态密度：直接带隙半导体中与能量$h\nu$的光子相互作用的能态密度，即单位体积内单位频率的能态数
$$
\rho(\nu) = \frac{(2m_r)^{3/2}}{\pi \hbar^2} (h\nu - E_g)^{1/2}, h\nu \ge E_g
$$
间接带隙半导体一般不会发生光子辐射，但会发生光子吸收

## 7.吸收率和发射率

### 1.占据概率

$$
f_e(\nu) = f_e(E_2)[1 - f_v(E_1)]
$$

$$
f_a(\nu) = [1 - f_c(E_2)]f_v(E_1)
$$

跃迁截面：
$$
\sigma(\nu)=\frac{\lambda^2}{8\pi\tau_r}g(\nu)
$$
自发辐射的概率密度
$$
P_{sp}(\nu)d\nu = \frac{1}{\tau_r} g(\nu)d\nu
$$
受激辐射的概率密度
$$
W_i(\nu)d\nu = \phi_v \sigma(\nu)d\nu = \phi_v \frac{\lambda^2}{8\pi \tau_r} g(\nu)d\nu
$$

### 2.自发辐射、受激辐射和吸收的速率

$$
r_{sp}(\nu) = \frac{1}{\tau_r} \rho(\nu) f_e(\nu)
$$

$$
r_{st}(\nu) = \phi_{\nu} \frac{\lambda^2}{8\pi \tau_r} \rho(\nu) f_e(\nu)
$$

$$
r_{ab}(\nu) = \phi_{\nu} \frac{\lambda^2}{8\pi \tau_r} \rho(\nu) f_a(\nu)
$$

### 3.热平衡时的自发辐射光谱密度

$$
f_e(\nu) = f(E_2)[1 - f(E_1)] \approx \exp\left(-\frac{h\nu}{k_B T}\right)
$$

$$
r_{sp}(\nu) \approx D_0 (h\nu - E_g)^{1/2} \exp\left(-\frac{h\nu - E_g}{k_B T}\right), h\nu \ge E_g
$$

其中：

$$
D_0 = \frac{(2m_r)^{3/2}}{\pi \hbar^2 \tau_r} \exp\left(-\frac{E_g}{k_B T}\right)
$$

### 4.准平衡时的增益系数——通过受激辐射和吸收速率相等可以推导

净增益系数为：
$$
\gamma_0(\nu) = \frac{\lambda^2}{8\pi \tau_r} \rho(\nu) f_g(\nu)
$$
其中费米反转因子由下式给出：
$$
f_g(\nu) \equiv f_e(\nu) - f_a(\nu) = f_c(E_2) - f_v(E_1)
$$
增益系数可以表示为：
$$
\gamma_0(\nu) = D_1 (h\nu - E_g)^{1/2} f_g(\nu), \quad h\nu \ge E_g
$$
其中：

$$
D_1 = \frac{\sqrt{2} m_r^{3/2} \lambda^2}{h^2 \tau_r}
$$

### 5.热平衡时的吸收速率——热平衡时无论本征半导体还是掺杂半导体的作用都是使光减弱，增益变为衰减

处于热平衡状态的半导体只有一个费米函数，因此：
$$
f_e(\nu) = f(E_2)[1 - f(E_1)] \approx \exp\left(-\frac{h\nu}{k_B T}\right)
$$
然后：
$$
r_{sp}(\nu) \approx D_0 (h\nu - E_g)^{1/2} \exp\left(-\frac{h\nu - E_g}{k_B T}\right), \quad h\nu \ge E_g
$$
其中：
$$
D_0 = \frac{(2m_r)^{3/2}}{\pi \hbar^2 \tau_r} \exp\left(-\frac{E_g}{k_B T}\right)
$$





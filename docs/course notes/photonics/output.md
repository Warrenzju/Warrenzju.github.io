# 激光振荡理论及其输出特性

## 一、激光振荡理论

- 放大器的小信号增益必须大于整个反馈系统的损耗，即在整个反馈回路中，存在净增益；
- 光在振荡器的整个回路中往返一周的总相位偏移量必须是2π的整数倍，这样经反馈输出信号的相位与原始输入信号的相位刚好相匹配

### 1.损耗

$$
\alpha_r = \alpha_s + \alpha_{m1} + \alpha_{m2}
$$

$$
\alpha_{m1} = \frac{1}{2d} \ln \frac{1}{R_1}
$$

$$
\alpha_{m2} = \frac{1}{2d} \ln \frac{1}{R_2}
$$

$$
\alpha_m = \alpha_{m1} + \alpha_{m2} = \frac{1}{2d} \ln \frac{1}{R_1 R_2}
$$

### 2.光子寿命

$$
\tau_p=\frac{1}{\alpha_rc}
$$

### 3. 光学谐振腔

- 谐振频率
	$$
	\nu_q=q\nu_F
	$$

- 谐振峰带宽
	$$
	\delta\nu\approx\frac{\nu_F}{F}=\frac{1}{2\pi\tau_p},\nu_F=c/2d
	$$

- 

- 细度
	$$
	F\approx\frac{\pi}{\alpha_rd}=2\pi\tau_p\nu_F
	$$

## 二、激光振荡条件

- 增益条件：决定了所需的最少的反转粒子数，并因此决定了激光振荡需要的泵浦阈值
- 相位条件：决定了激光振荡时的频率

#### 1.增益条件

激光振荡的启动必须满足小信号增益系数大于损耗系数
$$
\gamma_0(\nu) > \alpha_r
$$

$$
N_0 = \gamma_0(\nu)/\sigma(\nu) > \alpha_r/\sigma(\nu)
$$

$$
N_0 > N_t
$$

其中 $N_t$: 阈值反转粒子数差，决定了激光振荡的最小泵浦速率

where:
$$
N_t = \frac{\alpha_r}{\sigma(\nu)}
$$
or
$$
N_t = \frac{1}{c\tau_p \sigma(\nu)}
$$
代入
$$
\sigma(\nu)=\frac{\lambda^2}{8\pi t_{sp}}\text{g}(\nu)
$$
得到
$$
N_t = \frac{8\pi t_{sp}}{\lambda^2 c \tau_p \text{g}(\nu)}
$$
对于中心频率处$\text{g}(\nu_0)=2/\pi\Delta \nu$
$$
N_t = \frac{2\pi}{ \lambda^2 c } \frac{2\pi\Delta\nu t_{sp}}{\tau_p} 
$$
进一步地，如果跃迁只由自发辐射寿命为tsp的寿命增宽所限制，$\Delta\nu=1/2\pi t_{sp}$
$$
N_t = \frac{2\pi}{ \lambda^2 c } \frac{2\pi\Delta\nu t_{sp}}{\tau_p} \quad \longrightarrow \quad N_t = \frac{2\pi}{\lambda^2 c \tau_p} = \frac{2\pi\alpha_r}{\lambda^2}
$$

#### 2. 相位条件

$$
2kd + 2\varphi(\nu)d = 2\pi q, \quad q=1, 2, \dots
$$

当介质产生的额外相位不可忽略时，代入洛伦兹线形的相位变化
$$
\phi(\nu)=\frac{\nu-\nu_0}{\Delta \nu}\gamma(\nu)
$$
得
$$
\nu + \frac{c}{2\pi \Delta\nu} (\nu - \nu_0) \gamma(\nu) = \nu_q \quad
$$
or
$$
\nu = \nu_q - \frac{c}{2\pi \Delta\nu} (\nu - \nu_0) \gamma(\nu) \quad
$$
令$\nu=\nu_q'\approx \nu_q$
$$
\nu'_q = \nu_q - \frac{c}{2\pi} \frac{\nu_q - \nu_0}{\Delta\nu} \gamma(\nu_q) \quad 
$$
即实际振荡频率$\nu_q'$比冷腔频率$\nu_q$更靠近介质的中心频率$\nu_0$

在稳态条件下，增益等于损耗可得
$$
\gamma(\nu_q) = \alpha_r \approx \pi/Fd = (2\pi/c)\delta\nu
$$
代入
$$
\nu'_q = \nu_q - \frac{c}{2\pi} \frac{\nu_q - \nu_0}{\Delta\nu} \gamma(\nu_q)
$$
由此可见：

- 腔膜越陡（δv 越小），牵引效应越不明显
- 原子的振荡线宽越小（Δv越小），牵引效应就越明显

#### 3. 输出光子流密度

考虑稳态的时候增益等于损耗
$$
\frac{\gamma_0(\nu)}{[1 + \phi / \phi_s(\nu)]} = \alpha_r
$$
得到稳态时的光子流密度
$$
\phi =
\begin{cases}
\phi_s(\nu) \left[ \frac{\gamma_0(\nu)}{\alpha_r} - 1 \right], & \gamma_0(\nu) > \alpha_r \\
0, & \gamma_0(\nu) \le \alpha_r
\end{cases}
$$
可以将其换为用反转粒子数差表示的形式
$$
\phi =
\begin{cases}
\phi_s(\nu) \left( \frac{N_0}{N_t} - 1 \right), & N_0 > N_t \\
0, & N_0 \le N_t
\end{cases}
$$
假设反射镜的透射率为T，可以得到输出光子流密度（因为谐振腔里光有两个传播方向所以要除2）
$$
\phi_0 = \frac{T\phi}{2}
$$
对于的激光输出强度为
$$
I_0 = \frac{h\nu T\phi}{2}
$$
对应的激光输出功率为
$$
P_0 = I_0 A
$$
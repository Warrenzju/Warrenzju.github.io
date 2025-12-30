# 声光调制

## 1. 声波是如何改变折射率的

声波在空气中传播的时候，会导致空气中某个瞬间的某个位置的空气密度变大，某些位置的空气密度变小
$$
n=\sqrt{\epsilon_r}=\sqrt{1+\chi}
$$

$$
\chi=\frac{\vec p}{\epsilon_0 \vec E}
$$

$$
\vec p=Nq\vec l
$$

所以声波通过改变N来改变折射率

## 2. Bragg Diffraction—厚度相对于光栅的周期较大

声波振动方程

$$
s(x, t) = S_0 \cos(\Omega t - qx)
$$

**S₀**: the amplitude  
**Ω**: $\Omega = 2\pi f$  
**q**: $q = \frac{2\pi}{\Lambda}$ (wavenumber)

---

**The acoustic intensity (W/m²):**

$$
I_s = \frac{1}{2} \rho v_s^3 S_0^2
$$

**p**: photoelastic constant (光弹系数)  
**ρ**: the mass density  
**vₛ**: acoustic plane wave velocity

---

**折射率的变化量:**
$$
\Delta n(x, t) = -\frac{1}{2} p n^3 s(x, t)
$$
n为无声波时的材料的折射率，p为光弹常数，负号表示声波振动的正方向为折射率减小的方向

**折射率分布：**

$$
n(x,t) = n - \Delta n_0 \cos(\Omega t - qx)
$$

其中，
$$
\Delta n_0 = \frac{1}{2} p n^3 S_0
$$

---

**写成与声波强度的关系：**

$$
\Delta n_0 = \left( \frac{1}{2} M I_s \right)^{1/2}
$$

**声光品质因子** (merit for the strength of the acousto-optic effect)：
$$
M = \frac{p^2 n^6}{\rho v_s^3}
$$

---

对入射光场可以看做 **“静光栅”:**

$$
n(x,t) = n - \Delta n_0 \cos(qx - \varphi)
$$
其中$\varphi$是一个固定的相位，因为声波的频率远小于光波的频率，所以声波可以看作不变的

---

**总的反射系数：**
$$
r = \int_{-L/2}^{L/2} e^{j2kx\sin\theta} \frac{dr}{dx} dx
$$

其中，

**$e^{j2kx\sin\theta}$:**表示光波相对于x=0位置产生的相位差

$\Delta r=\frac{dr}{dx} \Delta x$:表示每一个微小薄层的反射振幅
$$
\frac{dr}{dx} = \frac{dr}{dn} \frac{dn}{dx} = \frac{dr}{dn} q \Delta n_0 \sin(qx - \varphi)
$$

---

**根据菲涅耳方程（Fresnel equations）：**

对于TE模式：
$$
\Delta r = \frac{-1}{2n \sin^2 \theta} \Delta n
$$

对于TM模式：
$$
\Delta r = \frac{- \cos 2\theta}{2n \sin^2 \theta} \Delta n
$$

在大多数声光器件中，$\theta$ 很小，因此 $\cos 2\theta \approx 1$。

---

**总的反射系数：**

$$
r = \int_{-L/2}^{L/2} e^{j2kx\sin\theta} \frac{dr}{dx} dx
$$

**反射系数微分的推导：**

$$
\frac{dr}{dx} = \frac{dr}{dn} \frac{dn}{dx} = \frac{dr}{dn} q \Delta n_0 \sin(qx - \varphi)
$$

**利用菲涅耳方程（TE模式，小角度近似）：**

$$
\Delta r = \frac{-1}{2n \sin^2 \theta} \Delta n
$$

代入得：

$$
\frac{dr}{dx} = \frac{-1}{2n \sin^2 \theta} \left[ q \Delta n_0 \sin(qx - \varphi) \right] = r' \sin(qx - \varphi)
$$

其中：

$$
r' = \frac{-q}{2n \sin^2 \theta} \Delta n_0
$$

**反射系数积分表达式：**

将 $\sin(qx - \varphi) $用欧拉公式展开：

$$
r = \frac{1}{2} jr' e^{j\varphi} \int_{-L/2}^{L/2} e^{j(2k\sin\theta - q)x} dx - \frac{1}{2} jr' e^{-j\varphi} \int_{-L/2}^{L/2} e^{j(2k\sin\theta + q)x} dx
$$

**布拉格条件与频移：**

- 当$ 2k \sin \theta = q $时，第一项取最大值（上频移，upshifted）
- 当 $2k \sin \theta = -q$ 时，第二项取最大值（下频移，downshifted）

对应的角度：

$$
\theta = \pm \sin^{-1} \left( \frac{q}{2k} \right)
$$

**上频移的反射振幅：**

假设满足布拉格条件 $2k \sin \theta = q$，并考虑相位项，反射系数可写为：

$$
r = \frac{1}{2} jr' L \operatorname{sinc} \left[ (q - 2k \sin \theta) \frac{L}{2\pi} \right] e^{j\varphi}
$$

其中 $\operatorname{sinc}(x) = \frac{\sin(\pi x)}{\pi x}$。

$$
q=\frac{2\pi}{\Lambda}
$$
所以可以推出关系如下，并把该角称为布拉格衍射角
$$
sin\theta_B=\frac{\lambda}{2\Lambda}
$$
也可以将上式改写为：
$$
r = \frac{1}{2} jr' L \operatorname{sinc} \left[ (sin\theta_B - \sin \theta) \frac{2L}{\lambda} \right] e^{j\varphi}
$$
当
$$
sin\theta_B - \sin \theta= \frac{\lambda}{2L}
$$
时，r取得最小值为0，且因为$L>>\lambda$，所以稍微偏离布拉格衍射角，反射率就会变得很小

---

**反射率：**
$$
R = |r|^2 = \frac{|r'|^2 L^2}{4}
$$

**将 $r'$ 代入：**

$$
R = \frac{\pi^2}{\lambda_0^2} \left( \frac{L}{\sin \theta} \right)^2 \Delta n_0^2
$$

**代入 $\Delta n_0^2 = \frac{1}{2} M I_s$：**

$$
R = \frac{\pi^2}{2\lambda_0^2} \left( \frac{L}{\sin \theta} \right)^2 M I_s
$$

**另一种常见形式（将 $\sin \theta$ 用布拉格角关系代入）：**

$$
R = 2\pi^2 n^2 \frac{L^2 \Delta^2}{\lambda_0^4} M I_s
$$

**重要结论：**

- $R$ 与声波强度 $I_s$ 成正比，但是当声波强度大到一定值后上述关系不满足，满足如下关系

$$
R = \sin^2 \left( \sqrt{R} \right)
$$

---

频率漂移和矢量合成：

光束看成能量为$\hbar\omega$，动量为$\hbar k$的光子流
声波看成能量为$\hbar\Omega$，动量为$\hbar q$的声子流
利用动量守恒：
$$
\hbar k\pm\hbar q=\hbar k_r
$$
利用能量守恒：
$$
\hbar\omega\pm\hbar\Omega=\hbar\omega_r
$$

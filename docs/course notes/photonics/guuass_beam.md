# 高斯光束
## 一、基本描述公式

$$
W(z)=W_0\sqrt{1+(\frac{z}{z_0})^2}
$$

$$
R(z)=z[1+(\frac{z_0}z)^2]
$$

$$
\zeta (z)=tan^{-1}\frac{z}{z_0}
$$

$$
W_0=\sqrt\frac{\lambda z_0}{\pi}
$$

$$
q=z+iz_0
$$


## 二、光强
光强可以表示为下式：

$$
I(\rho,z) = I_0 \left[ \frac{W_0}{W(z)} \right]^2 \exp\left[ -\frac{2\rho^2}{W^2(z)} \right]
$$

功率，与位置z无关：

$$
P=\frac12I_0\pi W_0^2
$$

用功率表示光强：

$$
I(\rho,z) = \frac{2P}{\pi W^2(z)} \exp\left[-\frac{2\rho^2}{W^2(z)}\right]
$$

发散角：

$$
\theta_0=\frac{W_0}{z_0}=\frac{\lambda_0}{\pi W_0}
$$

焦深（束面积为束腰的两倍）：

$$
2z_0=\frac{2\pi W_0^2}{\lambda}
$$

##  三、位相

高斯光束的位相：

$$
\varphi(\rho,z) = kz - \zeta(z) + \frac{k\rho^{2}}{2R(z)}
$$

- $kz$为平面波的位相
- $\zeta(z)$从$z=-\infty$到$z=+\infty$产生$\pi$的相移
- 第三项为波前项，在$z>>z_0$时近似于球面波
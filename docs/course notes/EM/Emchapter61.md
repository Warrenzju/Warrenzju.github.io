# Chapter 6

## 一、真空中静磁学的基本公理

$$
\nabla \cdot \boldsymbol{B}=0 \tag{6-1}
$$

$$
\nabla \times \boldsymbol{B}=\mu_0 \boldsymbol{J} \tag{6-2}
$$

分别运用散度定理和斯托克斯定理可得积分形式：
$$
\oint_S \boldsymbol{B} \cdot d\boldsymbol{s} = 0
$$
$$
\oint_C \boldsymbol{B} \cdot d\boldsymbol{l} = \mu I
$$

---

## 二、矢量磁位

由(6-1)及一个矢量的旋度的散度为0，定义矢量磁位\(\boldsymbol{A}\)：
$$
\boldsymbol{B} = \nabla \times \boldsymbol{A}
$$
代入(6-2)并令
$$
\nabla \cdot \boldsymbol{A} = 0
$$
可得
$$
\nabla^2 \boldsymbol{A} = -\mu \boldsymbol{J} \tag{6-3}
$$
(6-3)等价于：
$$
\nabla^2 A_x = -\mu J_x
$$

$$
\nabla^2 A_y = -\mu J_y
$$

$$
\nabla^2 A_z = -\mu J_z
$$

在真空中有一个特解：
$$
\boldsymbol{A} = \frac{\mu_0}{4\pi} \int_{V'} \frac{\boldsymbol{J}}{\boldsymbol{R}} \, dv' \ \ \ (\text{Wb/m}) \tag{6-4}
$$

总结：可以从\(\boldsymbol{J} \to \boldsymbol{A} \to \boldsymbol{B}\)

磁通量计算方法：
$$
\Phi = \int_S \boldsymbol{B} \cdot d\boldsymbol{s} = \int_S \left( \nabla \times \boldsymbol{A} \right) \cdot d\boldsymbol{s} = \oint_{C} \boldsymbol{A} \cdot d\boldsymbol{l}
$$

---

## 三、毕奥-萨伐定律及应用

对一根截面面积为\(S\)的细导线：
$$
\boldsymbol{J} \, dv' = \boldsymbol{J} \, S \, dl' = I \, d\boldsymbol{l}'
$$
将其代入(6-4)得：
$$
d\boldsymbol{B} = \frac{\mu_0 I}{4\pi} \left( \frac{d\boldsymbol{l}' \times \boldsymbol{R}}{R^3} \right)
$$

---

## 四、磁偶极子

$$
\boldsymbol{A} = \boldsymbol{a}_\phi \frac{\mu_0 (I \pi b^2)}{4\pi R^2} \sin \theta = \frac{\mu_0 \boldsymbol{m} \times \boldsymbol{a_R}}{4\pi R^2} \ \ \ (\text{Wb/m}) \tag{6-5}
$$

其中：
$$
\boldsymbol{m} = \boldsymbol{a_z} I S = \boldsymbol{a_z} m \ \ \ (\text{A/m}^2)
$$
被定义为一个矢量，大小为回路中电流和回路面积的乘积，方向是当右手的四指指向电流方向时，大拇指的方向。

$$
\boldsymbol{B} = \frac{\mu \boldsymbol{m}}{4\pi R^3} \left( \boldsymbol{a_R} 2 \cos \theta + \boldsymbol{a_\theta} \sin \theta \right)
$$

---

## 五、磁化强度和等效电流密度

定义磁化矢量\(\boldsymbol{M}\)：

$$
\boldsymbol{M} = \lim_{\Delta v \to 0} \frac{\sum_{k=1}^{n \Delta v} \boldsymbol{m}_k}{\Delta v}
$$

根据式(6-5)可得：

$$
\boldsymbol{A} = \frac{\mu_0}{4\pi} \int_{V'} \frac{\nabla' \times \boldsymbol{M}}{R} \, dv' + \frac{\mu_0}{4\pi} \int_{S'} \frac{\boldsymbol{M} \times \boldsymbol{a_n'}}{R} \, ds'
$$

与(6-4)比较，可将磁化矢量强度效应等效为一个体电流密度：

$$
\boldsymbol{J}_m = \nabla \times \boldsymbol{M}
$$

和一个面电流密度：
$$
\boldsymbol{J}_{ms} = \boldsymbol{M} \times \boldsymbol{a_n}
$$

---

## 六、磁场强度和相对磁导率

在磁性材料中：
$$
\nabla \times \left( \frac{\boldsymbol{B}}{\mu_0} - \boldsymbol{M} \right) = \boldsymbol{J}
$$
定义电场强度\(\boldsymbol{H}\)，使得：
$$
\boldsymbol{H} = \frac{\boldsymbol{B}}{\mu_0} - \boldsymbol{M}
$$
得到：
$$
\nabla \times \boldsymbol{H} = \boldsymbol{J} \tag{6-6}
$$
对其两边取标量面积分，得到相应的积分形式：
$$
\oint_c \boldsymbol{H} \cdot d\boldsymbol{l} = I
$$

---

## 七、静磁场的边界条件

由其散度为0可得，在分界面处的法向分量连续：
$$
B_{1n} = B_{2n}
$$

$$
\mu_1 H_{1n} = \mu_2 H_{2n}
$$

由(6-6)得其切向分量不连续：
$$
\boldsymbol{a}_{n2} \times \left( \boldsymbol{H}_1 - \boldsymbol{H}_2 \right) = \boldsymbol{J}_s
$$
\(\boldsymbol{a}_{n2}\)是分界面从媒质2向外的单位法线。

---

## 八、磁能

$$
W_m = \int_{V'} w_m \, dv'
$$

$$
w_m = \frac{1}{2} \boldsymbol{H} \cdot \boldsymbol{B} \ \ \ (\text{J/m}^3)
$$

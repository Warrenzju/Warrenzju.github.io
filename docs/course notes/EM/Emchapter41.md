
### 1. 泊松方程和拉普拉斯方程

泊松方程：
$$
\nabla^2 V = -\frac{\rho}{\epsilon}
$$
拉普拉斯方程：
$$
\nabla^2 V = 0
$$

$\nabla^2 V$表示梯度的散度：

- 直角坐标系：

  $$
  \nabla^2 V = \nabla \cdot \nabla V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2}
  $$

- 圆柱坐标：

  $$
  \nabla^2 V = \frac{1}{r} \frac{\partial }{\partial r} \left( r \frac{\partial V}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 V}{\partial \phi^2} + \frac{\partial^2 V}{\partial z^2}
  $$

- 球坐标：

  $$
  \nabla^2 V = \frac{1}{R^2} \frac{\partial }{\partial R} \left( R^2 \frac{\partial V}{\partial R} \right) + \frac{1}{R^2 \sin \theta} \frac{\partial }{\partial \theta} \left( \sin \theta \frac{\partial V}{\partial \theta} \right) + \frac{1}{R^2 \sin^2 \theta} \frac{\partial^2 V}{\partial \phi^2}
  $$

---

### 2. 电流密度和欧姆定律

由于电流是电荷的时间变化率，可得：
$$
\Delta I = N q \mathbf{u} \cdot \Delta \mathbf{s}
$$
定义**体电流密度 $\mathbf{J}$**：
$$
\mathbf{J} = N q \mathbf{u} = \rho \mathbf{u} \;\; (A/m^2) \tag{5-1}
$$
其中 $\rho$ 表示单位体积内的自由电荷密度

$$
I = \int_s \mathbf{J} \cdot d\mathbf{s}
$$

在传导电流中，可能有不止一种电荷载体，它们以不同速度漂移，可将（5-1）推广：
$$
\mathbf{J} = \sum_{i}^{} N_i q_i \mathbf{u}_i
$$
对金属导体而言，电荷载体的平均漂移速度可表示为：
$$
\mathbf{u} = \mu_e \mathbf{E} \;\; (m/s)
$$
其中 $\mu_e$ 是电子迁移率

代入式（5-1）可得
$$
\mathbf{J} = - \rho_e \mu_e \mathbf{E}
$$
定义电导率 $\sigma = - \rho_e \mu_e$，半导体中 $\sigma = - \rho_e \mu_e + \rho_h \mu_h$，得
$$
\mathbf{J} = \sigma \mathbf{E}
$$
称其为欧姆定律的点函数形式（使用时注意其电场强度为总的电场强度）

由
$$
J = \frac{I}{S} = \sigma E = \sigma \frac{V}{l}
$$
可得
$$
V = \left( \frac{l}{\sigma S} \right) I = R I
$$
所以
$$
R = \frac{l}{\sigma S}
$$

---

### 3. 电动势和基尔霍夫电压定律

**电动势**：
$$
V = \int_{1}^{2} \mathbf{E} \cdot d\mathbf{l}
$$
该式指电源外部电极 1（正极）指到电极 2（负极）

**基尔霍夫电压定律**：
$$
\sum_{j}^{} V_j = \sum_{k}^{} R_k I_k
$$

---

### 4. 连续性方程和基尔霍夫电流定律

由电流的定义：
$$
I = \oint_{S}^{} \mathbf{J} \cdot d\mathbf{s} = - \frac{dQ}{dt} = - \frac{d}{dt} \int_V \rho \, dv
$$
再由散度定理将面积分转换为体积分：

$$
\int_V \nabla \cdot \mathbf{J} \, dv = - \int_V \frac{\partial \rho }{\partial t} \, dv
$$

得到**连续性方程**：
$$
\nabla \cdot \mathbf{J} = - \frac{\partial \rho}{\partial t} \;\; (A/m^2)
$$
对于稳恒电流，电荷密度不随时间变化：
$$
\nabla \cdot \mathbf{J} = 0 \tag{5-2}
$$
式（5-2）是一个点函数关系，该式意味着 $\rho = 0$ 的所有点无流量源也满足这个关系式，这表明稳恒电流的场线或者流线自行闭合，可导出
$$
\oint_S \mathbf{J} \cdot d\mathbf{s} = 0
$$
可写为
$$
\sum_{j} I_j = 0
$$
该式即为**基尔霍夫电流定律**的表达式

---

### 5. 功耗和焦耳定律

易得
$$
dP = \mathbf{E} \cdot \mathbf{J} \, dv
$$
点函数 $\mathbf{E} \cdot \mathbf{J}$ 是稳恒电流条件下的功率密度，易得**焦耳定律**
$$
P = \int_V \mathbf{E} \cdot \mathbf{J} \, dv
$$
在恒定截面的导体中 $dv = ds \, dl$
$$
P = \int_L E \, dl \int_S J \, ds = V I
$$

---

### 6. 电流密度的边界条件

无散矢量场的法向分量在分界面是连续的：
$$
\nabla \cdot \mathbf{J} = 0
$$
$$
J_{1n} = J_{2n}
$$

无旋矢量场的切向分量在分界面是连续的：
$$
\nabla \times \left( \frac{\mathbf{J}}{\sigma} \right) = 0
$$

$$
\frac{\mathbf{J}_{1t}}{\sigma_1} = \frac{\mathbf{J}_{2t}}{\sigma_2}
$$

电场的方向分量必须同时满足下面两式：

$$
J_{1n} = J_{2n} \to \sigma_1 E_{1n} = \sigma_2 E_{2n}
$$

$$
D_{1n} - D_{2n} = \rho_s \to \epsilon_1 E_{1n} - \epsilon_2 E_{2n} = \rho_s
$$

其中参考单位法线由介质 2 向外，因此除非 $\sigma_2 / \sigma_1 = \epsilon_2 / \epsilon_1$，否则面电荷一定存在于分界面上

$$
\rho_s = \left( \epsilon_1 \frac{\sigma_2}{\sigma_1} - \epsilon_2 \right) E_{2n} = \left( \epsilon_1 - \epsilon_2 \frac{\sigma_1}{\sigma_2} \right) E_{2n}
$$

当介质 2 的导电性远好于介质 1 得
$$
\rho_s = \epsilon_1 E_{1n} = D_{1n}
$$

---

### 7. 电阻的计算

$$
RC = \frac{\epsilon}{\sigma}
$$
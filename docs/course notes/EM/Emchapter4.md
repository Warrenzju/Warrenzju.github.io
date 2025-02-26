# Chapter4、5

## 一、泊松方程和拉普拉斯方程

泊松方程：
$$
\nabla^2V=-\frac\rho\epsilon
$$
拉普拉斯方程：
$$
\nabla^2V=0
$$
$\nabla^2V$表示梯度的散度：

- 直角坐标系：

	$$
	\nabla^2V=\nabla\cdot\nabla V=\frac{\partial^2 V}{\partial x^2}+\frac{\partial^2 V}{\partial y^2}+\frac{\partial^2 V}{\partial z^2}
	$$

- 圆柱坐标：

	$$
	\nabla^2V=\frac1r\frac{\partial }{\partial r}(r\frac{\partial V}{\partial r})+\frac1{r^2}\frac{\partial^2 V}{\partial \phi^2}+\frac{\partial^2 V}{\partial z^2}
	$$

- 球坐标：

	$$
	\nabla^2V=\frac{1}{R^2}\frac{\partial }{\partial R}\left ( R^2\frac{\partial V}{\partial R}  \right ) +\frac{1}{R^2sin\theta}\frac{\partial }{\partial \theta }(sin\theta \frac{\partial V}{\partial \theta })+\frac{1}{R^2sin^2\theta }\frac{\partial^2V}{\partial \phi ^2}
	$$


## 二、电流密度和欧姆定律

由于电流是电荷的时间变化率，可得：
$$
\bigtriangleup I=Nq\vec{u}\cdot \bigtriangleup \vec{s}
$$
定义**体电流密度$J$**:
$$
\vec J=Nq\vec u=\rho\vec u\;\;(A/m^2)\tag{5-1}
$$
其中$\rho$表示单位体积内的自由电荷密度

$$
I=\int _s\vec{J}\cdot d\vec{s}
$$

在传导电流中，可能有不止一种电荷载体，它们以不同速度漂移，可将（5-1）推广：
$$
\vec J=\sum_{i}^{} N_iq_i\vec u_i
$$
对金属导体而言，电荷载体的平均漂移速度可表示为：
$$
\vec u=\mu_e\vec E\;\;(m/s)
$$
其中$\mu_e$是电子迁移率

代入式（5-1）可得
$$
\vec J=-\rho_e\mu_e\vec E
$$
定义电导率$\sigma=-\rho_e\mu_e$,半导体中$\sigma=-\rho_e\mu_e+\rho_h\mu_h$，得
$$
\vec J=\sigma\vec E
$$
称其为欧姆定律的点函数形式（使用时注意其电场强度为总的电场强度）

由
$$
J=\frac IS=\sigma E=\sigma \frac Vl
$$
可得
$$
V=(\frac{l}{\sigma S})I=RI
$$
所以
$$
R=\frac{l}{\sigma S}
$$

## 三、电动势和基尔霍夫电压定律

**电动势**：
$$
V =\int_{1}^{2} \vec{E} \cdot d\vec{l}
$$
该式指电源外部电极1（正级）指到电极2（负极）

**基尔霍夫电压定律**：

$$
\sum_{j}^{}V_j=\sum_{k}^{}R_kI_k
$$

## 四、连续性方程和基尔霍夫电流定律

由电流的定义：
$$
I=\oint_{S}^{}\vec{J}\cdot d\vec{s}=-\frac{dQ}{dt}=-\frac{d}{dt}\int_V\rho dv
$$
再由散度定理将面积分转换为体积分

$$
\int_V\nabla \cdot \vec{J}dv=-\int_V\frac{\partial \rho }{\partial t}dv  
$$

得到**连续性方程**：
$$
\nabla \cdot \vec{J}=-\frac{\partial \rho}{\partial t}  \;\;\;(A/m^2)
$$
对于稳恒电流，电荷密度不随时间变化：
$$
\nabla\cdot\vec J=0\tag{5-2}
$$
式（5-2）是一个点函数关系，该式意味着$\rho=0$的所有点无流量源也满足这个关系式，这表明稳恒电流的场线或者流线自行闭合，可导出
$$
\oint_S\vec J\cdot d\vec s=0
$$
可写为
$$
\sum_{j}I_j=0
$$
该式即为**基尔霍夫电流定律**的表达式

## 五、功耗和焦耳定律

易得
$$
dP=\vec E\cdot \vec Jdv
$$
点函数$\vec E\cdot\vec J$是稳恒电流条件下的功率密度，易得**焦耳定律**
$$
P=\int_V\vec E\cdot\vec Jdv
$$
再恒定截面的导体中$dv=dsdl$
$$
P=\int_L Edl\int_S Jds=VI
$$

## 六、电流密度的边界条件

无散矢量场的法向分量在分界面是连续的：
$$
\nabla\cdot \vec J=0
$$

$$
J_{1n}=J_{2n}
$$

无旋矢量场的切向分量在分界面是连续的：
$$
\nabla\times(\vec J/\sigma)=0
$$

$$
\frac{\vec J_{1t}}{\sigma_1}=\frac{\vec J_{2t}}{\sigma_2}
$$

电场的方向分量必须同时满足下面两式：  

$$
J_{1n}=J_{2n}\to \sigma _1E_{1n}=\sigma _2E_{2n}
$$

$$
D_{1n}-D_{2n}=\rho _s\to \epsilon _1E_{1n}-\epsilon _2E_{2n}=\rho _s
$$

其中参考单位法线由介质2向外，因此除非$\sigma_2/\sigma_1=\epsilon_2/\epsilon_1$，否则面电荷一定存在于分界面上

$$
\rho _s=\left ( \epsilon _1\frac{\sigma _2}{\sigma _1}-\epsilon _2  \right )E_{2n}= \left ( \epsilon _1-\epsilon _2\frac{\sigma _1}{\sigma _2}  \right )E_{2n} 
$$

当介质2 的导电性远好于介质1得

$$
\rho_S=\epsilon_1E_{1n}=D_{1n}
$$

## 七、电阻的计算

$$
RC=\frac\epsilon\sigma
$$




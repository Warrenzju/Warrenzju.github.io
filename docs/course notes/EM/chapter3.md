# chapter3

1. 静电学的两个基本定理
$$
\bigtriangledown\cdot E=\frac\rho \epsilon_0 \\
$$
$$
\bigtriangledown\times E=0
$$
1. 库伦定律：
$$
  E_P=\boldsymbol a_{qP}\frac{q}{4\pi\epsilon_0{\left|\boldsymbol R-\boldsymbol R'\right|}^2}
$$
  其中$a_{qP}$是从q到P所画的单位矢量

1. 相距$d$的电偶极子产生的电位
	$$
	\boldsymbol p=q\boldsymbol d\\
	$$
	$$
	V=\frac{qdcos\theta}{4\pi\epsilon_0R^2}=\frac{\boldsymbol p\cdot \boldsymbol a_R}{4\pi\epsilon_0R^2}
	$$
	电偶极子在球坐标下的电场强度
$$
E=-\nabla =\frac{p}{4\pi\epsilon_0R^3}(\boldsymbol a_R2cos\theta+\boldsymbol a_\theta sin\theta)
$$

1. 连续分布电荷的电场

  - 体电荷
  	$$
  	E=\frac{1}{4\pi\epsilon_0}\int_{V'}\boldsymbol a_R\frac{\rho_v}  {R^2}dv'
  	$$
  	
  	
  - 面电荷
  	$$
  	E=\frac{1}{4\pi\epsilon_0}\int_{S'}\boldsymbol a_R\frac{\rho_s} {R^2}ds'
  	$$

  - 线电荷
  	$$
  	E=\frac{1}{4\pi\epsilon_0}\int_{L'}\boldsymbol a_R\frac{\rho_l} {R^2}dl'
  	$$

5. 一个无旋矢量总是可以表示位一个标量场的梯度，所以可以定义一个**标量电位V**
	$$
	E=-\nabla V
	$$

6. 导体或真空界面的边界条件
	$$
	E_t=0\\
	$$
	$$
	E_n=\frac{\rho_s}{\epsilon_0}
	$$
	导体内
	$$
	\rho=0\\
	$$
	$$
	E=0
	$$

7. 极化电介质计算场公式
	$$
	V=\frac{1}{4\pi\epsilon_0}\oint_{V'}\frac{\rho_{p}}  {R}dv'+\frac{1}{4\pi\epsilon_0}\oint_{S'}\ a_R\frac{\rho_{ps}} {R}ds'
	$$
	其中等效极化电荷面密度$\rho_{ps}=\boldsymbol P\cdot\boldsymbol a_n$，等效极化电荷体密度$\rho_p=-\nabla \cdot\boldsymbol P$

8. 对电介质中的散度定理进行修正
	$$
	\nabla\cdot\boldsymbol E=\frac1\epsilon_0(\rho+\rho_p)
	$$
	将$\rho_p$进行代换得
	$$
	\nabla\cdot(\epsilon_0\boldsymbol E+\boldsymbol P)=\rho
	$$
	定义电位移
	$$
	D=\epsilon_0\boldsymbol E+\boldsymbol P
	$$
	得到两个任何媒质中的基本约束方程
	$$
	\nabla\cdot\boldsymbol D=\rho\\
	$$
	$$
	\nabla\times\boldsymbol E=0
	$$

9. 静电场的边界条件
	$$
	\boldsymbol E_{1t}=\boldsymbol E_{2t}\\
	$$
	$$
	\boldsymbol a_{n2}\cdot(\boldsymbol D_1-\boldsymbol D_2)=\rho_s
	$$
	

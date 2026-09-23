# 相对平衡的线性化

> 来源：Bullo & Lewis, *Supplementary Material* (2005)，S3.1–S3.3。
> 论文原文：[papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](../../papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)

## 1. 背景：受迫仿射联络控制系统

受迫仿射联络控制系统 $\Sigma=(Q,\nabla,Y,\mathscr{Y},\mathbb{R}^m)$，运动方程
$$\nabla_{\gamma'(t)}\gamma'(t)=\bar Y_0(\gamma(t))+\bar Y_1(\gamma'(t))+\sum_{a=1}^m u^a(t)Y_a(\gamma(t)).$$

**假设 S3.6**：外力可分解 $Y(v_q)=\bar Y_0(q)+\bar Y_1(v_q)$，其中 $\bar Y_0$ 为基本向量力（势能梯度），$\bar Y_1$ 为 $(1,1)$-张量场（如 Rayleigh 耗散）。

## 2. 沿受控轨迹的线性化（控制仿射情形）

**命题 S3.4**（切提升与微分算子）：沿 $X$ 的积分曲线 $\gamma$，定义 Lie drag 微分算子
$$\mathcal{L}^{X,\gamma}=[X_t,\Xi](\gamma(t)),$$
坐标下 $\mathcal{L}^{X,\gamma}(\xi)^i(t)=\dot\xi^i(t)-\tfrac{\partial X^i}{\partial x^j}(\gamma(t))\xi^j(t)$。$\xi$ 是 $X^T$ 的积分曲线 $\iff\mathcal{L}^{X,\gamma}(\xi)=0$ $\iff\xi$ 是 $X$ 沿 $\gamma$ 的变分。

**定义 S3.5**（控制仿射系统的线性化）：$L\Sigma(\gamma_0,u_0)=\mathcal{L}^{f_{u_0},\gamma_0}$，$b_{\Sigma,a}=\mathrm{vlft}(f_a)$，方程
$$\mathcal{L}\Sigma(\gamma_0,u_0)(\xi)(t)=\sum_{a=1}^m u^a(t)b_{\Sigma,a}(\gamma_0,u_0).$$

## 3. 受迫仿射联络控制系统的线性化

**命题 S3.7**（状态线性化）：设 $t\mapsto U(t)\oplus W(t)\in T_{\gamma_0'(t)}Q\oplus T_{\gamma_0'(t)}Q$ 是 $S_{\gamma_0(t)}^T$ 的积分曲线，则
$$W(t)=\nabla_{\gamma_0'(t)}U(t)+\tfrac{1}{2}T(U(t),\gamma_0'(t)),$$
$$\nabla_{\gamma_0'(t)}^2U(t)+R(U(t),\gamma_0'(t))\gamma_0'(t)+\nabla_{\gamma_0'(t)}\big(T(U(t),\gamma_0'(t))\big)=\nabla_{U(t)}(Y_0+Y_{u_0})+(\nabla_{U(t)}\bar Y_1)(\gamma_0'(t))+\bar Y_1(\nabla_{\gamma_0'(t)}U(t)).$$

**定义 3.8**（线性化）：$\{A_\Sigma(\gamma_0,u_0),b_{\Sigma,1},\dots,b_{\Sigma,m}\}$，其中
$$A_\Sigma(\gamma_0,u_0)(t)\cdot\xi(t)=R(\xi,\dot\gamma_0)\dot\gamma_0+\nabla_{\dot\gamma_0}(T(\xi,\dot\gamma_0))-\nabla_\xi Y_0-\nabla_\xi Y_{u_0}+(\nabla_\xi\bar Y_1)(\dot\gamma_0)+\bar Y_1(\nabla_{\dot\gamma_0}\xi),$$
$$b_{\Sigma,a}(\gamma_0,u_0)=Y_a(\gamma_0(t)),$$
线性化方程（式 S3.4）：
$$\nabla_{\gamma_0'(t)}^2\xi(t)+A_\Sigma(\gamma_0,u_0)(t)\cdot\xi(t)=\sum_{a=1}^m u^a(t)Y_a(\gamma_0(t)).$$

## 4. 相对平衡：约化与两种线性化

$\Sigma=(Q,\mathbb{G},V,F,\mathscr{F},U)$ 有完备无穷小对称 $X$，$\chi$ 为**正则相对平衡**（$X$ 的积分曲线，也是无控轨迹）。轨道空间 $B=Q/X$，约化系统状态空间 $TB\times\mathbb{R}$（式 S3.2）。

两种线性化视角：
1. **未约化**：沿 $\chi(t)$ 直接做轨迹线性化（含曲率、挠率、外力项）；
2. **约化**：相对平衡对应约化系统的平衡点 $(T\pi_B(\chi'(0)),1)$，得有限维 LTI 系统。

**定理 S3.14**（等价性）：$t\mapsto(x(t)\oplus\dot x(t)\oplus\nu(t),u(t))$ 是约化线性系统的解 $\iff(\xi,u)$（$\xi=T\pi_B$ 的纤维变分）是未约化线性化的解。

## 5. 线性化有效能量

未约化线性化有效能量（候选 Lyapunov 函数）：
$$E_\chi(u_{v_q}\oplus w_{v_q})=\tfrac12\|w_{v_q}-\nabla_{u_{v_q}}X\|_{\mathbb{G}}^2+\tfrac12\,\mathrm{Hess}\,V_X(u_{v_q},u_{v_q}),$$
约化版本 $E_\chi^{\mathrm{red}}$ 在 $TB\oplus\mathbb{R}$ 上，且 $\iota_{B,X}^*E_\chi^{\mathrm{red}}=E_\chi$（命题 S3.20）。

## 6. 线性稳定性（S3.3）

区分**基底（base）**方向（商流形 $B$）与**纤维（fiber）**方向（对称群轨道）：变分场分解 $\xi(t)=\mathrm{hor}(\xi(t))\oplus\zeta(t)X(\chi(t))$。

**定理 S3.25**（Lyapunov 充分条件，带 Rayleigh 耗散 $F(v_q)=-R_{\mathrm{diss}}^\flat(v_q-X(q))$）：
1. 若 $\mathrm{Hess}(V_X)_B(b_0)$ 正定 $\Rightarrow$ 线性基底+纤维稳定；
2. 若 $\mathrm{Hess}(V_X)_B(b_0)$ 正定且 $R_{\mathrm{diss}}$ 正定 $\Rightarrow$ 渐近基底+纤维稳定。

> 注：陀螺项的存在使仅靠势能 Hessian 难以获得渐近稳定，需反馈控制。

## 相关阅读
- [可控性](./controllability.md)
- [相对平衡的镇定](./stabilization-relative-equilibria.md)
- [Jacobi 方程与伴随 Jacobi 方程](../differential-geometry/jacobi-equations.md)

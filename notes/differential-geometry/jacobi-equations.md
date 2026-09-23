# Jacobi 方程与伴随 Jacobi 方程

> 来源：Bullo & Lewis, *Supplementary Material* (2005)，S1.3.10。
> 论文原文：[papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](../../papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)

## 1. 测地喷雾切提升的表示

**命题 S1.32**（测地喷雾切提升的表示）：对 $u_{v_q}\oplus w_{v_q}\in T_{v_q}TQ\cong T_qQ\oplus T_qQ$，
$$S^T(u_{v_q}\oplus w_{v_q})=v_q\oplus 0\oplus w_{v_q}\oplus\big(-\Omega_{HTQ}\big(\mathrm{hlft}_{v_q}(u_{v_q}),\mathrm{hlft}_{v_q}(v_q)\big)\big).$$

**引理 S1.33**：沿满足 $\nabla_{\dot\gamma}\dot\gamma=Y(t,\gamma)$ 的曲线 $\gamma$，向量场 $X=X_1\oplus X_2$ 的切向量场为
$$\dot\gamma'(t)\oplus Y(t,\gamma(t))\oplus\big(\nabla_{\dot\gamma}X_1+\tfrac{1}{2}T(X_1,\dot\gamma)\big)\oplus\big(\nabla_{\dot\gamma}X_2+\tfrac{1}{2}T(X_2,\dot\gamma)\big).$$

## 2. Jacobi 方程

**定理 S1.34**（切提升与 Jacobi 方程）：设 $\gamma$ 为仿射联络 $\nabla$ 的测地线，$t\mapsto U(t)\oplus W(t)$ 为 $S^T$ 的积分曲线，则
$$\nabla_{\gamma'(t)}^2U(t)+R(U(t),\gamma'(t))\gamma'(t)+\nabla_{\gamma'(t)}\big(T(U(t),\gamma'(t))\big)=0,$$
$$W(t)=\nabla_{\gamma'(t)}U(t)+\tfrac{1}{2}T(U(t),\gamma'(t)).$$

对无挠 Levi-Civita 联络（$T=0$），退化为经典 Jacobi 方程
$$\nabla_{\dot\gamma}^2U+R(U,\dot\gamma)\dot\gamma=0,$$
$U$ 即 Jacobi 场。

## 3. 伴随 Jacobi 方程

先定义对偶曲率与对偶挠率：
$$\langle R^*(\alpha_q,u_q)v_q;w_q\rangle=\langle\alpha_q;R(w_q,u_q)v_q\rangle,$$
$$\langle T^*(\alpha_q,u_q);w_q\rangle=\langle\alpha_q;T(w_q,u_q)\rangle.$$

沿测地线 $\gamma$ 的余向量场 $\alpha$ 满足**伴随 Jacobi 方程**：
$$\nabla_{\gamma'(t)}^2\alpha(t)+R^*(\alpha(t),\gamma'(t))\gamma'(t)-T^*\big(\nabla_{\gamma'(t)}\alpha(t),\gamma'(t)\big)=0.$$

**命题 S1.36**（测地喷雾余切提升的表示）：
$$S^{T^*}(\alpha_{v_q}\oplus\beta_{v_q})=v_q\oplus 0\oplus\big(\Omega_{HTQ}^\sharp(\mathrm{vlft}_{v_q}(\beta_{v_q}),\mathrm{hlft}_{v_q}(v_q))\big)\oplus(-\alpha_{v_q}).$$

**定理 S1.38**：$S^{T^*}$ 的积分曲线 $\Theta(t)\oplus\Lambda(t)$ 中 $\Lambda(t)$ 满足伴随 Jacobi 方程，且
$$\Theta(t)=-\nabla_{\gamma'(t)}\Lambda(t)+\tfrac{1}{2}T^*\big(\Lambda(t),\gamma'(t)\big).$$

**Levi-Civita 联络下的等价**：$\lambda(t)$ 是伴随 Jacobi 方程的解 $\iff\mathbb{G}^\sharp(\lambda(t))$ 是 Jacobi 场。

> 关键应用：伴随 Jacobi 方程正是仿射联络控制系统极大值原理中**协态方程**的核心（S4.4，定理 S4.26）。

## 相关阅读
- [Ehresmann 联络与 Sasaki 度量](./ehresmann-connections.md)
- [最优控制与极大值原理](../geometric-control/optimal-control.md)

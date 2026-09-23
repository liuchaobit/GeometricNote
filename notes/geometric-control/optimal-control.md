# 最优控制与极大值原理（Optimal Control & Maximum Principle）

> 来源：Bullo & Lewis, *Supplementary Material* (2005)，S4。
> 论文原文：[papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](../../papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)

## 1. 最优控制问题的几何表述（S4.1–S4.2）

控制系统 $\Sigma=(M,f,U)$ 带代价函数 $F:M\times\mathbb{R}^m\to\mathbb{R}$。目标泛函
$$A_{\Sigma,F}(\gamma,u)=\int_a^b F(\gamma(t),u(t))\,dt.$$

**哈密顿量**（$T^*M\times\mathbb{R}^m$ 上）：
$$H_{\Sigma,F}(\alpha_x,u)=\alpha_x\cdot f(x,u)-F(x,u),$$
**极大哈密顿量**：$H_{\Sigma,F}^{\max}(\alpha_x)=\sup\{H_{\Sigma,F}(\alpha_x,u)\mid u\in U\}$。

**定理 S4.11（极大值原理）**：$(\gamma,u)$ 是 $\mathscr{P}_{[a,b]}$ 的解，则存在 LAC 协向量场 $\chi$ 与常数 $\lambda_0\in\{0,1\}$：
1. 横截条件：$\chi(a)\in\mathrm{ann}(T_{\gamma(a)}S_0)$，$\chi(b)\in\mathrm{ann}(T_{\gamma(b)}S_1)$；
2. $t\mapsto\chi(t)$ 是 $X_{H_{\Sigma,F}^{\max}}$ 的积分曲线；
3. $\chi$ 沿 $u$ 对 $(\Sigma,\lambda_0 F)$ 极大化；
4. 要么 $\lambda_0=1$，要么 $\chi\neq0$；
5. 存在常数 $C$：$H_{\Sigma,F}(\chi(t),u(t))=C$（几乎处处）；自由区间问题另有 $H=0$。

局部坐标哈密顿方程（伴随方程）：
$$\dot x^i(t)=\tilde f^i(x(t),u(t)),\qquad \dot p_i(t)=-\frac{\partial\tilde f^j}{\partial x^i}p_j+\lambda_0\frac{\partial\tilde F}{\partial x^i}.$$

**极值分类**：
- 定义 S4.13–S4.14：受控极值、极值曲线、极值控制；伴随协向量场 $\chi$、常数 Lagrange 乘子 $\lambda_0$；
- 定义 S4.15：$\lambda_0=1$ 为**正常（normal）**，仅 $\lambda_0=0$ 满足为**异常（abnormal）**；
- 定义 S4.16：极大化条件对 $u$ 无信息时为**奇异（singular）**，否则**正则（regular）**。

## 2. 仿射联络控制系统的极大值原理（S4.4）

系统 $\nabla_{\gamma'(t)}\gamma'(t)=\sum_{a=1}^m u^a(t)Y_a(\gamma(t))$，状态在 $TQ$。利用 S1.3 的联络分裂写 $\Lambda_{v_q}=\alpha_{v_q}\oplus\beta_{v_q}\in T^*TQ$。

哈密顿量：
$$H_{\Sigma,F_{\mathscr{A}}}(\alpha_{v_q}\oplus\beta_{v_q},u)=\alpha_{v_q}\cdot v_q+u^a\big(\beta_{v_q}\cdot Y_a(q)\big)-F_{\mathscr{A}}(v_q,u).$$

**定理 S4.26**：存在 LAD 协向量场 $\lambda:I\to T^*Q$ 沿 $\gamma$ 与 $\lambda_0\in\{0,1\}$，使得协态满足**二阶伴随方程**（其左端正是**伴随 Jacobi 方程**）：
$$\nabla_{\gamma'(t)}^2\lambda(t)+R^*(\lambda(t),\gamma'(t))\gamma'(t)-T^*\big(\nabla_{\gamma'(t)}\lambda(t),\gamma'(t)\big)=\text{(外力/代价项)},$$
其中
$$\theta(t)=\tfrac12T^*\big(\lambda(t),\gamma'(t)\big)-\nabla_{\gamma'(t)}\lambda(t)+\lambda_0 f'\big(A(\gamma'(t),\dots)\big)\hat A(\gamma'(t),\dots).$$

> 关键结构（Remarks S4.27）：协态方程**内在解耦**为 $Q$ 上的二阶方程——这是仿射联络（众多 Ehresmann 联络）存在的红利；左端即伴随 Jacobi 方程，几何通过 $\nabla,R,T$ 进入最优控制。

## 3. 力极小控制（S4.5）

二次代价 $J=\tfrac12\int_0^T\|u\|^2\,dt$。按仿射联络类型讨论：一般仿射联络、完全驱动情形、Levi-Civita 联络；讨论奇异与异常极值。

## 4. 时间最优控制（S4.6）

$J=\int_0^T1\,dt$，控制幅值约束 $|u^a|\le U_{\max}$。同样导出伴随 Jacobi 方程，存在奇异时间最优极值。

## 5. 例：平面刚体（S4.7）

$SE(2)$ 上力最优/时间最优控制：非奇异受控极值（正则情形可显式求解）+ 奇异受控极值的刻画。

## 相关阅读
- [Jacobi 方程与伴随 Jacobi 方程](../differential-geometry/jacobi-equations.md)
- [相对平衡的线性化](./linearization-relative-equilibria.md)
- [可控性](./controllability.md)

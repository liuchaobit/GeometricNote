# 切丛、余切丛与辛几何基础

> 来源：Bullo & Lewis, *Geometric Control of Mechanical Systems — Supplementary Material* (2005)，S1.1。
> 论文原文：[papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](../../papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)

## 1. 微分形式（Differential forms）

**外 k-形式**：向量空间 $V$ 上的反对称 $(0,k)$-张量，记作 $\alpha\in\wedge_k(V)$，满足
$$\alpha(v_{\sigma(1)},\dots,v_{\sigma(k)}) = (-1)^{\mathrm{sgn}(\sigma)}\alpha(v_1,\dots,v_k).$$

**反对称化算子 Alt**：对 $t\in T_k^0(V)$，
$$\mathrm{Alt}(t)(v_1,\dots,v_k)=\frac{1}{k!}\sum_{\sigma\in S_k}(-1)^{\mathrm{sgn}(\sigma)}t(v_{\sigma(1)},\dots,v_{\sigma(k)}).$$

**楔积（wedge product）**：$\alpha\in\wedge_k(V),\ \beta\in\wedge_l(V)$，
$$\alpha\wedge\beta=\frac{(k+l)!}{k!\,l!}\mathrm{Alt}(\alpha\otimes\beta),\qquad \alpha\wedge\beta=(-1)^{kl}\beta\wedge\alpha.$$

基：$\dim\wedge_k(V)=\frac{n!}{(n-k)!k!}$；$\wedge_0(V)=\mathbb{R}$，$\wedge_1(V)=V^*$，$\wedge_n(V)\cong\mathbb{R}$。

**微分形式**：$\wedge_k(TM)$ 的光滑截面（定义 S1.4）。

## 2. 外微分（Exterior derivative）

定义 S1.5：$d\alpha\in\Gamma^\infty(\wedge_{k+1}(TM))$，坐标表示
$$d\alpha=\frac{\partial\alpha_{i_1\cdots i_k}}{\partial x^j}\,dx^j\wedge dx^{i_1}\wedge\cdots\wedge dx^{i_k}.$$

性质：
1. $df$ 即函数的微分；
2. $dd\alpha=0$；
3. $d(\alpha\wedge\beta)=d\alpha\wedge\beta+(-1)^k\alpha\wedge d\beta$；
4. $d(f^*\alpha)=f^*(d\alpha)$（拉回与外微分可交换）；
5. $\mathcal{L}_X(d\alpha)=d(\mathcal{L}_X\alpha)$。

## 3. 辛流形（Symplectic manifolds）

**定义 S1.6**：$(M,\omega)$ 为辛流形，其中 $\omega$ 是**闭**（$d\omega=0$）且**非退化**（$\omega^\flat:TM\to T^*M$ 为丛同构）的 2-形式。非退化性蕴含 $\dim M$ 为偶数。

**余切丛上的典范辛结构**：典范 1-形式（tautological form）
$$\theta_0=p_i\,dq^i\quad(\text{自然坐标}(q^i,p_i)),$$
典范辛形式
$$\omega_0=-d\theta_0=dq^i\wedge dp_i,\qquad [\omega_0]=\begin{pmatrix}0&I_n\\-I_n&0\end{pmatrix}.$$

**辛微分同胚**（定义 S1.7）：$\phi:M\to N$ 满足 $\phi^*\Omega=\omega$。

> 注（Remark S1.9）：不同文献辛形式符号约定可能相反，但哈密顿向量场局部坐标形式保持一致。

## 4. 哈密顿向量场（Hamiltonian vector fields）

**定义 S1.8**：给定哈密顿函数 $H$，哈密顿向量场
$$X_H(t,x)=-\omega^\sharp(dH(t,x)).$$

自然坐标 $(q^i,p_i)$ 下（式 S1.1）：
$$X_H=\frac{\partial H}{\partial p_i}\frac{\partial}{\partial q^i}-\frac{\partial H}{\partial q^i}\frac{\partial}{\partial p_i},$$
即哈密顿方程
$$\dot q^i=\frac{\partial H}{\partial p_i},\qquad \dot p_i=-\frac{\partial H}{\partial q^i}.$$

**守恒律**：若 $H$ 不显含时间，则 $\mathcal{L}_{X_H}H=-\omega(X_H,X_H)=0$，$H$ 为运动常数（能量守恒）。在最优控制中哈密顿量沿轨迹的常值性同样重要。

## 相关阅读
- [向量场的切提升与余切提升](./lifts.md)
- [Ehresmann 联络与 Sasaki 度量](./ehresmann-connections.md)
- [Jacobi 方程与伴随 Jacobi 方程](./jacobi-equations.md)

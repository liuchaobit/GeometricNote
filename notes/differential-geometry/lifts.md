# 向量场的切提升与余切提升

> 来源：Bullo & Lewis, *Supplementary Material* (2005)，S1.2。
> 论文原文：[papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](../../papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)

## 1. 切提升（Tangent lift）

对 $M$ 上（时变）向量场 $X$，其切提升 $X^T$ 是 $TM$ 上的向量场，局部坐标（式 S1.2）：
$$X^T = X^i\frac{\partial}{\partial x^i}+\left(\frac{\partial X^i}{\partial x^j}v^j+\frac{\partial X^i}{\partial t}\right)\frac{\partial}{\partial v^i}.$$

性质：
- $X^T$ 在纤维上是线性的（线性向量场）；
- 投影到 $X$：$T\pi_{TM}\circ X^T=X$；
- $X^T$ 的积分曲线刻画 $X$ 积分曲线的**变分**（见 Proposition S3.4 与 Jacobi 方程）。

## 2. 余切提升（Cotangent lift）

$X^{T^*}$ 是 $T^*M$ 上的向量场，定义为
$$X^{T^*}(t,\alpha_x)=\left.\frac{d}{ds}\right|_{s=0}T_x^*F_{t,-s}(\alpha_x),$$
局部坐标 $(x^i,p_i)$：
$$X^{T^*}=X^i\frac{\partial}{\partial x^i}-\frac{\partial X^j}{\partial x^i}p_j\frac{\partial}{\partial p_i}.$$

关键性质：$X^{T^*}$ 是以 $H_X(\alpha_x)=\langle\alpha_x;X(x)\rangle$ 为哈密顿量的哈密顿向量场。

## 3. 切提升与余切提升的联合性质

在 Whitney 和 $TM\oplus T^*M$ 上，$X^T\oplus X^{T^*}$ 保持配对函数 $f(v_x\oplus\alpha_x)=\langle\alpha_x;v_x\rangle$：
$$\mathcal{L}_{X^T\oplus X^{T^*}}f=0.$$
该性质唯一刻画余切提升。

## 4. 垂直提升的余切提升 $(\mathrm{vlft}(X))^{T^*}$

对 $T^*TQ$（自然坐标 $((q,v),(\alpha,\beta))$）：
$$(\mathrm{vlft}(X))^{T^*}=X^i\frac{\partial}{\partial v^i}-\frac{\partial X^j}{\partial q^i}\beta_j\frac{\partial}{\partial \alpha_i}.$$
在仿射联络分裂下（Lemma S4.24）：
$$(\mathrm{vlft}(X))^{T^*}(\alpha_{v_q}\oplus\beta_{v_q})=0\oplus X(q)\oplus\big(\tfrac{1}{2}T^*(\beta_{v_q},X(q))-(\nabla X)^*(\beta_{v_q})\big)\oplus 0.$$

## 5. 典范对合与典范自同态

- **典范对合** $I_Q:TTQ\to TTQ$：交换二重参数化曲面的两个参数；坐标下 $I_Q((q,v),(u,w))=((q,u),(v,w))$，且 $I_Q\circ I_Q=\mathrm{id}$。
- **典范自同态** $J_M\in\Gamma^\infty(T_1^1(TM))$：$J_M(X_{v_x})=\mathrm{vlft}_{v_x}(T\pi_{TM}(X_{v_x}))$，坐标下 $J_M=\tfrac{\partial}{\partial v^i}\otimes dx^i$。

## 相关阅读
- [切丛、余切丛与辛几何基础](./tangent-cotangent-bundle.md)
- [Ehresmann 联络与 Sasaki 度量](./ehresmann-connections.md)
- [Jacobi 方程与伴随 Jacobi 方程](./jacobi-equations.md)

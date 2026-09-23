# Ehresmann 联络与 Sasaki 度量

> 来源：Bullo & Lewis, *Supplementary Material* (2005)，S1.3。
> 论文原文：[papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](../../papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)

## 1. Ehresmann 联络

对纤维丛 $\pi:M\to B$，垂直子丛 $VM=\ker T\pi$。**Ehresmann 联络**即水平子丛 $HM$ 的选取，满足直和分解
$$TM=HM\oplus VM.$$
记 $\mathrm{ver}:TM\to VM$、$\mathrm{hor}:TM\to HM$，水平提升 $\mathrm{hlft}:T_bB\to H_xM$。联络形式 $\omega_{HM}=\mathrm{ver}$（$VM$-值 1-形式），**曲率**
$$\Omega_{HM}(u_x,v_x)=-\omega_{HM}([U,V](x));\qquad \Omega_{HM}=0\iff HM\text{ 可积}.$$

线性联络：向量丛上、垂直投影为向量丛映射的联络；对偶丛上诱导对偶联络。

## 2. 仿射联络诱导的 $TQ$ 上的 Ehresmann 联络

$Q$ 上仿射联络 $\nabla$、测地喷雾 $S$，在 $T_{v_q}TQ$ 给出分裂 $T_qQ\oplus T_qQ$（水平⊕垂直）。水平提升（命题 S1.29 附近）：
$$\mathrm{hlft}\left(\frac{\partial}{\partial q^i}\right)=\frac{\partial}{\partial q^i}-\frac{1}{2}(\Gamma^i_{ik}+\Gamma^i_{ki})v^k\frac{\partial}{\partial v^j}.$$

其曲率由曲率张量与挠率张量给出；对无挠 Levi-Civita 联络：
$$\Omega_{HTQ}\big(\mathrm{hlft}_{v_q}(u_q),\mathrm{hlft}_{v_q}(w_q)\big)=\mathrm{vlft}_{v_q}\big(R(u_q,w_q)v_q\big).$$

## 3. 更高阶丛上的联络

- $TTQ\to TQ$：利用二阶向量场得到分裂 $T_{X_{v_q}}TTQ\cong T_qQ\oplus T_qQ\oplus T_qQ\oplus T_qQ$；
- $T^*TQ\to TQ$：对偶构造，用于伴随 Jacobi 方程。

## 4. Sasaki 度量

$(Q,\mathbb{G})$ Riemann 流形、$\nabla$ 为 Levi-Civita 联络。切丛 $TQ$ 上的 Sasaki 度量（利用分裂 $T_{v_q}TQ\cong T_qQ\oplus T_qQ$）：
$$\mathbb{G}^T(u_{v_q}^1\oplus w_{v_q}^1,\,u_{v_q}^2\oplus w_{v_q}^2)=\mathbb{G}(u_{v_q}^1,u_{v_q}^2)+\mathbb{G}(w_{v_q}^1,w_{v_q}^2).$$

## 相关阅读
- [向量场的切提升与余切提升](./lifts.md)
- [Jacobi 方程与伴随 Jacobi 方程](./jacobi-equations.md)
- [切丛、余切丛与辛几何基础](./tangent-cotangent-bundle.md)

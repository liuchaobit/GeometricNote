# 可控性（Controllability）

> 来源：Bullo & Lewis, *Supplementary Material* (2005)，S2。
> 论文原文：[papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](../../papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)

本章扩展正文第 7 章的可控性结果：带基础外力、各向同性耗散力、以及具有对称性的系统。

## 1. 带基础外力的系统

受迫仿射联络控制系统（式 S2.1）：
$$\nabla_{\gamma'(t)}\gamma'(t)=\sum_{a=1}^m u^a(t)Y_a(\gamma(t))+Y(\gamma(t)),$$
对应 $TQ$ 上控制仿射系统 $\mathcal{G}_\Sigma=\{S+\mathrm{vlft}(Y),\,\mathrm{vlft}(Y_1),\dots,\mathrm{vlft}(Y_m)\}$。

**算法 S2.1**：归纳构造两个解析分布序列 $\mathcal{C}_{\mathrm{ver}}^{(k)}(\mathscr{Y},Y)$ 与 $\mathcal{C}_{\mathrm{hor}}^{(k)}(\mathscr{Y},Y)$（利用自由 Lie 代数与对称积的“原始括号”求值）。首几项生成元：
- $\mathcal{C}_{\mathrm{hor}}^{(1)}$ 由 $\{Y_1,\dots,Y_m\}$ 生成；
- $\mathcal{C}_{\mathrm{ver}}^{(1)}$ 由 $\{Y_1,\dots,Y_m,Y\}$ 生成；
- $\mathcal{C}_{\mathrm{hor}}^{(2)}$ 由 $\{\{Y_a:Y_b\}\}\cup\{\{Y_a,Y_b\}\}\cup\{\{Y_a:Y\}+[Y_a,Y]\}$ 生成；
- $\mathcal{C}_{\mathrm{ver}}^{(2)}$ 由 $\{\{Y_a:Y_b\}\}\cup\{\{Y_a:Y\}\}$ 生成。

**定理 S2.2**（可达性）：
$$\mathrm{Lie}^{(\infty)}(\mathcal{G}_\Sigma)_{0_{q_0}}\simeq\mathcal{C}_{\mathrm{hor}}^{(\infty)}(\mathscr{Y},Y)_{q_0}\oplus\mathcal{C}_{\mathrm{ver}}^{(\infty)}(\mathscr{Y},Y)_{q_0}\subset T_{q_0}Q\oplus T_{q_0}Q\simeq T_{0_{q_0}}TQ.$$
1. 从 $q_0$ **可达** $\iff$ $\mathcal{C}_{\mathrm{ver}}^{(\infty)}(\mathscr{Y},Y)_{q_0}=\mathcal{D}_{q_0}$ 且 $\mathcal{C}_{\mathrm{hor}}^{(\infty)}(\mathscr{Y},Y)_{q_0}=T_{q_0}Q$；
2. **构型可达**（configuration accessible）$\iff$ $\mathcal{C}_{\mathrm{hor}}^{(\infty)}(\mathscr{Y},Y)_{q_0}=T_{q_0}Q$。

**命题 S2.3**：$\mathcal{C}_{\mathrm{hor}}^{(\infty)}(\mathscr{Y},Y)$ 是对合分布。

**推论 S2.5**（STLC/STLCC 充分条件）：设 $Y(q_0)=0$。若每个“坏”对称积 $S\in\mathrm{Sym}_1(\mathfrak{m})^r$ 都能写成**更低阶**“好”对称积的线性组合（权重与障碍方法，沿袭定理 7.40），则：
1. $\mathcal{C}_{\mathrm{hor}}^{(\infty)}=\mathcal{D}_{q_0}$ 且 $\mathcal{C}_{\mathrm{hor}}^{(\infty)}=T_{q_0}Q$ $\Rightarrow$ **properly STLC**；
2. $\mathcal{C}_{\mathrm{hor}}^{(\infty)}=T_{q_0}Q$ $\Rightarrow$ **properly STLCC**。

> 注（Remark S2.6）：Lewis–Murray 1997 的定理 5.15 有误；无势能情形回到正文推论 7.41，有势能时必须用上述更精细的条件。

## 2. 各向同性耗散系统

各向同性耗散力 $F_{\mathrm{diss}}^\flat(v_q)=\delta v_q$（$\delta>0$），运动方程（式 S2.5）：
$$\nabla_{\gamma'(t)}\gamma'(t)=\sum_{a=1}^m u^a(t)Y_a(\gamma(t))-\delta\gamma'(t).$$

**定理 S2.7**（可达性）：
$$\mathrm{Lie}^{(\infty)}(\mathcal{G}_\Sigma)_{q_0}\simeq\mathrm{Lie}^{(\infty)}(\mathrm{Sym}^{(\infty)}(\mathscr{Y}))_{q_0}\oplus\mathrm{Sym}^{(\infty)}(\mathscr{Y})_{q_0}.$$
即：
1. 从 $q_0$ 可达 $\iff$ $\mathrm{Sym}^{(\infty)}(\mathscr{Y})_{q_0}=\mathcal{D}_{q_0}$ 且 $\mathrm{Lie}^{(\infty)}(\mathcal{D})_{q_0}=T_{q_0}Q$；
2. 构型可达 $\iff$ $\mathrm{Lie}^{(\infty)}(\mathrm{Sym}^{(\infty)}(\mathscr{Y}))_{q_0}=T_{q_0}Q$。

（证明利用 $[V_L,\mathrm{vlft}(Y_a)]=\mathrm{vlft}(Y_a)$、$[V_L,S]=S$，即 Liouville 向量场与生成元的对易结构。）

## 3. 对称性下的可控性

### 3.1 李群上的系统 $Q=G$

数据全部左不变，输入 $Y_a(g)=T_eL_g(\eta_a)$，$\eta_a\in\mathfrak{g}$。定义李代数上的对称积
$$\langle\xi:\eta\rangle_{\mathfrak{g}}=\langle X:Y\rangle(e),$$
Levi-Civita 情形（式 S2.6）：$\langle\xi:\eta\rangle_{\mathfrak{g}}=-\tfrac{1}{2}\big(\mathrm{ad}^*_\xi\ell(\eta)+\mathrm{ad}^*_\eta\ell(\xi)\big)$。

**命题 S2.8**（可达性）：
1. $\mathrm{Sym}^{(\infty)}(\mathscr{Y})_e$ 是含 $\mathscr{Y}_e$ 且对 $\langle\cdot:\cdot\rangle_{\mathfrak{g}}$ 封闭的最小子空间；
2. $\mathrm{Lie}^{(\infty)}(\mathrm{Sym}^{(\infty)}(\mathscr{Y}))_e$ 是其生成的最小李子代数；
3. $\mathrm{Sym}^{(\infty)}(\mathscr{Y})_g=T_eL_g(\mathrm{Sym}^{(\infty)}(\mathscr{Y})_e)$；
4. $\mathrm{Lie}^{(\infty)}(\mathrm{Sym}^{(\infty)}(\mathscr{Y}))_g=T_eL_g(\mathrm{Lie}^{(\infty)}(\mathrm{Sym}^{(\infty)}(\mathscr{Y}))_e)$。

优点：只需在单位元做**代数运算**，无需引入坐标（对 $SO(3)$、$SE(3)$ 尤其方便）。

**例 S2.10**：平面刚体（$SE(2)$，带推进器）。$\eta_1=\tfrac12 e_2$，$\eta_2=-\tfrac12e_1+\tfrac1m e_3$；对称积 $\langle\eta_1:\eta_2\rangle=-\tfrac{h}{mJ}e_3$ 等，由此重得 7.4.2 节可控性结论。

### 3.2 主纤维丛上的系统

$\pi:Q\to B=Q/G$ 为主纤维丛，$G$ 为对称群，$VQ=\ker T\pi$，水平子丛 $HQ=VQ^{\perp_G}$。动量映射 $J_Q:TQ\to\mathfrak{g}^*$。

**命题 S2.11**：水平分布 $HQ$ 光滑、正则、测地不变，且 $HQ=J_Q^{-1}(0)$。

**定理 S2.12**（主丛上的可控性）：
1. 若 $\dim G>0$，则 $\Sigma$ 从任何 $q$ 都**不可达**；
2. 若 $\mathrm{Lie}^{(\infty)}(J_Q^{-1}(0))=TQ$ 且 $V=0$：$\Sigma_B$ 从 $\pi(q)$ 可达 $\Rightarrow$ $\Sigma$ 从 $q$ 构型可达；
3. 定理 7.40 的假设在 $q$ 成立 $\iff$ 在 $\pi(q)$ 成立（STLC 假设等价）。

机械联络 $\mathcal{A}_G:TQ\to\mathfrak{g}$、曲率 $B_G(u_q,v_q)=-\mathcal{A}_G(\mathrm{hor}(U),\mathrm{hor}(V))(q)$，并有
$$\langle Y_a:Y_b\rangle=\mathrm{hor}\big(\langle Y_{B,a}:Y_{B,b}\rangle\big).$$

**例 S2.13**：机器人腿（$G=SO(2)$ 作用在 $Q=\mathbb{R}_+\times S^1\times S^1$），验证了定理 S2.12 的全部四类结论。

## 相关阅读
- [受迫仿射联络控制系统（模型与线性化）](./linearization-relative-equilibria.md)
- [相对平衡的镇定](./stabilization-relative-equilibria.md)

# 相对平衡的镇定（Stabilization of relative equilibria）

> 来源：Bullo & Lewis, *Supplementary Material* (2005)，S3.4–S3.5。
> 论文原文：[papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](../../papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)

## 1. 镇定问题表述

**受控相对平衡** $(\chi,u_0)$：$\chi(t)$ 是无穷小对称 $X$ 的积分曲线，且常值控制 $u_0$ 满足运动方程
$$\nabla_{\chi'(t)}^{\mathbb{G}}\chi'(t)=-\mathrm{grad}\,V(\chi(t))+\sum_{a=1}^m u_0^a\,\mathbb{G}^\sharp\circ F^a(\chi(t)).$$

**$X$-不变反馈**：反馈值沿对称群轨道不变。核心思想：**先在约化空间设计反馈，再提升回原系统**。

**命题 S3.32**：约化系统镇定 $\Rightarrow$ 原系统的 base+fiber 镇定。

## 2. 线性反馈镇定框架

1. 对约化线性系统 $\Sigma^{\mathrm{red,lin}}$ 设计 PD 类反馈；
2. 增益矩阵须满足**相容性条件**（compatible gain），尊重水平—垂直分解；
3. 若线性化系统能控，可实现局部渐近 base&fiber 镇定；
4. **势能塑形（potential shaping）**扩展至相对平衡情形。

## 3. 要点与提醒

- 优先**约化后设计、再提升**，避免在高维构型空间直接设计；
- 区分两个目标：**base 方向（商流形）镇定** 与 **fiber（对称方向）镇定**；
- 陀螺耦合项可能破坏仅势能型镇定的渐近性，需要阻尼注入或非线性反馈。

## 相关阅读
- [相对平衡的线性化](./linearization-relative-equilibria.md)
- [可控性](./controllability.md)
- [最优控制与极大值原理](./optimal-control.md)

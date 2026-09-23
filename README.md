# GeometricNote

微分几何与几何控制个人知识库，整理自 **Francesco Bullo & Andrew D. Lewis, *Geometric Control of Mechanical Systems: Modeling, Analysis, and Design for Simple Mechanical Control Systems — Supplementary Material*, February 2, 2005**。

## 论文原文

- [papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf](./papers/2004_Geometric_control_of_mechanical_systems_Bullo_Lewis.pdf)
- 主书：*Geometric Control of Mechanical Systems*, Texts in Applied Mathematics, Springer, 2004。

## 目录结构

```
GeometricNote/
├── index.html          # Wiki 单页站点（KaTeX 公式渲染）
├── README.md
├── papers/             # 论文原文 PDF
└── notes/
    ├── differential-geometry/   # 微分几何（对应论文 S1）
    └── geometric-control/       # 几何控制基础（对应论文 S2–S4）
```

## 笔记索引

### 微分几何（S1）
1. [切丛、余切丛与辛几何](./notes/differential-geometry/tangent-cotangent-bundle.md)
2. [向量场的切提升与余切提升](./notes/differential-geometry/lifts.md)
3. [Ehresmann 联络与 Sasaki 度量](./notes/differential-geometry/ehresmann-connections.md)
4. [Jacobi 方程与伴随 Jacobi 方程](./notes/differential-geometry/jacobi-equations.md)

### 几何控制基础（S2–S4）
1. [可控性（含各向同性耗散、对称性）](./notes/geometric-control/controllability.md)
2. [相对平衡的线性化](./notes/geometric-control/linearization-relative-equilibria.md)
3. [相对平衡的镇定](./notes/geometric-control/stabilization-relative-equilibria.md)
4. [最优控制与极大值原理](./notes/geometric-control/optimal-control.md)

## 使用说明

1. 仓库为 **Private**；GitHub Pages 私有仓库无法公开访问，仅本地浏览或授权访问。
2. `index.html` 为 Wiki 单页站点，内置 KaTeX；打开方式：
   - 本地直接双击打开（公式经 CDN 渲染，需联网）；
   - 或 `python3 -m http.server` 后在浏览器访问。
3. 所有笔记均标注来源章节（S1–S4）并附论文链接，关键定理公式忠于原文。
4. 新增笔记：在 `notes/` 对应分类目录添加 `.md`，并在 `index.html` 的 `<nav>` 与 `<main>` 中同步加入条目。

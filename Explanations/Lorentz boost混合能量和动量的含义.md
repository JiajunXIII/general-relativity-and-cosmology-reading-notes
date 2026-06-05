---
title: Lorentz boost混合能量和动量的含义
tags:
  - explanation
  - relativity/special-relativity
  - weinberg
---

# Lorentz boost混合能量和动量的含义

## 原文片段

> 如果 $p$ 守恒则 $E$ 必守恒，因为在 Lorentz 变换联系的两个坐标系中动量守恒会约束四动量的时间分量。

## 我在对话中提出的问题

我问：“‘Lorentz boost 会混合时间和空间。也就是说，一个参考系里的纯空间动量分量，在另一个参考系里会含有原来的时间分量 $p^0$，也就是能量。’这句话是什么意思？同时需要解释 Lorentz boost。”

## 已给出的解答

这句话的意思是：换到一个相对运动的惯性系后，新参考系测到的动量分量，不只是旧参考系的动量分量，还会包含旧参考系的能量。

四动量是四维矢量。既然四维坐标 $(x,t)$ 在 boost 下会混合，那么任何四维矢量也会用同样方式混合。在 $c=1$ 下，四动量可以写成

$$
p^\alpha=(p_x,p_y,p_z,E).
$$

考虑沿 $x$ 方向的 boost。它的变换形式可以写成

$$
p'_x=\gamma(p_x-uE),
$$

$$
E'=\gamma(E-u p_x).
$$

符号正负取决于定义 $S'$ 相对 $S$ 的运动方向；但结构不变。重点是

$$
p'_x \text{ 含有 } E,
$$

并且

$$
E' \text{ 含有 } p_x.
$$

这就是“一个参考系里的纯空间动量分量，在另一个参考系里会含有原来的时间分量 $p^0$，也就是能量”的含义。

这里的“含有”不是说能量神秘地变成了动量，而是说：同一个四维矢量，在不同坐标系下分解成空间分量和时间分量时，分解方式变了。类似地，在二维平面里，如果旋转坐标轴，新的 $x'$ 坐标会同时包含旧的 $x$ 和旧的 $y$。Lorentz boost 可以理解成 spacetime 中的 hyperbolic rotation。

## 简明解释

假设一个粒子在 $S$ 系中静止，则

$$
p_x=0,\qquad E=m.
$$

现在换到一个相对它运动的参考系 $S'$。由 boost 公式

$$
p'_x=\gamma(p_x-uE),
$$

代入 $p_x=0$，得到

$$
p'_x=-\gamma uE=-\gamma um.
$$

这个粒子在原参考系中没有空间动量，但在新参考系中有动量。新动量来自四动量的时间分量 $E$ 被 boost 混入了空间分量。物理上这完全合理：一个粒子在自己静止系里不动，但在另一个相对运动的参考系里当然在运动，因此有动量。

这也解释了 Weinberg 的守恒性论证。若某个反应在 $S$ 系中满足

$$
\Delta\sum_n p_{n,x}=0,
$$

而在 boosted frame 中也要求

$$
\Delta\sum_n p'_{n,x}=0,
$$

则

$$
\Delta \sum_n p'_{n,x}
=
\gamma\left(
\Delta \sum_n p_{n,x}
-
u\Delta \sum_n E_n
\right).
$$

第一个参考系中动量守恒，所以 $\Delta\sum_n p_{n,x}=0$。于是

$$
0
=
-\gamma u\Delta\sum_n E_n.
$$

如果 boost 速度 $u\neq 0$，就得到

$$
\Delta\sum_n E_n=0.
$$

因此，在相对论里，如果要求动量守恒在所有惯性系中都成立，就必须同时要求能量守恒。真正自然的守恒律是四动量守恒：

$$
\Delta\sum_n p_n^\alpha=0.
$$

## 相关概念

- [[Lorentz boost]]
- [[四动量]]
- [[Lorentz变换与Poincare变换]]
- [[Explanations/四动量总变化量求和的含义]]
- [[Explanations/标准boost空间部分的意义]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.4-能量和动量]]

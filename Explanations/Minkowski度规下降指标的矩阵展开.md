---
title: Minkowski度规下降指标的矩阵展开
tags:
  - explanation
  - relativity/tensor
  - weinberg
---

# Minkowski度规下降指标的矩阵展开

## 原文片段

> 在特殊相对论中，metric 是 Minkowski metric：
>
> $$
> \eta_{\alpha\beta}=\mathrm{diag}(1,1,1,-1).
> $$
>
> 所以如果
>
> $$
> u^\alpha=(u^1,u^2,u^3,u^0),
> $$
>
> 那么降指标后
>
> $$
> u_\alpha=(u^1,u^2,u^3,-u^0).
> $$

## 我在对话中提出的问题

我说：我不理解这一步。

## 已给出的解答

降指标定义为

$$
u_\alpha=\eta_{\alpha\beta}u^\beta.
$$

Weinberg 的指标顺序是 $1,2,3,0$，因此

$$
\eta_{\alpha\beta}
=
\begin{pmatrix}
1&0&0&0\\
0&1&0&0\\
0&0&1&0\\
0&0&0&-1
\end{pmatrix}.
$$

把它乘到列向量

$$
u^\beta
=
\begin{pmatrix}
u^1\\
u^2\\
u^3\\
u^0
\end{pmatrix}
$$

上，得到

$$
u_\alpha
=
\begin{pmatrix}
u^1\\
u^2\\
u^3\\
-u^0
\end{pmatrix}.
$$

因此

$$
u_1=u^1,\qquad
u_2=u^2,\qquad
u_3=u^3,\qquad
u_0=-u^0.
$$

## 简明解释

降指标就是“用 metric 乘一下”。Weinberg 的 metric 对空间方向乘 $+1$，对时间方向乘 $-1$，所以时间分量变号。

## 相关概念

- [[协变矢量与逆变矢量]]
- [[Minkowski度规号差与eta00]]
- [[四维速度]]
- [[Explanations/四维速度内积记号的含义]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.3-粒子动力学]]

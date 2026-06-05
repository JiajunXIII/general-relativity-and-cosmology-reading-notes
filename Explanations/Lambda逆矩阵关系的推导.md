---
title: Lambda逆矩阵关系的推导
tags:
  - explanation
  - derivation
  - relativity/lorentz
  - tensor-analysis
---

# Lambda逆矩阵关系的推导

## 原文片段

> 则知 $\Lambda_\alpha{}^\beta$ 是矩阵 $\Lambda^\beta{}_\alpha$ 的逆，即
>
> $$
> \Lambda_\alpha{}^\gamma\Lambda^\alpha{}_\beta=\delta^\gamma{}_\beta .
> $$

## 我在对话中提出的问题

我问：为什么

$$
\Lambda_\alpha{}^\gamma \Lambda^\alpha{}_\beta
=
\delta^\gamma{}_\beta?
$$

## 已经给出的解答

Lorentz 变换保持 Minkowski 内积不变，因此

$$
\eta_{\alpha\delta}\Lambda^\alpha{}_\beta\Lambda^\delta{}_\varepsilon
=
\eta_{\beta\varepsilon}.
$$

又由定义

$$
\Lambda_\alpha{}^\gamma
=
\eta_{\alpha\delta}\eta^{\gamma\varepsilon}
\Lambda^\delta{}_\varepsilon .
$$

代入得到

$$
\Lambda_\alpha{}^\gamma \Lambda^\alpha{}_\beta
=
\eta_{\alpha\delta}\eta^{\gamma\varepsilon}
\Lambda^\delta{}_\varepsilon
\Lambda^\alpha{}_\beta .
$$

把 $\eta^{\gamma\varepsilon}$ 提出来：

$$
\Lambda_\alpha{}^\gamma \Lambda^\alpha{}_\beta
=
\eta^{\gamma\varepsilon}
\left(
\eta_{\alpha\delta}
\Lambda^\alpha{}_\beta
\Lambda^\delta{}_\varepsilon
\right).
$$

括号中正是度规不变性给出的 $\eta_{\beta\varepsilon}$，所以

$$
\Lambda_\alpha{}^\gamma \Lambda^\alpha{}_\beta
=
\eta^{\gamma\varepsilon}\eta_{\beta\varepsilon}
=
\delta^\gamma{}_\beta .
$$

## 简明解释

$\Lambda^\alpha{}_\beta$ 用于逆变分量从旧参考系到新参考系的变换，$\Lambda_\alpha{}^\gamma$ 是相应的反向变换矩阵。两者连续作用等于什么都不做，因此得到单位张量 $\delta^\gamma{}_\beta$。

## 相关概念

- [[Minkowski度规的指标形式]]
- [[Kronecker delta与单位变换]]
- [[协变矢量与逆变矢量]]
- [[Lorentz变换与Poincare变换]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.5-矢量和张量]]

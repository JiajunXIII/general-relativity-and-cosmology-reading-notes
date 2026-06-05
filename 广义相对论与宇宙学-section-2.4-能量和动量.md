---
title: 广义相对论与宇宙学 section 2.4 能量和动量
tags:
  - reading-note
  - relativity/special-relativity
  - weinberg
source_markdown: "E:\\JiajunX\\PycharmProjects\\Physics_for_Intelligence\\temp\\teacher-pdf-reader\\weinberg_gr_pages_40_53.md"
---

# 广义相对论与宇宙学 section 2.4 能量和动量

本节的核心不是重新发明动量和能量，而是说明为什么在相对论里，动量和能量必须合在一起，成为一个四维矢量。上一节 2.3 已经把 Newton 第二定律改写成四维形式：

$$
f^\alpha = m \frac{d^2 x^\alpha}{d\tau^2}.
$$

这里 $x^\alpha$ 是 spacetime 坐标，$\tau$ 是 proper time，也就是粒子自己携带的钟所测到的时间。这个式子自然提示我们：如果加速度是 $d^2x^\alpha/d\tau^2$，那么它前面的一阶导数 $dx^\alpha/d\tau$ 就应该扮演速度的四维版本。于是 Weinberg 定义 [[Concepts/四动量|四动量]]，也就是 energy-momentum four-vector：

$$
p^\alpha \equiv m \frac{dx^\alpha}{d\tau}.
\tag{2.4.1}
$$

这一步不是随便定义，而是为了让动力学方程保持 Lorentz covariant，也就是说所有惯性系都能用同一种形式写物理定律。有了 $p^\alpha$，相对论版 Newton 第二定律就变成：

$$
\frac{dp^\alpha}{d\tau} = f^\alpha.
\tag{2.4.2}
$$

这和非相对论中的 $d\mathbf p/dt=\mathbf F$ 很像，只是这里的时间参数从坐标时间 $t$ 换成了 proper time $\tau$，动量也从三维矢量变成了四维矢量。

## 空间分量为什么是动量

先看 $p^\alpha$ 的空间分量。由于

$$
d\tau = \sqrt{dt^2-d\mathbf x^2},
$$

而

$$
\mathbf v = \frac{d\mathbf x}{dt},
$$

所以

$$
d\tau = \sqrt{1-v^2}\,dt.
$$

因此

$$
\frac{dt}{d\tau} = \frac{1}{\sqrt{1-v^2}} \equiv \gamma.
$$

这就是 Lorentz factor：

$$
\gamma = (1-v^2)^{-1/2}.
\tag{2.4.5}
$$

现在计算 $p^\alpha$ 的空间部分：

$$
\mathbf p = m \frac{d\mathbf x}{d\tau}.
$$

把 $d\mathbf x/d\tau$ 拆成两段：

$$
\frac{d\mathbf x}{d\tau}
=
\frac{d\mathbf x}{dt}\frac{dt}{d\tau}
=
\mathbf v \gamma.
$$

所以得到

$$
\mathbf p = m\gamma \mathbf v.
\tag{2.4.3}
$$

这就是 relativistic momentum。它和 Newton 动量 $\mathbf p=m\mathbf v$ 的差别只在于多了 $\gamma$。当 $v\ll 1$ 时，$\gamma\approx 1$，于是相对论动量自动退化为普通动量：

$$
\mathbf p = m\mathbf v + O(v^3).
\tag{2.4.6}
$$

直觉上，速度越接近光速，$\gamma$ 越大，因此同样增加一点速度，需要越来越大的动量变化。这是有质量粒子无法被加速到光速的数学原因之一。

## 时间分量为什么是能量

接着看时间分量。因为 $x^0=t$，所以

$$
p^0 = m\frac{dt}{d\tau}.
$$

而刚才已经知道

$$
\frac{dt}{d\tau}=\gamma.
$$

于是

$$
p^0 \equiv E = m\gamma.
\tag{2.4.4}
$$

Weinberg 把 $p^0$ 定义为能量。这里使用的是自然单位 $c=1$。如果恢复 $c$，这就是更熟悉的

$$
E = \gamma mc^2.
$$

在低速极限下，对 $\gamma$ 展开：

$$
\gamma = 1+\frac12 v^2+O(v^4).
$$

这个展开来自 Taylor 展开和 generalized binomial theorem，见 [[Explanations/Gamma因子低速展开的推导|Gamma因子低速展开的推导]]；其中核心函数 $(1-x)^{-1/2}$ 的级数公式见 [[Explanations/函数一减x的负二分之一次方Taylor展开的推导|函数一减x的负二分之一次方Taylor展开的推导]]。

所以

$$
E = m\gamma
=
m+\frac12 mv^2+O(v^4).
\tag{2.4.7}
$$

这句话非常重要：相对论能量包含两部分。第一部分是 $m$，也就是静止能量；在普通单位里是 $mc^2$。第二部分是

$$
\frac12 mv^2,
$$

也就是低速时熟悉的 Newton 动能。这里的 $v$ 在自然单位中是无量纲速度；恢复 $c$ 时需要区分 $v$ 与有单位速度 $u$，见 [[Explanations/自然单位c等于1时动能项的单位恢复|自然单位c等于1时动能项的单位恢复]]。

所以相对论并不是推翻 Newton 力学，而是在低速极限下包含 Newton 力学，同时额外告诉我们：即使粒子静止，它也有能量。这就是 $E=mc^2$ 的来源之一。Weinberg 在这里用 $c=1$，所以写作 $E=m$。如果一个系统发生质量亏损，例如核裂变、核聚变或放射性衰变，减少的静质量会转化成其他形式的能量。

## 为什么不推荐相对论质量

书中提到，有些人会把 $m\gamma$ 称为 relativistic mass，记作 $\tilde m$，这样就能写成

$$
\mathbf p = \tilde m \mathbf v.
$$

但 Weinberg 明确说他不采用这个习惯。他说“质量”总是指常数 $m$，也就是 invariant mass 或 rest mass。

原因是 $m$ 是 Lorentz invariant，不同惯性系都同意它的值；而 $m\gamma$ 依赖观察者，因为 $\gamma$ 依赖速度。把 $m\gamma$ 也叫“质量”，容易让人误以为质量本身变了。更好的说法是：质量不变，能量和动量随参考系改变。

## 为什么它们真的应该叫动量和能量

Weinberg 接下来问了一个更根本的问题：为什么有权把 $\mathbf p$ 和 $E$ 叫作动量和能量？

答案不是因为名字像，而是因为它们具有正确的守恒性质。在物理中，动量和能量之所以重要，是因为它们是 conserved quantities。如果一个反应中，总动量和总能量在一个惯性系中守恒，那么我们希望所有 Lorentz 相关的惯性系也都认为它们守恒。否则守恒定律就不是相对论性的物理定律，而只是某个坐标系里的偶然说法。

关键是：因为 $dx^\alpha$ 是四维矢量，$m$ 和 $d\tau$ 是 Lorentz invariant，所以

$$
p^\alpha = m\frac{dx^\alpha}{d\tau}
$$

本身也是四维矢量。因此 Lorentz 变换下有

$$
p'^\alpha = \Lambda^\alpha_{\ \beta}p^\beta.
$$

如果一个反应里所有粒子的四动量总变化是

$$
\Delta \sum_n p_n^\beta = 0,
$$

那么在另一个惯性系中，

$$
\Delta \sum_n p_n'^\alpha
=
\Lambda^\alpha_{\ \beta}
\Delta \sum_n p_n^\beta
=
0.
$$

这个式子的意思是“反应前所有粒子的四动量总和等于反应后所有粒子的四动量总和”，见 [[Explanations/四动量总变化量求和的含义|四动量总变化量求和的含义]]。

这就是本节的概念核心。相对论中不是分别发明能量守恒和动量守恒，而是把它们统一成一句话：

$$
\Delta \sum_n p_n^\alpha = 0.
$$

空间分量给出动量守恒，时间分量给出能量守恒。

## 动量守恒为什么会逼出能量守恒

Weinberg 还指出一个事实：如果你要求动量守恒在不同惯性系中都成立，那么能量守恒也会被迫出现。

直觉是这样的：[[Concepts/Lorentz boost|Lorentz boost]] 会混合时间和空间。也就是说，一个参考系里的纯空间动量分量，在另一个参考系里会含有原来的时间分量 $p^0$，也就是能量。这个说法的具体含义见 [[Explanations/Lorentz boost混合能量和动量的含义|Lorentz boost混合能量和动量的含义]]。

形式上，如果

$$
\Delta \sum_n p_n^i=0,
$$

而另一个参考系中也要求

$$
\Delta \sum_n p_n'^i=0,
$$

但

$$
\Delta \sum_n p_n'^i
=
\Lambda^i_{\ \beta}
\Delta \sum_n p_n^\beta.
$$

展开后包含一项

$$
\Lambda^i_{\ 0}
\Delta \sum_n p_n^0.
$$

对于 boost，$\Lambda^i_{\ 0}$ 一般不为零。因此要让不同参考系中动量都守恒，就必须有

$$
\Delta \sum_n p_n^0=0,
$$

也就是能量守恒。

这说明在相对论里，能量守恒不是附加规则，而是 Lorentz symmetry 和动量守恒共同要求的结果。

## 能量-动量关系

接下来 Weinberg 从定义中消去速度，得到最重要的能量-动量关系：

$$
E(\mathbf p)=\sqrt{\mathbf p^2+m^2}.
\tag{2.4.8}
$$

推导很短。由

$$
\mathbf p = m\gamma \mathbf v
$$

所以

$$
\mathbf p^2 = m^2\gamma^2 v^2.
$$

而

$$
E=m\gamma.
$$

所以

$$
E^2-\mathbf p^2
=
m^2\gamma^2(1-v^2).
$$

又因为

$$
\gamma^2 = \frac{1}{1-v^2},
$$

因此

$$
E^2-\mathbf p^2=m^2.
$$

也就是

$$
E^2=\mathbf p^2+m^2.
$$

用 Weinberg 的 metric convention，$\eta_{\alpha\beta}$ 的空间部分为正，时间部分为负，所以同一个关系也可写成四维不变量：

$$
\eta_{\alpha\beta}p^\alpha p^\beta = -m^2.
\tag{2.4.9}
$$

因为

$$
\eta_{\alpha\beta}p^\alpha p^\beta
=
\mathbf p^2 - E^2
=
-m^2.
$$

这说明 $m$ 是四动量长度的 invariant。不同观察者会测到不同的 $E$ 和 $\mathbf p$，但都会同意

$$
E^2-\mathbf p^2=m^2.
$$

这和不同观察者测到不同的时间间隔、空间间隔，但同意 spacetime interval，是同一种思想。

## 无质量粒子

最后，Weinberg 讨论 $m=0$ 的情况。对于光子这样的无质量粒子，不能直接使用

$$
\mathbf p=m\gamma\mathbf v,\qquad E=m\gamma,
$$

因为 $m=0$，同时 $v=1$ 使 $\gamma\to\infty$，形式上变成 $0\cdot\infty$ 的不定式。

但是能量-动量关系仍然有效。令 $m=0$，得到

$$
E=|\mathbf p|.
$$

同时，从有质量粒子的公式可以得到普遍关系：

$$
\frac{\mathbf p}{E}=\mathbf v.
\tag{2.4.10}
$$

对于无质量粒子，

$$
\frac{|\mathbf p|}{E}=1.
$$

所以速度大小就是 $1$，也就是光速。这说明无质量粒子必须以光速运动；反过来，有质量粒子因为 $m\neq 0$，不能达到 $v=1$。

## 本节核心图像

这一节可以用一句话概括：相对论把能量和动量合并成同一个几何对象 $p^\alpha$。

如果只看三维空间，会觉得动量 $\mathbf p$ 和能量 $E$ 是两个不同概念。但在四维 spacetime 中，它们只是同一个四矢量的不同分量。Lorentz boost 就像在 spacetime 中换观察角度；换角度以后，原来的时间分量和空间分量会混合。因此能量和动量也会混合。

这就是为什么相对论里最自然的守恒律不是单独写能量守恒和动量守恒，而是写：

$$
\Delta \sum_n p_n^\alpha=0.
$$

它一次性包含两者，并且自动保证所有惯性观察者都同意这个守恒律。

## 常见误区

第一个误区是把 $m\gamma$ 当成真正变化的质量。Weinberg 的约定是：质量 $m$ 是 invariant mass，不随参考系变。

第二个误区是忘记本章使用 $c=1$。恢复单位后，$E=m\gamma$ 应写为 $E=\gamma mc^2$。

第三个误区是以为 $E=m$ 只是一种符号技巧。它表示静止能量；恢复单位就是 $E=mc^2$。

第四个误区是把 $E=\sqrt{\mathbf p^2+m^2}$ 理解为普通三维公式。它背后真正的不变量是四维关系 $\eta_{\alpha\beta}p^\alpha p^\beta=-m^2$。

第五个误区是对无质量粒子直接套 $\mathbf p=m\gamma\mathbf v$。应使用 $E=|\mathbf p|$ 和 $\mathbf p/E=\mathbf v$。

## 自检问题

1. 为什么 $p^\alpha=m dx^\alpha/d\tau$ 一定是四维矢量？
2. 为什么 $p^0$ 被解释为能量，而不是某个任意的新量？
3. 从 $E=m\gamma$ 如何得到低速极限 $E=m+\frac12mv^2+\cdots$？
4. 为什么一个参考系中四动量守恒会推出所有 Lorentz 相关参考系中四动量守恒？
5. 对光子而言，为什么 $m=0$ 会推出 $E=|\mathbf p|$？

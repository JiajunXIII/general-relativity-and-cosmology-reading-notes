---
title: 广义相对论与宇宙学 section 2.3 粒子动力学
tags:
  - reading-note
  - relativity/special-relativity
  - weinberg
source_markdown: "E:\\JiajunX\\PycharmProjects\\Physics_for_Intelligence\\temp\\teacher-pdf-reader\\weinberg_gr_pages_40_53.md"
---

# 广义相对论与宇宙学 section 2.3 粒子动力学

我先说明一下：源 Markdown 里中文有明显编码损坏，但 section 2.3 的公式和逻辑链条是完整的。下面按 Weinberg 的原始思路来讲，不只讲公式结果，而是讲他为什么这样定义。

## 1. 本节要解决什么问题

2.1 和 2.2 已经建立了两个核心事实：

第一，惯性系之间不是 Galilean transformation，而是 Lorentz transformation。也就是说，时空坐标 $x^\alpha$ 的变换必须保持固有时：

$$
d\tau^2 = dt^2 - d\boldsymbol{x}^2
$$

第二，运动时钟会 time dilation，因此当粒子速度接近光速时，不能再直接用 Newton 形式：

$$
\boldsymbol{F} = m \frac{d^2 \boldsymbol{x}}{dt^2}
$$

因为这里的 $t$ 是某个特定参考系里的坐标时间，不是 Lorentz invariant 的量。不同观察者的 $t$ 不同，如果我们用 $t$ 做动力学参数，方程很难自动保持相对论协变性。

所以 2.3 的核心问题是：怎样把 Newton 第二定律改写成一个 Lorentz covariant 的形式，使所有惯性系都同意它的结构？

Weinberg 的回答是：不要用三维位置 $\boldsymbol{x}(t)$ 直接写运动方程，而是用四维世界线 $x^\alpha(\tau)$，并用固有时 $\tau$ 作为参数。

## 2. 从“瞬时静止系”开始理解

先讲物理图像。假设一个粒子在某个实验室系中高速运动，速度为 $\boldsymbol{v}$。在实验室系中，你不能直接用普通 Newton 力学。但是在某一瞬间，我们总可以做一个 Lorentz boost，切换到粒子的 instantaneous rest frame，也就是粒子在这一瞬间静止的参考系。

在这个瞬时静止系里，粒子的速度暂时为零，因此普通 Newton 力的概念仍然有清楚意义。假设我们知道在这个瞬时静止系中作用在粒子上的普通三维力 $\boldsymbol{F}$。那么可以想象一种笨办法：

先 boost 到粒子瞬时静止系，在那里用 Newton 公式算出一个小的速度改变；然后再 boost 回原来的实验室系；下一瞬间继续重复这个过程。

这个办法概念上可行，但计算上很麻烦。Weinberg 接下来做的事情，就是把这个“每一瞬间切到静止系”的过程包装成一个四维方程。

## 3. 四维力的定义

Weinberg 定义 relativistic force，也就是 [[Concepts/四维力|四维力]] $f^\alpha$：

$$
f^\alpha = m \frac{d^2 x^\alpha}{d\tau^2}
\tag{2.3.1}
$$

这里：

- $x^\alpha(\tau)$ 是粒子的四维世界线；
- $\tau$ 是粒子自身携带的固有时；
- $m$ 是静质量；
- $f^\alpha$ 是四维量，不只是普通三维力。

这个定义非常像 Newton 第二定律，但有两个关键替换：

Newton 形式是：

$$
\boldsymbol{F} = m \frac{d^2 \boldsymbol{x}}{dt^2}
$$

相对论形式是：

$$
f^\alpha = m \frac{d^2 x^\alpha}{d\tau^2}
$$

也就是说：

- 三维位置 $\boldsymbol{x}$ 变成四维坐标 $x^\alpha$；
- 坐标时间 $t$ 变成固有时 $\tau$；
- 三维力 $\boldsymbol{F}$ 变成四维力 $f^\alpha$。

为什么这一步自然？因为 $d\tau$ 是 Lorentz invariant，所有惯性观察者都同意它。因此用 $\tau$ 参数化运动，可以让方程天生适合 Lorentz transformation。

## 4. 四维力必须满足两个条件

定义了 $f^\alpha$ 之后，Weinberg 要说明它和普通 Newton 力 $\boldsymbol{F}$ 的关系。这里有两个性质。

第一个性质：在粒子瞬时静止系中，四维力应该退化为普通力。

如果粒子瞬时静止，那么：

$$
d\tau = dt
$$

此时空间分量应该就是普通 Newton 力：

$$
f^i = F^i
$$

而时间分量定义为零：

$$
F^0 \equiv 0
\tag{2.3.2}
$$

所以在瞬时静止系中，我们可以把四维力写成：

$$
F^\alpha = (F^i, F^0) = (\boldsymbol{F}, 0)
$$

注意 Weinberg 的指标顺序是空间指标 $1,2,3$ 加时间指标 $0$，并且 metric 约定是：

$$
\eta_{\alpha\beta} = \mathrm{diag}(+1,+1,+1,-1)
$$

所以这里的时间分量在最后。

第二个性质：四维力必须像四维矢量那样变换。

因为 $dx^\alpha$ 是四维矢量，而 $d\tau$ 是 invariant，所以：

$$
\frac{dx^\alpha}{d\tau}
$$

也是四维矢量。再对 $\tau$ 求导，仍然得到四维矢量。因此：

$$
f^{\prime \alpha}
=
\Lambda^\alpha_{\ \beta} f^\beta
\tag{2.3.3}
$$

这就是四维力的 Lorentz transformation law。

这一步非常重要：它保证如果某个观察者写下了 $f^\alpha = m d^2x^\alpha/d\tau^2$，另一个 Lorentz 相关的观察者也会写下同样形式的方程。物理定律的形式不依赖于惯性系。

## 5. 从瞬时静止系变回实验室系

现在问题变成：如果我们知道粒子瞬时静止系里的普通力 $\boldsymbol{F}$，那么实验室系里的四维力 $f^\alpha$ 是什么？

设粒子在实验室系中的速度是 $\boldsymbol{v}$。我们选择一个 Lorentz boost $\Lambda(\boldsymbol{v})$，它把粒子静止系中的粒子变成实验室系中速度为 $\boldsymbol{v}$ 的粒子。

因为 $f^\alpha$ 是四维矢量，所以：

$$
f^\alpha
=
\Lambda^\alpha_{\ \beta}(\boldsymbol{v}) F^\beta
\tag{2.3.4}
$$

这句话的意思很朴素：先在粒子的瞬时静止系中写出四维力 $(\boldsymbol{F},0)$，然后用 Lorentz boost 把它变到实验室系。

这就是 Weinberg 把“反复切换瞬时静止系”的笨办法压缩成一个公式。

## 6. 空间分量：相对论力不只是普通力

把 Lorentz boost 的具体形式代进去，并使用 $F^0 = 0$，得到空间分量：[[Explanations/式2.3.5的推导|式2.3.5的推导]]

$$
\boldsymbol{f}
=
\boldsymbol{F}
+
(\gamma - 1)\boldsymbol{v}
\frac{\boldsymbol{v}\cdot\boldsymbol{F}}{v^2}
\tag{2.3.5}
$$

其中：

$$
\gamma = \frac{1}{\sqrt{1-v^2}}
$$

这里采用自然单位 $c=1$。

这个公式很有物理含义。它告诉我们：实验室系中的四维力空间分量 $\boldsymbol{f}$ 不一定等于瞬时静止系中的普通力 $\boldsymbol{F}$。差别来自力在速度方向上的分量。

为了看得更清楚，可以把 $\boldsymbol{F}$ 分解成平行于速度和垂直于速度的部分：

$$
\boldsymbol{F}
=
\boldsymbol{F}_\parallel
+
\boldsymbol{F}_\perp
$$

其中：

$$
\boldsymbol{F}_\parallel
=
\boldsymbol{v}
\frac{\boldsymbol{v}\cdot\boldsymbol{F}}{v^2}
$$

那么式子变成：

$$
\boldsymbol{f}
=
\gamma \boldsymbol{F}_\parallel
+
\boldsymbol{F}_\perp
$$

因为：

$$
\boldsymbol{F}_\parallel
+
(\gamma-1)\boldsymbol{F}_\parallel
=
\gamma \boldsymbol{F}_\parallel
$$

这说明：

- 垂直于运动方向的力分量不被 $\gamma$ 放大；
- 平行于运动方向的力分量会被 $\gamma$ 放大。

直觉上，这是因为 Lorentz boost 主要混合时间方向和运动方向。垂直方向没有被 boost 直接混合，所以形式更简单；平行方向与时间分量混合，因此出现 $\gamma$。这个 boost 的空间部分在 2.1 中已经给出，见 [[Explanations/标准boost空间部分的意义|标准boost空间部分的意义]]。

## 7. 时间分量：功率进入四维力

四维力的时间分量是：[[Explanations/式2.3.6的推导|式2.3.6的推导]]

$$
f^0
=
\gamma \boldsymbol{v}\cdot\boldsymbol{F}
=
\boldsymbol{v}\cdot\boldsymbol{f}
\tag{2.3.6}
$$

这个式子非常值得停下来理解。

在 Newton 力学中，力对粒子做功的功率是：

$$
\frac{dE}{dt}
=
\boldsymbol{F}\cdot\boldsymbol{v}
$$

也就是力在速度方向上的分量才改变能量。垂直于速度的力只改变运动方向，不改变速率，所以不做功。

在相对论中，能量和动量会合并为四维动量。因此，四维力的时间分量自然应该和能量变化有关。这里 $f^0$ 中出现 $\boldsymbol{v}\cdot\boldsymbol{F}$，正是在提示：四维力的时间分量不是额外神秘的东西，它对应力对粒子能量的改变。

这里 Weinberg 还没有正式定义四维动量和能量，那是 2.4 的内容。但 2.3 已经在为 2.4 铺路：一旦你接受 $f^\alpha$ 是四维力，自然会定义四维动量 $p^\alpha = m dx^\alpha/d\tau$，然后 $f^\alpha = dp^\alpha/d\tau$。这就是下一节的逻辑。

## 8. 为什么还要检查归一化条件

既然运动方程是：

$$
f^\alpha
=
m \frac{d^2x^\alpha}{d\tau^2}
$$

那么给定初始位置和初始四维速度，原则上就可以求出 $x^\alpha(\tau)$。但这里有一个限制：$\tau$ 必须真的是固有时，而不是随便选的参数。

[[Concepts/四维速度|四维速度]]定义为：

$$
u^\alpha
=
\frac{dx^\alpha}{d\tau}
$$

因为：

$$
d\tau^2 = dt^2 - d\boldsymbol{x}^2
$$

所以四维速度必须满足归一化条件：

$$
-1
=
\eta_{\alpha\beta}
\frac{dx^\alpha}{d\tau}
\frac{dx^\beta}{d\tau}
\tag{2.3.7}
$$

用 $u^\alpha$ 写就是：

$$
\eta_{\alpha\beta}u^\alpha u^\beta = -1
$$

也就是：

$$
u^\alpha u_\alpha
=
\eta_{\alpha\beta}u^\alpha u^\beta
=
-1
$$

其中 $u^\alpha u_\alpha=\eta_{\alpha\beta}u^\alpha u^\beta$ 是降指标后的 Minkowski 内积记号，见 [[Explanations/四维速度内积记号的含义|四维速度内积记号的含义]]；下指标 $u_\alpha$ 的来源见 [[Concepts/协变矢量与逆变矢量|协变矢量与逆变矢量]]，Minkowski metric 降指标的矩阵展开见 [[Explanations/Minkowski度规下降指标的矩阵展开|Minkowski度规下降指标的矩阵展开]]。

这相当于说：四维速度的 Minkowski norm 固定为 $-1$。这是因为粒子沿 timelike worldline 运动。

现在自然会问：如果一开始满足这个条件，运动方程演化之后会不会破坏它？

Weinberg 说不会。因为对它关于 $\tau$ 求导：

$$
\frac{d}{d\tau}
\left(
\eta_{\alpha\beta}u^\alpha u^\beta
\right)
=
2\eta_{\alpha\beta}
\frac{du^\alpha}{d\tau}
u^\beta
$$

而由 $f^\alpha = m du^\alpha/d\tau$，这等价于要求：[[Explanations/式2.3.8的推导|式2.3.8的推导]]

$$
0
=
2\eta_{\alpha\beta}f^\alpha
\frac{dx^\beta}{d\tau}
\tag{2.3.8}
$$

也就是：

$$
\eta_{\alpha\beta} f^\alpha u^\beta = 0
$$

这句话的几何意义非常漂亮：四维力 $f^\alpha$ 总是与四维速度 $u^\alpha$ Minkowski 正交。[[Explanations/四维力与四维速度正交的含义|四维力与四维速度正交的含义]]

这不是普通欧氏空间里的垂直，而是 Minkowski metric 意义下的正交。

为什么它成立？最简单是在粒子瞬时静止系中看。此时：

$$
u^\alpha = (0,0,0,1)
$$

按照 Weinberg 的指标顺序，空间分量为零，时间分量为一。而在瞬时静止系中：

$$
f^\alpha = (\boldsymbol{F},0)
$$

所以 $f^\alpha$ 只有空间分量，$u^\alpha$ 只有时间分量。二者的 Minkowski 内积显然为零：

$$
\eta_{\alpha\beta} f^\alpha u^\beta = 0
$$

而这个内积是 Lorentz invariant。如果在一个惯性系中为零，那么在所有 Lorentz 相关的惯性系中都为零。

这一步保证了运动方程的自洽性：四维力不会把四维速度推出合法的 timelike 归一化曲面。

## 9. 本节的核心直觉

这一节可以用一句话概括：相对论粒子动力学不是抛弃 Newton 第二定律，而是把它提升为四维、固有时参数化、Lorentz covariant 的形式。

更具体地说，Newton 力学里我们关心：

$$
\boldsymbol{F}
=
m\boldsymbol{a}
$$

相对论里我们关心：

$$
f^\alpha
=
m\frac{d^2x^\alpha}{d\tau^2}
$$

但是这个 $f^\alpha$ 不是随便定义出来的。它必须满足：

- 在粒子瞬时静止系中，空间分量就是普通三维力 $\boldsymbol{F}$；
- 时间分量在静止系中为零；
- 在 Lorentz transformation 下像四维矢量一样变换；
- 与四维速度正交，从而保持 $u^\alpha u_\alpha = -1$。

这四点合起来，就是 relativistic particle dynamics 的基础。

## 10. 常见误区

第一个误区是把 $\boldsymbol{F}$ 和 $\boldsymbol{f}$ 混为一谈。$\boldsymbol{F}$ 是粒子瞬时静止系中的普通三维力，而 $\boldsymbol{f}$ 是四维力的空间分量。二者一般不相等，只有在低速极限或特殊方向上才简单对应。

第二个误区是认为四维力的时间分量 $f^0$ 可有可无。其实 $f^0$ 很重要，它编码能量变化。若 $\boldsymbol{v}\cdot\boldsymbol{F}=0$，力不做功，时间分量为零；若力有沿速度方向的分量，粒子能量改变，$f^0$ 就不为零。

第三个误区是觉得 $f^\alpha u_\alpha=0$ 表示“力不改变运动”。不是这样。它只表示四维力不会改变四维速度的固定 Minkowski norm。粒子的三维速度、能量、动量当然都可以改变。

第四个误区是把 $\tau$ 当作普通时间。$\tau$ 是粒子自己的 proper time。只有在粒子瞬时静止系中，$\tau$ 才等于那个系的坐标时间 $t$。

## 11. 自检问题

1. 为什么相对论动力学更自然地使用 $d/d\tau$，而不是 $d/dt$？
2. 在粒子瞬时静止系中，为什么 $F^0\equiv 0$？
3. 如果 $\boldsymbol{F}\perp \boldsymbol{v}$，那么 $f^0$ 是多少？这说明了什么？
4. 如果 $\boldsymbol{F}\parallel \boldsymbol{v}$，那么 $\boldsymbol{f}$ 和 $\boldsymbol{F}$ 的关系是什么？
5. 为什么只要在瞬时静止系中证明 $f^\alpha u_\alpha=0$，就能推出所有惯性系中也成立？

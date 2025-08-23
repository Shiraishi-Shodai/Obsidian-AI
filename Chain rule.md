---
tags:
  - Back_Propagation
  - DeepLearning
  - Gradient
created:
  - 2025-02-05 12:37
---

# Chain rule

## Feeling Notes
---
- [[Chain rule]]
- -[[What is back propagation]]
## Literature Notes
---
- [[Gradient descent method]]
- [[Back propagation]]
- [[Deep Learning]]
- [[Neural Network]]
## References
---
-  https://free.kikagaku.ai/tutorial/basic_of_deep_learning/learn/neural_network_basic_backward
- https://github.com/oreilly-japan/deep-learning-from-scratch
- https://www.try-it.jp/chapters-7403/sections-7421/lessons-7438/question-2/

## 連鎖律の原理
---
入れ子になった関数である合成関数の微分は、合成関数を構成しているそれぞれの関数の微分をかけることで求められるというルール。この仕組みを利用し、合成関数(**目的関数**)の微分から各重みまでに経由する関数の微分をかけることで各重みの更新量を計算することが出来る。

### 例1 xに関するzの微分を求めよ
---
$z = t^2$
$t = x + y$

## $\frac{\partial z}{\partial x} = \frac{\partial z}{\partial t} \frac{\partial t}{\partial x}$

1. tに関するzの微分を求める
   $z = 2t$
2. xに関するtの微分を求める
    $t = 1$
3. それぞれの関数の微分をかける
   $2t1$
	 $= 2・(x + y)$

### 例2 yに関するzの微分を求めよ
---
$z = t^2$
$t = x + y$

## $\frac{\partial z}{\partial x} = \frac{\partial z}{\partial t} \frac{\partial t}{\partial y}$

1. tに関するzの微分を求める
   $z = 2t$
2. yに関するtの微分を求める
    $t = 1$
3. それぞれの関数の微分をかける
   $2t1$
	 $= 2・(x + y)$

### 例3 xに関するzの微分を求めよ
---
$z = u^2$
$u = 2x + 4$

## $\frac{\partial z}{\partial x} = \frac{\partial z}{\partial u} \frac{\partial u}{\partial x}$

1. uに関するzの微分を求める
   $z = 2u$
2. xに関するuの微分を求める
    $u = 2$
3. それぞれの関数の微分をかける
   $2u ・ 2$
	 $= 2・(2x + 4) ・ 2$
    $= 8x + 16$

## 平均二乗誤差の微分
---
![[Image.jpeg]]
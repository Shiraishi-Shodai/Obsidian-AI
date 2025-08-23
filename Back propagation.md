---
tags:
  - DeepLearning
  - Gradient
  - "#Back_Propagation"
created:
  - 2025-02-05 12:19
---

# Back propagation

## Feeling Notes
---
- [[What is back propagation|What is back propagation]]
## References
---
- https://github.com/oreilly-japan/deep-learning-from-scratch
- https://free.kikagaku.ai/tutorial/basic_of_deep_learning/learn/neural_network_basic_backward

## 誤差逆伝搬法とは
---
重みに関する損失関数の勾配を効率的に計算するための方法。
数値微分と比べて計算スピードが速い
損失関数を各重みで微分することでそれぞれの重みの更新量を計算する

各重みの更新量の計算には[[Chain rule]]という仕組みを使う。
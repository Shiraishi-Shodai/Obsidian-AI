---
tags:
  - Attention
  - QKV
created:
  - 2025-08-24 00:23
---


## References
---
- [[わからないこと]]
- [[QKVって何？]]

# Attentionの基本式
---
この式は、**Scaled Dot-Product Attention（スケールド・ドット積アテンション）** の基本形

$$
Attention(Q,K,V)=softmax(QKTdk)V\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
$$

Q：質問のベクトル
K：質問に対して注意を向ける対象のタグのベクトル
Q：答えのベクトル


## 内積 QKTQK^T
---
質問と注意を向ける対象のタグの類似度を表す


## 計算例
---



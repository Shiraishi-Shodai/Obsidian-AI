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

いいね。まずは**超シンプルな1クエリ×2トークン**の例で手を動かしましょう。

- $Q = [1,,0] \quad (\text{形: } 1\times 2)$
    
- $K_1 = [1,,0],; K_2 = [0,,1] \quad (\text{まとめて } K=\begin{bmatrix}1&0\0&1\end{bmatrix})$
    
- $V_1 = [5,,10],; V_2 = [20,,30] \quad (\text{まとめて } V=\begin{bmatrix}5&10\20&30\end{bmatrix})$
    
- 次元は $d_k = 2$
    

まず最初のステップ：  
**内積スコア $QK^T$** を出します（「各Keyとの類似度」）。

質問（1コだけ）：  
$Q \cdot K_1^T$ と $Q \cdot K_2^T$ の値はいくつになりますか？  
（ヒント: $[1,0]\cdot[1,0]=?$、$[1,0]\cdot[0,1]=?$）

---

👉 これでMarkdownにすると、数式部分はLaTeXとして綺麗に表示されます。

このまま **演算過程まで解いて欲しい**ですか？それともまずは「数式が表示されるように整形」だけで十分ですか？
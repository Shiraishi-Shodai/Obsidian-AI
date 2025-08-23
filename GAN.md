---
tags:
  - "#DeepLearning"
  - "#UnsupervisedLearning"
  - "#GAN"
  - "#GenerativeAI"
created:
  - 2025-02-08 23:26
---

## Feeling Notes
---
-
## Literature Notes
---
- 
## References
---
- [【Deep Learning研修（発展）】データ生成・変換のための機械学習　第２回前編「GAN（基本的なアイデア）」](https://www.youtube.com/watch?v=D6kAKzfQlHk)

# GAN
---
教師なし学習の一種。

## GANの定式化
---
Generatorが作るデータと真のデータとの類似度を最大化して、DiscriminatorがGeneratorが生成したデータを正しく識別する確率を最小化する。

## 構成要素

### 1. Generator：偽のサンプルを出力する
確率分布から確率変数をデータに変換する
U-netというネットワークを活用
### 2. Discriminator: 偽物かどうかを見分ける
Generatorが作ったデータ化か学習データ化を識別する
Discriminatorは予め本物のデータを学習する
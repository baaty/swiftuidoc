---
layout: page
---

### 説明

アフィン変換が適用された形状

### 使い方

    TransformedShape(shape: 図形(Content), transform: アフィン変換行列(CGAffineTransform))

### 例

#### 基本的な使い方

    TransformedShape(shape: Circle(), transform: CGAffineTransform())

### 宣言

    @frozen struct TransformedShape<Content> where Content : Shape

### プロパティ

| 名前             | 型                                   | 説明              |
| -------------- | ----------------------------------- | --------------- |
| animatableData | ScaledShape<Content>.AnimatableData | アニメーションするためのデータ |
| animatableData | EmptyAnimatableData                 | アニメーションするためのデータ |
| shape          | Content                             | 図形              |
| transform      | CGAffineTransform                   | トランスフォーム        |

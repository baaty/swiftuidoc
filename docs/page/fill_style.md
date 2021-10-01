---
layout: page
---

### 説明

ベクトル図形をラスタライズするためのスタイル

### 使い方

    FillStyle(eoFill: 偶数od規則を使用するか(Bool) = false, antialiased: アンチエイリアスを使用するか(Bool) = true)

### 例

#### 基本的な使い方

    FillStyle()

### 宣言

    @frozen struct FillStyle

### プロパティ

| 名前            | 型    | 説明                         |
| ------------- | ---- | -------------------------- |
| isAntialiased | Bool | シェイプのエッジにアンチエイリアスを適用するか    |
| isEOFilled    | Bool | シェイプをレンダリングする際に偶奇ルールを使用するか |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/fillstyle>

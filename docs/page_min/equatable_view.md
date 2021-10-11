---
layout: page
---

### 説明

自分自身を以前の値と比較し新しい値が以前の値と同じであれば子の更新を阻止するビュータイプ

### 使い方

    EquatableView(content: コンテンツ)

### 例

#### 基本的な使い方

    EquatableView(content: hogeView)

### 宣言

    @frozen struct EquatableView&lt;Content&gt; where Content : Equatable, Content : View

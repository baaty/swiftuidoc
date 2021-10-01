---
layout: page
---

### 説明

スクロールビュー

### 使い方

    ScrollView(スクロール可能な軸(Axis.Set) = .vertical, showsIndicators: オフセット表示するか(Bool) = true) {
        コンテンツ(Content)
    }

    ScrollView(スクロール可能な軸(Axis.Set) = .vertical, showsIndicators: オフセット表示するか(Bool) = true, content: コンテンツ)

### 引数の使い方

#### Axis.Set

| 名前                                      | 説明                       |
| --------------------------------------- | ------------------------ |
| .horizontal                             | 縦スクロール                   |
| .vertical                               | 横スクロール                   |
| Axis.Set()                              | 空のオプションセットを作成            |
| Axis.Set(Sequence)                      | アイテムの有限のシーケンスから新しいセットを作成 |
| Axis.Set(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成  |
| Axis.Set(rawValue: Int8)                | 与えられた生の値から新しいオプションセットを作成 |

### 例

#### 基本的な使い方

    ScrollView() {
        Text("スクロールビュー1")
        Text("スクロールビュー2")
    }

#### 横スクロール

    ScrollView(.horizontal) {
        HStack {
            Text("スクロールビュー1")
            Text("スクロールビュー2")
        }
    }

### 宣言

    struct ScrollView<Content> where Content : View

### プロパティ

| 名前              | 型        | 説明                                         |
| --------------- | -------- | ------------------------------------------ |
| content         | Content  | スクロールビューのコンテンツ                             |
| axes            | Axis.Set | スクロールビューのスクロール可能な軸                         |
| showsIndicators | Bool     | コンテンツのスクロール可能なコンポーネントをプラットフォームに適した方法で表示するか |

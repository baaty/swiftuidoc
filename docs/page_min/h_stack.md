---
layout: page
---

### 説明

子ビューを右方向に並べて配置し必要な場合にのみ作成するコンテナビュー  
最大10個まで配置することが可能

### 使い方

    HStack(alignment: 配置(VerticalAlignment) = .center, spacing: 間隔(CGFloat) = nil) {
        コンテンツ(Content)
    }

    HStack(alignment: 配置(VerticalAlignment) = .center, spacing: 間隔(CGFloat) = nil, content: コンテンツ)

### 引数の使い方

#### VerticalAlignment

| 名前                 | 説明  |
| ------------------ | --- |
| .bottom            | 下   |
| .center            | 中   |
| .firstTextBaseline | 先頭の行のベースライン |
| .lastTextBaseline  | 最終の行のベースライン |
| .top               | 上   |

### 例

#### 基本的な使い方

    HStack {
        Text("Hello")
        Divider()
        Text("World")
    }

#### 最大の10個配置10個配置

    HStack {
        Text("ビュー1")
        Text("ビュー2")
        Text("ビュー3")
        Text("ビュー4")
        Text("ビュー5")
        Text("ビュー6")
        Text("ビュー7")
        Text("ビュー8")
        Text("ビュー9")
        Text("ビュー10")
    }

#### VStackの中にHStack

    VStack {
        Text("ビュ-")
        HStack {
            Text("子ビュ-")
        }
    }

#### 右に揃えて配置

    HStack(alignment: .left) {
        Text("右寄りテキスト")
    }

#### ビュー同士の間隔を空ける

    HStack(spacing: 24) {
        Text("ビュー1")
        Text("ビュー2")
    }

### 宣言

    @frozen struct HStack<Content> where Content : View

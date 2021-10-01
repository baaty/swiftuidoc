---
layout: page
---

### 説明

子ビューを下方向に並べて配置し必要な場合にのみ作成するコンテナビュー  
最大10個まで配置することが可能

### 使い方

    VStack(alignment: 配置(HorizontalAlignment) = .center, spacing: 間隔(CGFloat) = nil) {
        コンテンツ(Content)
    }

    VStack(alignment: 配置(HorizontalAlignment) = .center, spacing: 間隔(CGFloat) = nil, content: コンテンツ)

### 引数の使い方

##### HorizontalAlignment

| 名前        | 説明  |
| --------- | --- |
| .center   | 中央 |
| .leading  | 左   |
| .trailing | 右   |

### 例

#### 基本的な使い方

    VStack {
        Text("Hello")
        Divider()
        Text("World")
    }

#### 最大の10個配置10個配置

    VStack {
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

#### VStackの中にVStack

    VStack {
        Text("ビュ-")
        VStack {
            Text("子ビュ-")
        }
    }

#### 右に揃えて配置

    VStack(alignment: .trailing) {
        Text("右寄りテキスト")
    }

#### ビュー同士の間隔を空ける

    VStack(spacing: 24) {
        Text("ビュー1")
        Text("ビュー2")
    }

### 宣言

    @frozen struct VStack<Content> where Content : View

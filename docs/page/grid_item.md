---
layout: page
---

### 説明

1つのグリッドアイテム(行や列など)の説明

### 使い方

    GridItem(サイズ(GridItem.Size) = .flexible(), spacing: 間隔(CGFloat) = nil, alignment: 配置(Alignment) = nil)
        .メソッド

### 引数の使い方

#### GridItem.Size

| 名前                                                             | 説明                          |
| -------------------------------------------------------------- | --------------------------- |
| .adaptive(minimum: CGFloat, maximum: CGFloat = .infinity)      | フレキシブルなアイテムのスペースに複数のアイテムを配置 |
| .fixed(CGFloat)                                                | 指定された固定サイズ                  |
| .flexible(minimum: CGFloat = 10, maximum: CGFloat = .infinity) | フレキシブルなアイテム                 |

#### Alignment

| 名前              | 説明      |
| --------------- | ------- |
| .bottom         | ビューの下   |
| .bottomLeading  | ビューの左下  |
| .bottomTrailing | ビューの右下  |
| .center         | ビューの真ん中 |
| .leading        | ビューの左   |
| .top            | ビューの上   |
| .topLeading     | ビューの左上  |
| .topTrailing    | ビューの右上  |
| .trailing       | ビューの右   |

### 例

#### 基本的な使い方

    GridItem()

### プロパティ

| 名前        | 型             | 説明               |
| --------- | ------------- | ---------------- |
| alignment | Alignment     | 配置する際に使用するアライメント |
| spacing   | CGFloat       | 次の項目までの間隔        |
| size      | GridItem.Size | サイズ              |

### 宣言

    struct GridItem

### 参考サイト

<https://developer.apple.com/documentation/swiftui/griditem>

---
layout: page
---

### 説明

1つのグリッドアイテム(行や列など)の説明

### 使い方

    GridItem(サイズ(GridItem.Size) = .flexible(), spacing: 間隔(CGFloat) = nil, alignment: 配置(Alignment) = nil)

### 引数の使い方

#### GridItem.Size

| 名前                                                             | 説明                          |
| -------------------------------------------------------------- | --------------------------- |
| .adaptive(minimum: CGFloat, maximum: CGFloat = .infinity)      | フレキシブルなアイテムのスペースに複数のアイテムを配置 |
| .fixed(CGFloat)                                                | 指定された固定サイズ                  |
| .flexible(minimum: CGFloat = 10, maximum: CGFloat = .infinity) | フレキシブルなアイテム                 |

#### Alignment

| 名前              | 説明   |
| --------------- | ---- |
| .bottom         | 下寄せ  |
| .bottomLeading  | 左下寄せ |
| .bottomTrailing | 右下寄せ |
| .center         | 中央寄せ |
| .leading        | 左寄せ  |
| .top            | 上寄せ  |
| .topLeading     | 左上寄せ |
| .topTrailing    | 右寄せ上 |
| .trailing       | 右寄せ  |

### 例

#### 基本的な使い方

    GridItem()

### 宣言

    struct GridItem

### プロパティ

| 名前        | 型             | 説明               |
| --------- | ------------- | ---------------- |
| alignment | Alignment     | 配置する際に使用するアライメント |
| spacing   | CGFloat       | 次の項目までの間隔        |
| size      | GridItem.Size | サイズ              |

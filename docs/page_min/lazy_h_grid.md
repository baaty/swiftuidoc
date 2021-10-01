---
layout: page
---

### 説明

右方向に拡大するグリッドに子ビューを配置し必要な場合にのみアイテムを作成するコンテナビュー

### 使い方

    LazyHGrid(rows: グリッドアイテムの配列([GridItem]), alignment: 配置(VerticalAlignment) = .center, spacing: 間隔(CGFloat) = nil, pinnedViews: {
        固定するビュー(PinnedScrollableViews)
    }) {
        コンテンツ(Content)
    }

    LazyHGrid(rows: グリッドアイテムの配列([GridItem]), alignment: 配置(VerticalAlignment) = .center, spacing: 間隔(CGFloat) = nil, pinnedViews: 固定するビュー(PinnedScrollableViews) = .init(), content: コンテンツ)

### 引数の使い方

#### GridItem

| 名前                                                                                                                                   | 説明                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | --------------------------- |
| GridItem(.adaptive(minimum: CGFloat, maximum: CGFloat = .infinity), spacing: 間隔(CGFloat) = nil, alignment: 配置(Alignment) = nil)      | フレキシブルなアイテムのスペースに複数のアイテムを配置 |
| GridItem(.fixed(CGFloat), spacing: 間隔(CGFloat) = nil, alignment: 配置(Alignment) = nil)                                                | 指定された固定サイズ                  |
| GridItem(.flexible(minimum: CGFloat = 10, maximum: CGFloat = .infinity), spacing: 間隔(CGFloat) = nil, alignment: 配置(Alignment) = nil) | フレキシブルなアイテム                 |

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

#### PinnedScrollableViews

| 名前                                                   | 説明                       |
| ---------------------------------------------------- | ------------------------ |
| .sectionFooters                                      | 各セクションのフッター表示が固定         |
| .sectionHeaders                                      | 各セクションのヘッダー表示が固定         |
| PinnedScrollableViews()                              | 空のオプションセットを作成            |
| PinnedScrollableViews(S)                             | アイテムの有限のシーケンスから新しいセットを作成 |
| PinnedScrollableViews(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成  |
| PinnedScrollableViews(rawValue: UInt32)              | 与えられた生の値から新しいオプションセットを作成 |

### 例

#### 基本的な使い方

    let gridItem = [GridItem()]
    LazyHGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### グリッド同士の間隔を指定

    let gridItem = [GridItem()]
    LazyHGrid(rows: gridItem, spacing: 12) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### グリッドを右寄せ

    let gridItem = [GridItem(alignment: .trailing)]
    LazyHGrid(rows: gridItem, spacing: 12) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### 固定したグリッドを指定

    let gridItem = [GridItem()]
    LazyHGrid(rows: gridItem, pinnedViews: [.sectionHeaders]) {
        Section(header: {}) {
            Text("グリッド1")
            Text("グリッド2")
            Text("グリッド3")
        }
    }

#### 複数行グリッド

    let gridItem = [GridItem(), GridItem()]
    LazyHGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### グリッドの固定サイズを指定

    let gridItem = [GridItem(.fixed(12))]
    LazyHGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### フレキシブルなグリッドに複数のアイテムを配置

    let gridItem = [GridItem(.adaptive(minimum: 12, maximum: 12))]
    LazyHGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### フレキシブルなグリッド

    let gridItem = [GridItem(.flexible(minimum: 12, maximum: 12))]
    LazyHGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

### 宣言

    struct LazyHGrid<Content> where Content : View

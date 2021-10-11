---
layout: page
---

### 説明

下方向に拡大するグリッドに子ビューを配置し必要な場合にのみアイテムを作成するコンテナビュー

### 使い方

    LazyVGrid(columns: グリッドアイテムの配列([GridItem]), alignment: 配置(HorizontalAlignment) = .center, spacing: 間隔(CGFloat) = nil, pinnedViews: {
        固定するビュー(PinnedScrollableViews)
    }) {
        コンテンツ(Content)
    }

    LazyVGrid(columns: グリッドアイテムの配列([GridItem]), alignment: 配置(HorizontalAlignment) = .center, spacing: 間隔(CGFloat) = nil, pinnedViews: 固定するビュー(PinnedScrollableViews) = .init(), content: コンテンツ)

### 例

#### 基本的な使い方

    let gridItem = [GridItem()]
    LazyVGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### グリッド同士の間隔を指定

    let gridItem = [GridItem()]
    LazyVGrid(rows: gridItem, spacing: 12) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### グリッドを右寄せ

    let gridItem = [GridItem(alignment: .trailing)]
    LazyVGrid(rows: gridItem, spacing: 12) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### 固定したグリッドを指定

    let gridItem = [GridItem()]
    LazyVGrid(rows: gridItem, pinnedViews: [.sectionHeaders]) {
        Section(header: {}) {
            Text("グリッド1")
            Text("グリッド2")
            Text("グリッド3")
        }
    }

#### 複数行グリッド

    let gridItem = [GridItem(), GridItem()]
    LazyVGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### グリッドの固定サイズを指定

    let gridItem = [GridItem(.fixed(12))]
    LazyVGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### フレキシブルなグリッドに複数のアイテムを配置

    let gridItem = [GridItem(.adaptive(minimum: 12, maximum: 12))]
    LazyVGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

#### フレキシブルなグリッド

    let gridItem = [GridItem(.flexible(minimum: 12, maximum: 12))]
    LazyVGrid(rows: gridItem) {
        Text("グリッド1")
        Text("グリッド2")
        Text("グリッド3")
    }

### 宣言

    struct LazyVGrid&lt;Content&gt; where Content : View

---
layout: page
---

### 説明

子ビューを下方向に並べて配置し必要な場合にのみ作成するコンテナビュー  
VStackとの違いは画面外にある子ビューは作成されないこと

### 使い方

    LazyVStack(alignment: 配置(HorizontalAlignment) = .center, spacing: 間隔(CGFloat) = nil, pinnedViews: {
        ピン留めされる子ビュー(PinnedScrollableViews)
    }) {
        コンテンツ(Content)
    }

    LazyVStack(alignment: 配置(HorizontalAlignment) = .center, spacing: 間隔(CGFloat) = nil, pinnedViews: ピン留めされる子ビュー(PinnedScrollableViews) = .init(), content: コンテンツ)

### 引数の使い方

#### HorizontalAlignment

| 名前        | 説明  |
| --------- | --- |
| .center   | 中央  |
| .leading  | 左   |
| .trailing | 右   |

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

    LazyVStack {
        ForEach(1...100, id: \.self) {
            Text("Row \($0)")
        }
    }

#### ScrollViewと使う

    ScrollView() {
        LazyVStack {
            ForEach(1...100, id: \.self) {
                Text("Row \($0)")
            }
        }
    }

#### 右に揃えて配置

    LazyVStack(alignment: .right) {
        ForEach(1...100, id: \.self) {
            Text("Row \($0)")
        }
    }

#### ビュー同士の間隔を空ける

    LazyVStack(spacing: 20) {
        ForEach(1...100, id: \.self) {
            Text("Row \($0)")
        }
    }

#### ピン留めされる子ビューあり

    LazyVStack(pinnedViews: [.sectionHeaders]) {
        Section(header: {
            Text("固定されたメッセージ")
        }) {
            ForEach(1...100, id: \.self) {
                Text("Row \($0)")
            }
        }
    }

### 宣言

    struct LazyVStack<Content> where Content : View

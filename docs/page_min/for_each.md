---
layout: page
---

### 説明

ビューを繰り返し定義するコントローラ

### 使い方

#### 与えられた定数の範囲でオンデマンドでビューを計算するインスタンスを作成

    ForEach(範囲(Range<Int>)) {
        コンテンツ(View)
    }

    ForEach(範囲(Range<Int>), content: コンテンツ)

#### 基礎となるデータのアイデンティティに基づいてアップデート全体を一意に識別しビューを作成するインスタンスを作成

    ForEach(データ(Data)) {
        コンテンツ(View)
    }

    ForEach(データ(Data), content: コンテンツ)

#### 基礎となるデータの識別子へのキーパスに基づいて更新全体を一意に識別してビューを作成するインスタンスを作成

    ForEach(データ(Data), id: 識別子へのキーパス(KeyPath<Data.Element, ID>)) {
        コンテンツ(View)
    }

    ForEach(データ(Data), id: 識別子へのキーパス(KeyPath<Data.Element, ID>), content: コンテンツ)

### 例

#### 基本的な使い方

    private struct NamedFont: Identifiable {
        let name: String
        let font: Font
        var id: String { name }
    }
    private let namedFonts: [NamedFont] = [
        NamedFont(name: "Large Title", font: .largeTitle),
        NamedFont(name: "Title", font: .title),
        NamedFont(name: "Headline", font: .headline),
        NamedFont(name: "Body", font: .body),
        NamedFont(name: "Caption", font: .caption)
    ]
    var body: some View {
        ForEach(namedFonts) { namedFont in
            Text(namedFont.name)
                .font(namedFont.font)
        }
    }

### 宣言

    struct ForEach<Data, ID, Content> where Data : RandomAccessCollection, ID : Hashable

### プロパティ

| 名前      | 型                         | 説明                 |
| ------- | ------------------------- | ------------------ |
| content | (Data.Element) -> Content | 必要に応じてコンテンツを作成する機能 |
| data    | Data                      | 基礎となる識別データのコレクション  |

### メソッド

| 名前       | 説明                  |
| -------- | ------------------- |
| onDelete | 削除された時に実行するアクションを設定 |
| onInsert | 挿入された時に実行するアクションを設定 |
| onMove   | 移動された時に実行するアクションを設定 |

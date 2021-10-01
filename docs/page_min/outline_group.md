---
layout: page
---

### 説明

階層的なデータから必要に応じてビューを表示

### 使い方

#### ルートデータ要素とその子へのキーパスからアウトライングループを作成

    OutlineGroup(識別データのコレクションのルート(DataElement), children: 子を示すプロパティへのキーパス(KeyPath<DataElement, Data?>)) {
        コンテンツ
    }

    OutlineGroup(識別データのコレクションのルート(DataElement), children: 子を示すプロパティへのキーパス(KeyPath<DataElement, Data?>), content: コンテンツ)

#### ルートデータ要素のコレクションとその子へのキーパスからアウトライングループを作成

    OutlineGroup(識別されたデータ(Data), children: 子を示すプロパティへのキーパス(KeyPath<DataElement, Data?>)) {
        コンテンツ
    }

    OutlineGroup(識別されたデータ(Data), children: 子を示すプロパティへのキーパス(KeyPath<DataElement, Data?>), content: コンテンツ)

#### ルートデータ要素やその識別子へのキーパスおよびその子へのキーパスからアウトライングループを作成

    OutlineGroup(識別データのコレクションのルート(DataElement), id: 識別子へのキーパス(KeyPath<DataElement, ID>), children: 子を示すプロパティへのキーパス(KeyPath<DataElement, Data?>), content: コンテンツ)

    OutlineGroup(識別データのコレクションのルート(DataElement), id: 識別子へのキーパス(KeyPath<DataElement, ID>), children: 子を示すプロパティへのキーパス(KeyPath<DataElement, Data?>)) {
        コンテンツ
    }

#### ルートデータ要素やデータ要素の識別子へのキーパス子要素へのキーパスのコレクションからアウトライングループを作成

    OutlineGroup(識別されたデータ(Data), id: 識別子へのキーパス(KeyPath<DataElement, ID>), children: 子を示すプロパティへのキーパス(KeyPath<DataElement, Data?>)) {
        コンテンツ
    }

    OutlineGroup(識別されたデータ(Data), id: 識別子へのキーパス(KeyPath<DataElement, ID>), children: 子を示すプロパティへのキーパス(KeyPath<DataElement, Data?>), content: コンテンツ

### 例

#### 基本的な使い方

    struct FileItem: Identifiable {
        var id = UUID()
        var name = ""
        var children: [FileItem]? = nil
    }
    struct ContentView: View {
        let data = FileItem(name: "親", children: [FileItem(name: "子")])
        var body: some View {
            OutlineGroup(data, children: \.children) { item in
                Text("\(item.name)")
            }
        }
    }

### 宣言

    struct OutlineGroup<Data, ID, Parent, Leaf, Subgroup> where Data : RandomAccessCollection, ID : Hashable

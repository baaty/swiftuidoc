---
layout: page
---

### 説明

リスト

### 使い方

#### 指定された内容のリストを作成

    List {
        コンテンツ(Content)
    }

    List(content: コンテンツ)

#### 指定された内容のリストを作成し1行の選択

    List(selection: 選択された行(Binding<SelectionValue?>)?) {
        コンテンツ(Content)
    }

    List(selection: 選択された行(Binding<SelectionValue?>)?, content: コンテンツ)

#### 複数行の選択をサポートするリストを指定された内容で作成

    List(selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?) {
        コンテンツ(Content)
    }

    List(selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?, content: コンテンツ)

#### 一定の範囲で必要に応じてビューを計算するリストを作成

    List(範囲(Range<Int>), rowContent: 1行分のビューを作成するビュー)

    List(範囲(Range<Int>)) {
        1行分のビューを作成するビュー(View)
    }

#### 一定の範囲で必要に応じてビューを計算するリストを作成しオプションでユーザーが1つの行を選択

    List(範囲(Range<Int>), selection: 選択された行(Binding<SelectionValue?>)?) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), selection: 選択された行(Binding<SelectionValue?>)?, rowContent: 1行分のビューを作成するビュー)

#### 一定の範囲で必要に応じてビューを計算するリストを作成しオプションでユーザーが複数の行を選択

    List(範囲(Range<Int>), selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?, rowContent: 1行分のビューを作成するビュー)

#### 基礎となるデータの識別子へのキーパスに基づいて行を識別するリストを作成

    List(範囲(Range<Int>), id: 識別子のキーパス(KeyPath<Data.Element, ID>)) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), id: 識別子のキーパス(KeyPath<Data.Element, ID>), rowContent: 1行分のビューを作成するビュー)

#### 識別可能なデータの基礎となるコレクションから必要に応じて行を計算するリストを作成

    List(範囲(Range<Int>)) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), rowContent: 1行分のビューを作成するビュー)

#### 識別可能なデータの基礎となるコレクションから必要に応じて行を計算する階層型リストを作成

    List(範囲(Range<Int>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>)) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), rowContent: 1行分のビューを作成するビュー)

#### 基になるデータの識別子へのキーパスに基づいて行を識別する階層型リストを作成

    List(範囲(Range<Int>), id: 識別子のキーパス(KeyPath<Data.Element, ID>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>)) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), id: 識別子のキーパス(KeyPath<Data.Element, ID>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), rowContent: 1行分のビューを作成するビュー)

#### 識別可能なデータの基礎となるコレクションから必要に応じて行を計算するリストを作成しオプションでユーザーが1つの行を選択

    List(範囲(Range<Int>), selection: 選択された行(Binding<SelectionValue?>)?) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), selection: 選択された行(Binding<SelectionValue?>)?, rowContent: 1行分のビューを作成するビュー)

#### 識別可能なデータの基礎となるコレクションから必要に応じて行を計算するリストを作成しオプションでユーザーが複数の行を選択

    List(範囲(Range<Int>), selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?, rowContent: 1行分のビューを作成するビュー)

#### 識別可能なデータの集合体から必要に応じて行を計算する階層型リストを作成しオプションでユーザーが単一の行を選択

    List(範囲(Range<Int>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), selection: 選択された行(Binding<SelectionValue?>)?) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), selection: 選択された行(Binding<SelectionValue?>)?, rowContent: 1行分のビューを作成するビュー)

#### 基になるデータの識別子へのキーパスに基づいて行を識別する階層型リストを作成しオプションでユーザーが単一の行を選択

    List(範囲(Range<Int>), id: 識別子のキーパス(KeyPath<Data.Element, ID>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), selection: 選択された行(Binding<SelectionValue?>)?) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), id: 識別子のキーパス(KeyPath<Data.Element, ID>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), selection: 選択された行(Binding<SelectionValue?>)?, rowContent: 1行分のビューを作成するビュー)

#### 識別可能なデータのコレクションから必要に応じて行を計算する階層型リストを作成

    List(範囲(Range<Int>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?, rowContent: 1行分のビューを作成するビュー)

#### データの識別子へのキーパスに基づいて行を識別する階層型リストを作成しオプションでユーザーが複数の行を選択

    List(範囲(Range<Int>), id: 識別子のキーパス(KeyPath<Data.Element, ID>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?) {
        1行分のビューを作成するビュー(View)
    }

    List(範囲(Range<Int>), id: 識別子のキーパス(KeyPath<Data.Element, ID>), children: 子を示すプロパティへのキーパス(KeyPath<Data.Element, Data?>), selection: 選択された行を識別するためのSet(Binding<Set<SelectionValue>>)?, rowContent: 1行分のビューを作成するビュー) 

### 例

#### 基本的な使い方

    List {
        Text("リストのテキスト1")
        Text("リストのテキスト2")
        Text("リストのテキスト3")
    }

#### idを指定

    var array = ["1", "2", "3",]
    var body: some View {
        List(array, id: \.self) { s in
            Text(s)
        }
    }

#### ヘッダーとフッターを設定

    List {
        Section(header: Text("ヘッダー"), footer: Text("フッター")) {
            Text("リストのテキスト")
        }
    }

#### スタイルを設定

    List {
        Text("リストのテキスト")
    }
        .listStyle(.bordered)

#### リストから削除

    @State var data = ["1", "2", "3"]
    var body: some View {
        List {
            Section(header: Text("リスト").padding()) {
                ForEach(data, id: \.self) { i in
                    Text(i)
                }
                    .onDelete(perform: delete)
            }
        }
    }
    func delete(i: IndexSet) {
        if let first = i.first {
            data.remove(at: first)
        }
    }

#### リストから移動

    @State var data = ["1", "2", "3"]
    var body: some View {
        List {
            Section(header: Text("リスト").padding()) {
                ForEach(data, id: \.self) { i in
                    Text(i)
                }
                    .onMove(perform: move)
            }
        }
    }
    func move(i: IndexSet, i2: Int) {
        if let first = i.first {
            data.insert(data.remove(at: first), at: i2)
        }
    }

#### 選択リスト

    @State private var data = ["1", "2", "3"]
    @State private var selection: String?
    var body: some View {
        VStack {
            List(data, id: \.self, selection: $selection) { i in
                Text(i)
            }
            EditButton()
        }
    }

#### 複数選択リスト

    @State private var data = ["1", "2", "3"]
    @State private var selection: Set<String>?
    var body: some View {
        VStack {
            List(data, id: \.self, selection: $selection) { i in
                Text(i)
            }
            EditButton()
        }
    }

### 宣言

    struct List<SelectionValue, Content> where SelectionValue : Hashable, Content : View

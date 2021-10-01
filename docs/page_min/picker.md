---
layout: page
---

### 説明

複数の選択肢から1つの値を選択するためのコントロール

### 使い方

#### カスタムラベルを表示するピッカーを作成

    Picker(selection: $現在選択されているオプションを決定するプロパティ(Binding<SelectionValue>), label: ラベル(Label)) {
        表示内容(Content)
    }

    Picker(selection: $現在選択されているオプションを決定するプロパティ(Binding<SelectionValue>), label: ラベル(Label), content: 表示内容)

#### ローカライズされた文字列キーからラベルを生成するピッカーを作成

    Picker(ローカライズされた文字列キー(LocalizedStringKey), selection: $現在選択されているオプションを決定するプロパティ(Binding<SelectionValue>)) {
        表示内容(Content)
    }

    Picker(ローカライズされた文字列キー(LocalizedStringKey), selection: $現在選択されているオプションを決定するプロパティ(Binding<SelectionValue>), content: 表示内容)

#### 文字列からラベルを生成するピッカーを作成

    Picker(現在選択されているオプション(StringProtocol), selection: $現在選択されているオプションを決定するプロパティ(Binding<SelectionValue>)) {
        表示内容(Content)
    }

    Picker(現在選択されているオプション(StringProtocol), selection: $現在選択されているオプションを決定するプロパティ(Binding<SelectionValue>), content: 表示内容)

### 例

#### 基本的な使い方

    @State private var selection = "hoge"
    var body: some View {
        Picker("ピッカー名", selection: $selection) {
            Text("hoge")
            Text("fuga")
        }
    }

#### tagで識別

    @State private var selection = 1
    var body: some View {
        Picker("ピッカー名", selection: $selection) {
            Text("hoge").tag(0)
            Text("fuga").tag(1)
        }
    }

#### 要素に画像

    @State private var selection = "hoge"
    var body: some View {
        Picker("ピッカー名", selection: $selection) {
            Text("hoge")
            Text("fuga")
        }
    }

### 宣言

    struct Picker<Label, SelectionValue, Content> where Label : View, SelectionValue : Hashable, Content : View

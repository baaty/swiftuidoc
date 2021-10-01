---
layout: page
---

### 説明

ナビゲーションの表示を制御するビュー

### 使い方

#### デスティネーションビューを表示するナビゲーションリンクを作成

    NavigationLink(destination: 遷移先ビュー(Destination)) {
        トリガーとなるビュー(Label)
    }

    NavigationLink(destination: 遷移先ビュー(Destination), label: トリガーとなるビュー)

#### WatchKitストーリーボードのビューを表示するナビゲーションリンクを作成

    NavigationLink(destinationName: "ストーリーボード名") {
        トリガーとなるビュー(Label)
    }

    NavigationLink(destinationName: "ストーリーボード名", label: トリガーとなるビュー)

#### ローカライズされた文字列キーからリンクが生成するテキストラベルを持つ目的地のビューを提示するナビゲーションリンクを作成

    NavigationLink(ローカライズされた文字列キー(LocalizedStringKey), destination: 遷移先ビュー(Destination))

#### タイトル文字列から生成されるテキストラベルを持つ目的地のビューを表示するナビゲーションリンクを作成

    NavigationLink(タイトル(StringProtocol), destination: 遷移先ビュー(Destination))

#### アクティブ時に目的地のビューを表示するナビゲーションリンクを作成

    NavigationLink(destination: 遷移先ビュー(Destination), isActive: デスティネーションが現在表示されているかどうか(Binding<Bool>)) {
        トリガーとなるビュー(Label)
    }

    NavigationLink(destination: 遷移先ビュー(Destination), isActive: デスティネーションが現在表示されているかどうか(Binding<Bool>), label: トリガーとなるビュー)

#### WatchKitストーリーボードのビューをアクティブに表示するナビゲーションリンクを作成

    NavigationLink(destinationName: "ストーリーボード名", isActive: デスティネーションが現在表示されているかどうか(Binding<Bool>)) {
        トリガーとなるビュー(Label)
    }

    NavigationLink(destinationName: "ストーリーボード名", isActive: デスティネーションが現在表示されているかどうか(Binding<Bool>), label: トリガーとなるビュー)

#### アクティブなときにデスティネーションビューを表示するナビゲーションリンクを作成しリンクがタイトル文字列から生成するテキストラベルを付与

    NavigationLink(タイトル(StringProtocol), destination: 遷移先ビュー(Destination), isActive: デスティネーションが現在表示されているかどうか(Binding<Bool>))

#### ローカライズされた文字列キーからリンクが生成するテキストラベルを持つアクティブ時に目的地ビューを提示するナビゲーションリンクを作成

    NavigationLink(ローカライズされた文字列キー(LocalizedStringKey), destination: 遷移先ビュー(Destination), isActive: デスティネーションが現在表示されているかどうか(Binding<Bool>))

#### バインドされた選択変数が指定されたタグの値と一致したときに移動先のビューを表示するナビゲーションリンクを作成

    NavigationLink(destination: 遷移先ビュー(Destination), tag: タグ(Hashable), selection: 選択肢(Binding<Hashable?>)) {
        トリガーとなるビュー(Label)
    }

    NavigationLink(destination: 遷移先ビュー(Destination), tag: タグ(Hashable), selection: 選択肢(Binding<Hashable?>), label: トリガーとなるビュー)

#### バインドされた選択変数が指定した値と一致したときにWatchKitストーリーボードのビューを表示するナビゲーションリンクを作成

    NavigationLink(ローカライズされた文字列キー(LocalizedStringKey), destination: 遷移先ビュー(Destination), tag: タグ(Hashable), selection: 選択肢(Binding<Hashable?>))

#### バインドされた選択変数が指定された値と一致したときにリンクがローカライズされた文字列キーから生成するテキストラベルを使って目的のビューを表示するナビゲーションリンクを作成

    NavigationLink(タイトル(StringProtocol), destination: 遷移先ビュー(Destination), tag: タグ(Hashable), selection: 選択肢(Binding<Hashable?>))

### 例

#### 基本的な使い方

    struct SubView: View {
        var body: some View {
            Text("サブビュー")
        }
    }
    struct ContentView: View {
        var body: some View {
            NavigationView {
                NavigationLink("サブビューへ", destination: SubView())
            }
        }
    }

#### リンクをカスタマイズ

    NavigationLink(destination: SubView()) {
        HStack {
            Text("カスタマイズするリンク")
            Spacer()
            Image(systemName: "paperplane")
        }
            .padding()
    }

### 宣言

    struct NavigationLink<Label, Destination> where Label : View, Destination : View

### メソッド

| 名前           | 説明            |
| ------------ | ------------- |
| isDetailLink | リンク先を詳細ビューで表示 |

---
layout: page
---

### 説明

展開したり折りたたんだりするビュー  
メニューなどでよく使われるやつ

### 使い方

#### ディスクロージャーグループを作成し指定された文字列を使ってラベルのテキストビューを作成

    DisclosureGroup(タイトル(StringProtocol), content: 展開したときに表示される内容)

    DisclosureGroup(タイトル(StringProtocol)) {
        展開したときに表示される内容
    }

#### ローカライズされた文字列キーを使用してラベルのテキスト・ビューを作成し開示グループを作成

    DisclosureGroup(タイトルのローカライズキー(LocalizedStringKey), content: 展開したときに表示される内容)

    DisclosureGroup(タイトルのローカライズキー(LocalizedStringKey)) {
        展開したときに表示される内容
    }

#### ローカライズされた文字列キーを使用してラベルのテキストビューを作成し拡張状態（展開または折りたたまれた状態）へのバインディングを使用して開示グループを作成

    DisclosureGroup(タイトルのローカライズキー(LocalizedStringKey), isExpanded: $状態(Binding<Bool>)) {
        展開したときに表示される内容
    }

    DisclosureGroup(タイトルのローカライズキー(LocalizedStringKey), isExpanded: $状態(Binding<Bool>), content: 展開したときに表示される内容)

#### 提供された文字列を使用してラベルのテキストビューを作成し展開状態（展開または折りたたまれた状態）へのバインディングを使用して開示グループを作成

    DisclosureGroup(タイトル(StringProtocol), isExpanded: $状態(Binding<Bool>)) {
        展開したときに表示される内容
    }

    DisclosureGroup(タイトル(StringProtocol), isExpanded: $状態(Binding<Bool>), content: 展開したときに表示される内容)

#### 指定されたラベルとコンテンツビューを持つ開示グループを作成

    DisclosureGroup(content: {
        展開したときに表示される内容
    }) {
        内容を説明するビュー
    }

    DisclosureGroup(content: 展開したときに表示される内容, label: 内容を説明するビュー)

#### 与えられたラベルとコンテンツビューおよび展開状態（展開または折りたたまれた状態）へのバインディングを持つ開示グループを作成

    DisclosureGroup(isExpanded: $状態(Binding<Bool>), content: {
        展開したときに表示される内容
    }) {
        内容を説明するビュー
    }

    DisclosureGroup(isExpanded: $状態(Binding<Bool>), content: 展開したときに表示される内容, label: 内容を説明するビュー)

### 例

#### 基本的な使い方

    @State private var topExpanded = true
    var body: some View {
        DisclosureGroup(isExpanded: $topExpanded) {
            Text("展開したときに表示されるテキスト")
        }
    }

#### ラベルをカスタマイズ

    @State private var topExpanded = true
    var body: some View {
        DisclosureGroup("展開", isExpanded: $topExpanded, content: {
            Text("展開したときに表示されるテキスト")
        }) {
            HStack {
                Image(systemName: "line.horizontal.3")
                Text("メニュー")
            }
        }
    }

### 宣言

    struct DisclosureGroup<Label, Content> where Label : View, Content : View

---
layout: page
---

### 説明

文字を入力するためのテキストインターフェイスを表示

### 使い方

#### タイトル文字列から生成されたテキストラベルを持つテキストフィールドを作成

    TextField("プレースホルダ用メッセージ(StringProtocol)", text: $表示・編集するテキスト(Binding<String>)) { _ in
        編集した時に実行するアクション(Void)
    } onCommit: {
        テキストフィールドにフォーカスがある時に実行するアクション(Void)
    }

    TextField("プレースホルダ用メッセージ(StringProtocol)", text: $表示・編集するテキスト(Binding<String>), onEditingChanged: 編集した時に実行するアクション, onCommit: テキストフィールドにフォーカスがある時に実行するアクション)

#### ローカライズされたタイトル文字列から生成されたテキストラベルを持つテキストフィールドを作成

    TextField(ローカライズされた文字列キー(LocalizedStringKey), text: $表示・編集するテキスト(Binding<String>)) { _ in
        編集した時に実行するアクション(Void)
    } onCommit: {
        テキストフィールドにフォーカスがある時に実行するアクション(Void)
    }

    TextField(ローカライズされた文字列キー(LocalizedStringKey), text: $表示・編集するテキスト(Binding<String>), onEditingChanged: 編集した時に実行するアクション, onCommit: テキストフィールドにフォーカスがある時に実行するアクション)

### 例

#### 基本的な使い方

    @State private var username: String = ""
    var body: some View {
        TextField("ユーザネーム", text: $username)
    }

#### キーボードを変更

    @State private var phone: String = ""
    var body: some View {
        TextField("電話番号", text: $phone)
            .keyboardType(.phonePad)
    }

#### 変更不可

    @State private var username: String = ""
    var body: some View {
        TextField("ユーザネーム", text: $username)
            .disabled(true)
    }

### 宣言

    struct TextField<Label> where Label : View

---
layout: page
---

### 説明

プライベートテキストを安全に入力するためのコントロールで入力した内容がマスクして表示  
パスワードを入力するときに使われることが多い

### 使い方

    SecureField(ローカライズされた文字列キー(LocalizedStringKey), text: $表示・編集するテキスト(Binding<String>)) {
        セキュアフィールドにフォーカスがある時に実行するアクション(Void)
    }

    SecureField(ローカライズされた文字列キー(LocalizedStringKey), text: $表示・編集するテキスト(Binding<String>), onCommit: セキュアフィールドにフォーカスがある時に実行するアクション)

    SecureField("プレースホルダ用メッセージ(StringProtocol)", text: $表示・編集するテキスト(Binding<String>)) {
         セキュアフィールドにフォーカスがある時に実行するアクション(Void)
    }

    SecureField("プレースホルダ用メッセージ(StringProtocol)", text: $表示・編集するテキスト(Binding<String>), onCommit: セキュアフィールドにフォーカスがある時に実行するアクション)

### 例

#### 基本的な使い方

    @State private var password = ""
    var body: some View {
        SecureField("パスワード", text: $password)
    }

### 宣言

    struct SecureField<Label> where Label : View

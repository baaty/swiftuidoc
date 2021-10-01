---
layout: page
---

### 説明

アクションのメニューを表示するためのコントロール  
メニュー項目は最大で10個

### 使い方

#### 文字列からラベルを生成するメニューを作成

    Menu(メニューの内容を表す文字列(StringProtocol)) {
        メニュー項目のグループ(Content)
    }

    Menu(メニューの内容を表す文字列(StringProtocol), content: メニュー項目のグループ)

#### ローカライズされた文字列キーからラベルを生成するメニューを作成

    Menu(ローカライズされた文字列キー(LocalizedStringKey)) {
        メニュー項目のグループ(Content)
    }

    Menu(ローカライズされた文字列キー(LocalizedStringKey), content: メニュー項目のグループ)

#### カスタムラベル付きのメニューを作成

    Menu(content: メニュー項目のグループ, label: メニューの内容を説明するビュー)

### 例

#### 基本的な使い方

    Menu("メニュー") {
        Button("メニュー項目", action: {
            // 実行するアクション
        })
    }

#### メニューをカスタマイズ

    Menu(content: {
        Button("メニュー項目", action: {
            // 実行するアクション
        })
    }) {
        Image(systemName: "doc.text")
        Text("メニュー")
    }

#### メニュー項目をカスタマイズ

    Menu("メニュー") {
        Button(action: {
            // 実行するアクション
        }) {
            Image(systemName: "doc.text")
            Text("メニュー項目")
        }
    }

#### メニューにサブメニュー

    Menu("メニュー") {
        Menu("サブメニュー") {
            Button("サブメニュー項目", action: {
                // 実行するアクション
            })
        }
    }

#### メニュー項目が10個以上ある場合

    Menu("10個以上あるメニュー") {
        Button("メニュー項目1", action: {})
        Button("メニュー項目2", action: {})
        Button("メニュー項目3", action: {})
        Button("メニュー項目4", action: {})
        Button("メニュー項目5", action: {})
        Button("メニュー項目6", action: {})
        Button("メニュー項目7", action: {})
        Button("メニュー項目8", action: {})
        Button("メニュー項目9", action: {})
        Menu("サブメニュー") {
            Button("メニュー項目10", action: {})
            Button("メニュー項目11", action: {})
        }
    }

### 宣言

    struct Menu<Label, Content> where Label : View, Content : View

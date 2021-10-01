---
layout: page
---

### 説明

ボタンを押したときにアクションを実行するコントロール

### 使い方

#### カスタムラベルを表示するボタンを作成

    Button(action: 実行内容) {
        表示内容
    }

    Button(action: 実行内容, label: 表示内容)

#### 文字列からラベルを生成するボタンを作成

    Button("ボタン名(StringProtocol)") {
        実行内容
    }

    Button("ボタン名(StringProtocol)", action: 実行内容)

#### ローカライズされた文字列キーからラベルを生成するボタンを作成

    Button(ローカライズされた文字列キー(LocalizedStringKey)) {
        実行内容
    }

    Button(ローカライズされた文字列キー(LocalizedStringKey), action: 実行内容)

#### カスタムアピアランスとカスタムインタラクションビヘイビアを持つスタイルの構成に基づいてボタンを作成

    Button(スタイル(PrimitiveButtonStyleConfiguration))

### 例

#### テキストのみのボタン

    Button("ボタンのテキスト") {
        // 実行内容
    }

#### ボタンを作成

    Button(action: {
        // 実行内容
    }) {
        Text("ボタンの名前")
    }

#### ボタンに画像

    Button(action: {
        // 実行内容
    }) {
        Image("hoge")
            .renderingMode(.original)
    }

#### 背景を設定

    Button(action: {
        // 実行内容
    }) {
        Text("ボタンの名前")
            .background(Color.yellow)
    }

#### paddingを設定

    Button(action: {
        // 実行内容
    }) {
        Text("ボタンの名前")
            .padding()
    }

#### ボタンにアイコンを表示

    Button(action: {
        // 実行内容
    }) {
        HStack {
            Button(systemName: "rectangle.grid")
            Text("画像")
        }
    }

#### 角が丸いボタン

    Button(action: {
        // 実行内容
    }) {
        VStack {
            Text("ボタンの名前")
        }
            .background(Color.yellow)
            .cornerRadius(12)

    }

#### 円型のボタン

    Button(action: {
        // 実行内容
    }) {
        VStack {
            Button(systemName: "rectangle.grid")
            Text("画像")
        }
            .background(Color.yellow)
            .mask(Circle())

    }

#### ボタンに縁

    Button(action: {
        // 実行内容
    }) {
        VStack {
            Button(systemName: "rectangle.grid")
            Text("画像")
        }
            .border(Color.black)

    }

#### ボタンを右に寄せる

    HStack {
        Spacer()
        Button(action: {
            // 実行内容
        }) {
            VStack {
                Text("右寄せするテキスト")
            }
                .background(Color.yellow)
                .mask(Circle())


        }
            .padding(.trailing, 24)
    }

#### ボタンにスタイルを適応

    Button(action: {
        // 実行内容
    }) {
        VStack {
            Text("スタイルを適応するボタン")
        }
            .buttonStyle(.borderedProminent)
    }

#### ボタンサイズを大きく

    Button(action: {
        // 実行内容
    }) {
        VStack {
            Text("サイズの大きなボタン")
                .frame(maxWidth: .infinity)
        }
            .buttonStyle(.borderedProminent)
    }

### 宣言

    struct Button<Label> where Label : View

### メソッド

| 名前          | 説明          |
| ----------- | ----------- |
| buttonStyle | ボタンのスタイルの設定 |

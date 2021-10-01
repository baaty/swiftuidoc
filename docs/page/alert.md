---
layout: page
---

### 説明

アラート

### 使い方

#### ボタン1つでアラートを作成

    Alert(title: タイトル(Text), message: メッセージ(Text) = nil, dismissButton: 解除するボタン(Alert.Button) = nil)
        .メソッド

#### 2つのボタンを持つアラートを作成

    Alert(title: タイトル(Text), message: メッセージ(Text) = nil, primaryButton: 最初のボタン(Alert.Button), secondaryButton: 2番目のボタン(Alert.Button))
        .メソッド

### 引数の使い方

#### Alert.Button

| 名前                                      | 説明                              |
| --------------------------------------- | ------------------------------- |
| .default(Text, action: (() -> Void)     | デフォルト                           |
| .cancel()                               | キャンセルを示すアラートボタンをシステムが提供するラベルで作成 |
| .cancel(Text, action: (() -> Void)      | キャンセルを示すアラートボタンをカスタムラベル付きで作成    |
| .destructive(Text, action: (() -> Void) | 破壊的な動作を示すスタイルのアラートボタンを作成        |

### 宣言

    struct Alert

### メソッド

| 名前                 | 説明                  |
| ------------------ | ------------------- |
| sideBySideButtons | サイドバイサイドのボタンアラートを作成 |

### 例

#### 基本的な使い方

    @State var isError: Bool = false
    var body: some View {
        Button("Alert") {
            self.isError = true
        }
            .alert(isPresented: $isError, content: {
                Alert(title: Text("Error"), message: Text("Error Reason"), dismissButton: .default(Text("OK")))
            })
    }

#### 2つのボタンを持つアラートを作成

    @State var isError: Bool = false
    var body: some View {
        Button("Alert") {
            self.isError = true
        }
            .alert(isPresented: $isError, content: {
                Alert(title: Text("Error"), message: Text("Error Reason"), primaryButton: .default(Text("OK")), secondaryButton: .default(Text("NG")))
            })
    }

### メソッド詳細

#### sideBySideButtons

##### 意味

サイドバイサイドのボタンアラートを作成

##### 使い方

    .sideBySideButtons(title: タイトル(Text), message: メッセージ(Text) = nil, primaryButton: 最初のボタン(Alert.Button), secondaryButton: 2番目のボタン(Alert.Button))

##### 例

    Alert.sideBySideButtons(title: Text("Error"))

### 参考サイト

<https://developer.apple.com/documentation/swiftui/alert>

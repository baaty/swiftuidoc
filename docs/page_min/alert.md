---
layout: page
---

### 説明

アラート

### 使い方

#### ボタン1つでアラートを作成

    Alert(title: タイトル(Text), message: メッセージ(Text) = nil, dismissButton: 閉じるボタン(Alert.Button) = nil)

#### ボタン2つでアラートを作成

    Alert(title: タイトル(Text), message: メッセージ(Text) = nil, primaryButton: 左側に表示するボタン(Alert.Button), secondaryButton: 右側に表示するボタン(Alert.Button))

### 引数の使い方

#### Alert.Button

| 名前                                      | 説明                              |
| --------------------------------------- | ------------------------------- |
| .default(Text, action: (() -> Void)     | デフォルト                           |
| .cancel()                               | キャンセルを示すアラートボタンをシステムが提供するラベルで作成 |
| .cancel(Text, action: (() -> Void)      | キャンセルを示すアラートボタンをカスタムラベル付きで作成    |
| .destructive(Text, action: (() -> Void) | 破壊的な動作を示すスタイルのアラートボタンを作成        |

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

#### ボタン2つでアラートを作成

    @State var isError: Bool = false
    var body: some View {
        Button("Alert") {
            self.isError = true
        }
            .alert(isPresented: $isError, content: {
                Alert(title: Text("Error"), message: Text("Error Reason"), primaryButton: .default(Text("OK")), secondaryButton: .default(Text("NG")))
            })
    }

#### キャンセルボタン

    @State var isError: Bool = false
    var body: some View {
        Button("Alert") {
            self.isError = true
        }
            .alert(isPresented: $isError, content: {
                Alert(title: Text("Error"), message: Text("Error Reason"), dismissButton: .cancel(Text("キャンセル")))
            })
    }

### 宣言

    struct Alert

### メソッド

| 名前                | 説明                  |
| ----------------- | ------------------- |
| sideBySideButtons | サイドバイサイドのボタンアラートを作成 |

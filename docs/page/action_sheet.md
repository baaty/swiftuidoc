---
layout: page
---

### 説明

アクションシート

### 使い方

    ActionSheet(title: タイトル(Text), message: メッセージ(Text) = nil, buttons: 表示するボタン([ActionSheet.Button]) = [.cancel()])
        .メソッド

### 引数の使い方

#### ActionSheet.Button

| 名前                                      | 説明                              |
| --------------------------------------- | ------------------------------- |
| .default(Text, action: (() -> Void)     | デフォルト                           |
| .cancel()                               | キャンセルを示すアラートボタンをシステムが提供するラベルで作成 |
| .cancel(Text, action: (() -> Void)      | キャンセルを示すアラートボタンをカスタムラベル付きで作成    |
| .destructive(Text, action: (() -> Void) | 破壊的な動作を示すスタイルのアラートボタンを作成        |

### 宣言

    struct ActionSheet

### 例

#### 基本的な使い方

    @State private var showActionSheet = false
    var body: some View {
        Text("ActionSheet")
            .actionSheet(isPresented: $showActionSheet) {
                ActionSheet(title: Text("Action"), message: Text("Description"), buttons: [
                        .default(Text("OK"), action: {}),
                        .destructive(Text("Delete"), action: {})
                    ])
            }
    }

### 参考サイト

<https://developer.apple.com/documentation/swiftui/actionsheet>
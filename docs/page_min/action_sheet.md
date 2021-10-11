---
layout: page
---

### 説明

アクションシートを定義

### 使い方

    ActionSheet(title: タイトル(Text), message: メッセージ(Text) = nil, buttons: 表示するボタンの配列([ActionSheet.Button]) = [.cancel()])

### 引数の使い方

#### ActionSheet.Button

| 名前                                      | 説明                              |
| --------------------------------------- | ------------------------------- |
| .default(Text, action: (() -> Void)     | デフォルト                           |
| .cancel()                               | キャンセルを示すアラートボタンをシステムが提供するラベルで作成 |
| .cancel(Text, action: (() -> Void)      | キャンセルを示すアラートボタンをカスタムラベル付きで作成    |
| .destructive(Text, action: (() -> Void) | 破壊的な動作を示すスタイルのアラートボタンを作成        |

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

### 宣言

    struct ActionSheet

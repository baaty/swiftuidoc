---
layout: page
---

### 説明

長い形式のテキストを表示および編集できるビュー

### 使い方

    TextEditor(text: "編集するテキスト(Binding<String>)")

### 例

#### 基本的な使い方

    @State private var fullText: String = "This is some editable text..."
    var body: some View {
        VStack {
            Text("テキストエディタ")
            TextEditor(text: $fullText)
        }
    }

### 宣言

    struct TextEditor

### メソッド

| 名前                     | 説明                                        |
| ---------------------- | ----------------------------------------- |
| font                   | デフォルトフォントを設定                              |
| foregroundColor        | 表示されるテキストの色を設定                            |
| multilineTextAlignment | 複数行テキストの配置を設定                             |
| lineSpacing            | 行間のスペースを設定                                |
| allowsTightening       | テキストを1行に収めるために必要な場合に文字間のスペースを圧縮できるかどうかを設定 |
| autocapitalization     | 自動大文字を適用するかどうかを設定                         |
| disableAutocorrection  | 自動修正を無効にするかどうかを設定                         |
| keyboardType           | キーボードタイプを設定                               |

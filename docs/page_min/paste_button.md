---
layout: page
---

### 説明

ペーストボードからデータを読み込んでクローザーに配信するシステムボタン

### 使い方

#### ペーストボードから特定の種類のデータを受け取るPasteボタンを作成

    PasteButton(supportedContentTypes: 識別子([UTType])) { 引数([NSItemProvider]) in
        実行内容(Void)
    }

    PasteButton(supportedContentTypes: 識別子([UTType]), payloadAction: 実行内容)

#### Pasteボタンを作成しペーストボードから特定のタイプのデータを受け取りアプリに送信する前にデータのカスタム検証

    PasteButton(supportedContentTypes: 識別子([UTType]), validator: { 引数([NSItemProvider]) in
        バリデータ
    }) {
        実行内容
    }

    PasteButton(supportedContentTypes: 識別子([UTType]), validator: バリデータ?, payloadAction: 実行内容)

### 例

#### 基本的な使い方

    @State private var pastedText: String = ""
    private let plainTextUTIIdentifier = UTType.utf8PlainText.identifier
    var body: some View {
        HStack {
            PasteButton(
                supportedContentTypes: [.utf8PlainText]
            ) { itemProviders in
                itemProviders.first(where: {
                                        $0.hasItemConformingToTypeIdentifier(
                                            plainTextUTIIdentifier)})?
                    .loadDataRepresentation(forTypeIdentifier:
                                                plainTextUTIIdentifier) { data, _ in
                        if let data = data,
                        let string = String(data: data, encoding: .utf8) {
                            pastedText = string
                        }
                    }
            }
            Divider()
            Text(pastedText)
            Spacer()
        }
    }

### 宣言

    struct PasteButton

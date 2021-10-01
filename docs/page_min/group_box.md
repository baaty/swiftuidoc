---
layout: page
---

### 説明

似ているコンテンツをグルーピングするためのビュー

### 使い方

#### 基本的な使い方

    GroupBox {
        コンテンツ
    }

    GroupBox(content: コンテンツ)

#### ラベルを指定

    GroupBox(label: ラベル(Label)) {
        コンテンツ
    }

    GroupBox(label: ラベル(Label), content: コンテンツ)

#### GroupBoxStyleを指定

    GroupBox(GroupBoxStyle(GroupBoxStyleConfiguration))

### 例

#### 基本的な使い方

    @State private var textField = ""
    var body: some View {
        GroupBox {
            Text("グループ分けするテキスト")
            TextField("グループ分けするテキストフィールド", text: $textField)
        }
    }

#### ラベルを付ける

    GroupBox(label: Text("グループラベル")) {
        Text("グループ分けするテキスト")
    }

### 宣言

    struct GroupBox<Label, Content> where Label : View, Content : View

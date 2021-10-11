---
layout: page
---

### 説明

入力フォームを作るためのコンテナビュー

### 使い方

    Form {
        コンテンツ(Content)
    }

    Form(content: コンテンツ)

### 例

#### 基本的な使い方

    Form {
        Section {
            Text("Formに表示するテキスト1")
        }
        Section {
            Text("Formに表示するテキスト2")
        }
    }

#### sectionのヘッダーとフッター

    Form {
        Section(heder: Text("ヘッダーテキスト"), footer: Text("フッターテキスト")) {
            Text("Formに表示するテキスト")
        }
    }

#### 背景の色を変える

    Form {
        Section {
            Text("Section全体の色を変える")
        }
            .listRowBackground(Color.yellow)
        Section {
            Text("行ごとに色を変える")
                .listRowBackground(Color.yellow)
        }
    }

#### 更新方法

    @State private var textField = ""
    var body: some View {
        Form {
            Section {
                TextField("更新するテキスト", text: $textField)
            }
            Section {
                Button(action: {
                    // 更新するときの処理
                }) {
                    Text("更新")
                }
            }
        }
    }

#### 折り畳み式Form

    @State private var isExpanded = true
    var body: some View {
        Form {
            DisclosureGroup("Audio Settings", isExpanded: $isExpanded) {
                Text("折り畳むテキスト")
            }
        }
    }
    
### 宣言

    struct Form&lt;Content&gt; where Content : View

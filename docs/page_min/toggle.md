---
layout: page
---

### 説明

オンとオフの状態を切り替えるコントロール

### 使い方

#### カスタムラベルを表示するトグルを作成

    Toggle(isOn: $オンかオフか(Binding<Bool>)) {
        表示内容(Label)
    }

    Toggle(isOn: $オンかオフか(Binding<Bool>), label: 表示内容)

#### 文字列からラベルを生成するトグルを作成

    Toggle(トグルの説明(StringProtocol), isOn: $オンかオフか(Binding<Bool>))

#### ローカライズされた文字列キーからラベルを生成するトグルを作成

    Toggle(ローカライズされた文字列キー(LocalizedStringKey), isOn: $オンかオフか(Binding<Bool>))

#### トグルスタイルの設定に基づいてトグルを作成

    Toggle(スタイル(ToggleStyleConfiguration))

### 例

#### 基本的な使い方

    @State private var vibrateOnRing = false
    var body: some View {
        Toggle(isOn: $vibrateOnRing) {
            Text("Vibrate on Ring")
        }
    }

### 宣言

    struct Toggle<Label> where Label : View

---
layout: page
---

### 説明

スライダー操作で値を選択するためのコントロール

### 使い方

#### 与えられた範囲から値を選択し与えられたラベルを表示するスライダを作成

    Slider(value: $境界線内の選択された値(Binding<浮動小数点型>), in: 有効範囲(ClosedRange<浮動小数点型>) = 0...1, onEditingChanged: { 引数(Bool) in
        編集開始・終了時のコールバック(Void)
    }) {
        インスタンスの目的を説明するビュー(View)
    }

    Slider(value: $境界線内の選択された値(Binding<浮動小数点型>), in: 有効範囲(ClosedRange<浮動小数点型>) = 0...1, onEditingChanged: 編集開始・終了時のコールバック = { _ in }, label: インスタンスの目的を説明するビュー)

#### 与えられたラベルを表示し指定された範囲からステップインクリメントで値を選択するスライダーを作成

    Slider(value: $境界線内の選択された値(Binding<浮動小数点型>), in: 有効範囲(ClosedRange<浮動小数点型>) = 0...1, step: 有効範囲(V.Stride) = 1, onEditingChanged: { 引数(Bool) in
        編集開始・終了時のコールバック(Void)
    }) {
        インスタンスの目的を説明するビュー(View)
    }

    Slider(value: $境界線内の選択された値(Binding<浮動小数点型>), in: 有効範囲(ClosedRange<浮動小数点型>) = 0...1, step: 有効範囲(V.Stride) = 1, onEditingChanged: 編集開始・終了時のコールバック = { _ in }, label: インスタンスの目的を説明するビュー)

#### 与えられた範囲から値を選択し与えられたラベルを表示するスライダを作成

    Slider(value: $境界線内の選択された値(Binding<浮動小数点型>), in: 有効範囲(ClosedRange<浮動小数点型>) = 0...1, onEditingChanged: {
        編集開始・終了時のコールバック(Void)
    }, minimumValueLabel: bounds.lowerBoundを記述したビュー(ValueLabel), maximumValueLabel: bounds.lowerBoundを記述したビュー(ValueLabel)) {
        インスタンスの目的を説明するビュー(View)
    }

    Slider(value: $境界線内の選択された値(Binding<浮動小数点型>), in: 有効範囲(ClosedRange<浮動小数点型>) = 0...1, onEditingChanged: 編集開始・終了時のコールバック = { _ in }, minimumValueLabel: bounds.lowerBoundを記述したビュー(ValueLabel), maximumValueLabel: bounds.lowerBoundを記述したビュー(ValueLabel), label: インスタンスの目的を説明するビュー)

### 浮動小数点型の種類

| 名前          | 説明      |
| ----------- | ------- |
| 小数点付きの数字    | Float   |
| CGFloat(数字) | CGFloat |
| Double(数字)  | Double  |
| Float(数字)   | Float   |
| Float16(数字) | Float16 |
| Float80(数字) | Float80 |

### ClosedRangeの使い方

| 名前       | 説明   |
| -------- | ---- |
| 数字...数字　 | 値の範囲 |

### 例

#### 基本的な使い方

    @State private var speed = 0.5
    var body: some View {
        VStack {
            Slider(value: $speed)
        }
    }

#### 有効範囲を設定

    @State private var speed = 10.0
    var body: some View {
        VStack {
            Slider(value: $speed, in: 0...50)
        }
    }


### 宣言

    struct Slider<Label, ValueLabel> where Label : View, ValueLabel : View

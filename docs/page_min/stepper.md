---
layout: page
---

### 説明

インクリメントとデクリメントの動作を行うコントロール

### 使い方

#### タイトル文字列を使ってステッパーを作成しユーザーがステッパーの増減ボタンをクリックまたはタップしたときに指定したクロージャを実行

    Stepper(ステッパーのタイトル(StringProtocol), onIncrement: {
        プラスボタンを押したときに実行されるクロージャー(Void)
    }, onDecrement: {
        マイナスボタンを押したときに実行されるクロージャー
    }) {
        編集の開始と終了時に呼び出されるクロージャ
    }

    Stepper(ステッパーのタイトル(StringProtocol), onIncrement: プラスボタンを押したときに実行されるクロージャー?, onDecrement: マイナスボタンを押したときに実行されるクロージャー?, onEditingChanged: 編集の開始と終了時に呼び出されるクロージャ)

#### タイトルキーを使用するステッパーを作成しユーザーがステッパーのインクリメントおよびデクリメントボタンをクリックまたはタップしたときに指定したクロージャを実行

    Stepper(ローカライズされた文字列キー(LocalizedStringKey), onIncrement: {
        プラスボタンを押したときに実行されるクロージャー(Void)
    }, onDecrement: {
        マイナスボタンを押したときに実行されるクロージャー
    }) {
        編集の開始と終了時に呼び出されるクロージャ
    }

    Stepper(ローカライズされた文字列キー(LocalizedStringKey), onIncrement: プラスボタンを押したときに実行されるクロージャー?, onDecrement: マイナスボタンを押したときに実行されるクロージャー?, onEditingChanged: 編集の開始と終了時に呼び出されるクロージャ)

#### 値に対するバインディングを指定したステップサイズで指定したクローズドレンジ内でインクリメントデクリメントするステッパーインスタンスを作成

    Stepper(ステッパーのタイトル(StringProtocol), value: $バインディング値(Binding<Strideable>), in: ステッパーが許容する上限と下限(ClosedRange<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1) {
        編集の開始と終了時に呼び出されるクロージャ(Void)
    }

    Stepper(ステッパーのタイトル(StringProtocol), value: $バインディング値(Binding<Strideable>), in: ステッパーが許容する上限と下限(ClosedRange<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1, onEditingChanged: 編集の開始と終了時に呼び出されるクロージャ)

#### 値に対するバインディングを指定したステップサイズで指定したクローズドレンジ内でインクリメントデクリメントするステッパーインスタンスを作成

    Stepper(ステッパーのタイトル(LocalizedStringKey), value: $バインディング値(Binding<Strideable>), in: ステッパーが許容する上限と下限(ClosedRange<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1) {
        編集の開始と終了時に呼び出されるクロージャ(Void)
    }

    Stepper(ステッパーのタイトル(LocalizedStringKey), value: $バインディング値(Binding<Strideable>), in: ステッパーが許容する上限と下限(ClosedRange<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1, onEditingChanged: 編集の開始と終了時に呼び出されるクロージャ)

#### タイトルキーを持ち指定された値とステップ量に合わせてバインディングをインクリメントデクリメントするように設定されたステッパーを作成

    Stepper(ステッパーのタイトル(StringProtocol), value: $バインディング値(Binding<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1) {
        編集の開始と終了時に呼び出されるクロージャ(Void)
    }

    Stepper(ステッパーのタイトル(StringProtocol), value: $バインディング値(Binding<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1, onEditingChanged: 編集の開始と終了時に呼び出されるクロージャ) 

#### ユーザーがステッパーをインクリメントまたはデクリメントしたときに指定したクロージャを実行するステッパーのインスタンスを作成

    Stepper(onIncrement: プラスボタンを押したときに実行されるクロージャー?, onDecrement: マイナスボタンを押したときに実行されるクロージャー?, onEditingChanged: {
        編集の開始と終了時に呼び出されるクロージャ
    }) {
        ラベル
    }

    Stepper(onIncrement: プラスボタンを押したときに実行されるクロージャー?, onDecrement: マイナスボタンを押したときに実行されるクロージャー?, onEditingChanged: 編集の開始と終了時に呼び出されるクロージャ, label: ラベル)

#### ステップ値を使って指定した値の範囲内でバインディングを値にインクリメントまたはデクリメントするように構成されたステッパーを作成

    Stepper(value: $バインディング値(Binding<Strideable>), in: ステッパーが許容する上限と下限(ClosedRange<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1, onEditingChanged: {
        編集の開始と終了時に呼び出されるクロージャ
    }) {
        ラベル
    }

    Stepper(value: $バインディング値(Binding<Strideable>), in: ステッパーが許容する上限と下限(ClosedRange<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1, onEditingChanged: 編集の開始と終了時に呼び出されるクロージャ, label: ラベル)

#### 指定されたステップ値を使ってバインディングを値にインクリメントまたはデクリメントするように構成されたステッパーを作成

    Stepper(value: $バインディング値(Binding<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1, onEditingChanged: {
        編集の開始と終了時に呼び出されるクロージャ
    }) {
        ラベル
    }

    Stepper(value: $バインディング値(Binding<Strideable>), step: 増加または減少させる量(Strideable.Stride) = 1, onEditingChanged: 編集の開始と終了時に呼び出されるクロージャ, label: ラベル)

### 例

#### 基本的な使い方

    @State private var value = 0
    var body: some View {
        Stepper("ステッパー", value: $value)
    }

#### 範囲指定

    @State private var value = 0
    var body: some View {
        Stepper("ステッパー", value: $value, in: 1...10)
    }

### 宣言

    struct Stepper<Label> where Label : View

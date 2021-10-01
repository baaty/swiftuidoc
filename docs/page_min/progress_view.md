---
layout: page
---

### 説明

タスクの完了に向けた進捗状況を示すビュー

### 使い方

#### 不確定な進捗状況を表示するプログレスビューをラベルなしで作成

    ProgressView()

#### 不確定な進捗状況を表示するプログレスビューを作成しカスタムラベルを表示

    ProgressView() {
        ラベル
    }

    ProgressView(label: ラベル)

#### 確定した進捗状況を表示するプログレスビューを作成

    ProgressView(value: 進捗(BinaryFloatingPoint)?, total: 値の合計(BinaryFloatingPoint) = 1.0)

#### 確定した進捗状況を表示するプログレスビューをカスタムラベル付きで作成

    ProgressView(value: 進捗(BinaryFloatingPoint)?, total: 値の合計(BinaryFloatingPoint) = 1.0) {
        ラベル(Label)
    }

    ProgressView(value: 進捗(BinaryFloatingPoint)?, total: 値の合計(BinaryFloatingPoint) = 1.0, label: ラベル)

#### 不確定な進捗状況を表示するプログレスビューを作成し文字列からラベルを生成

    ProgressView(進行中のタスクのタイトル(StringProtocol))

#### ローカライズされた文字列からラベルを生成する不確定な進捗状況を表示するプログレスビューを作成

    ProgressView(ローカライズされた文字列キー(LocalizedStringKey))

#### スタイル設定に基づいてプログレスビューを作成

    ProgressView(スタイル(ProgressViewStyleConfiguration))

#### 与えられたプログレスインスタンスを視覚化するプログレスビューを作成

    ProgressView(プログレスインスタンス(Progress))

#### ローカライズされた文字列からラベルを生成する確定した進捗状況を表示するプログレスビューを作成

    ProgressView(進行中のタスクのタイトル(StringProtocol or LocalizedStringKey), value: 進捗(BinaryFloatingPoint)?, total: 値の合計(BinaryFloatingPoint) = 1.0)

#### 確定した進捗状況を表示するプログレスビューをカスタムラベル付きで作成

    ProgressView(value: 進捗(BinaryFloatingPoint)?, total: 値の合計(BinaryFloatingPoint) = 1.0, label: {
        ラベル(Lavel)
    }) {
        完了した進捗状況のレベルを表すビュー(CurrentValueLabel)
    }

    ProgressView(value: 進捗(BinaryFloatingPoint)?, total: 値の合計(BinaryFloatingPoint) = 1.0, label: ラベル, currentValueLabel: 完了した進捗状況のレベルを表すビュー)

### 例

#### 基本的な使い方

    @State private var progress = 0.5
    var body: some View {
        ProgressView(value: progress)
        Button("More", action: { progress += 0.05 })
    }

#### 進捗ラベルをカスタマイズ

    @State private var progress = 0.5
    var body: some View {
        ProgressView(value: progress, label: {
            Text("進捗状況")
        }) {
            Text("進捗率: \(progress)")
        }
    }

#### 進捗バーをカスタマイズ

    @State private var progress = 0.5
    var body: some View {
        ProgressView(value: progress)
            .accentColor(.yellow)
    }

### 宣言

    struct ProgressView<Label, CurrentValueLabel> where Label : View, CurrentValueLabel : View

---
layout: page
---

### 説明

範囲内の値を表示するビュー

### 使い方

#### 範囲内の値を示すゲージを作成しゲージの目的と現在の値を説明

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1) {
        表示内容(Label)
    }

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1, label: 表示内容)

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1), label: {
        表示内容(Label)
    }) {
        現在の値を表すビュー(CurrentValueLabel)
    }

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1, label: 表示内容, currentValueLabel: 現在の値を表すビュー)

#### 範囲内の値を表すゲージを作成

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1, label: {
        表示内容(Label)
    }, currentValueLabel: {
        現在の値を表すビュー(CurrentValueLabel)
    }) {
        タグ付けされたビューを含むビュービルダー(MarkedValueLabels)
    }

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1, label: 表示内容, currentValueLabel: 現在の値を表すビュー, markedValueLabels: タグ付けされたビューを含むビュービルダー)

#### 指定した範囲の値を表示するゲージを作成しゲージの現在値、最小値、最大値

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1, label: {
        表示内容(Label)
    }, currentValueLabel: {
        現在の値を表すビュー(CurrentValueLabel)
    }, minimumValueLabel: {
        下限を表すビュー(BoundsLabel)
    }) {
        上限を表すビュー(BoundsLabel)
    }

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1, label: 表示内容, currentValueLabel: 現在の値を表すビュー, minimumValueLabel: 下限を表すビュー, maximumValueLabel: 上限を表すビュー)

#### 範囲内の値を表すゲージを作成

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1, label: {
        表示内容(Label)
    }, currentValueLabel: {
        現在の値を表すビュー(CurrentValueLabel)
    }, minimumValueLabel: {
        下限を表すビュー(BoundsLabel)
    }, maximumValueLabel: {
        上限を表すビュー(BoundsLabel)
    }) {
        タグ付けされたビューを含むビュービルダー(MarkedValueLabels)
    }

    Gauge(value: ゲージに表示する値(BinaryFloatingPoint), in: 有効な値の範囲(ClosedRange<BinaryFloatingPoint>) = 0...1, label: 表示内容, currentValueLabel: 現在の値を表すビュー, minimumValueLabel: 下限を表すビュー, maximumValueLabel: 上限を表すビュー, markedValueLabels: タグ付けされたビューを含むビュービルダーs)

### 例

#### 基本的な使い方

    struct SimpleGauge: View {
        @State private var batteryLevel = 0.4
        var body: some View {
            Gauge(value: batteryLevel) {
                Text("Battery Level")
            }
        }
    }

### 宣言

    struct Gauge<Label, CurrentValueLabel, BoundsLabel, MarkedValueLabels> where Label : View, CurrentValueLabel : View, BoundsLabel : View, MarkedValueLabels : View

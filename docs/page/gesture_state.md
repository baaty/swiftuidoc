---
layout: page
---

### 説明

ユーザーがジェスチャーを行っている間にプロパティを更新しジェスチャーが終わるとプロパティを初期状態に戻すプロパティラッパー

### 使い方

#### 初期値を持つジェスチャーから派生したビュー・ステートを作成

    GestureState(initialValue: 状態の初期値(Value))

#### 状態の初期値を持つジェスチャーから派生したビューの状態とそれをリセットするためのトランザクションを提供するクロージャを作成

    GestureState(initialValue: 状態の初期値(Value)) {
        Transactionを提供するクロージャー
    }

    GestureState(initialValue: 状態の初期値(Value), reset: Transactionを提供するクロージャー)

#### 初期状態の値とそれをリセットするためのトランザクションを持つジェスチャーから派生したビューの状態を作成

    GestureState(initialValue: 状態の初期値(Value), resetTransaction: ビューの更新のためのメタデータを提供するトランザクション(Transaction))

#### ジェスチャーから派生したビューの状態をそれをリセットするためのトランザクションを提供するクロージャとともに作成

    GestureState {
        Transactionを提供するクロージャー
    }

    GestureState(reset: Transactionを提供するクロージャー)

#### ジェスチャーから派生したビューの状態をそれをリセットするためのトランザクションとともに作成

    GestureState(resetTransaction: ビューの更新のためのメタデータを提供するトランザクション(Transaction) = Transaction())

#### ジェスチャーから派生したビュー・ステートを作成

    GestureState(wrappedValue: ジェスチャーの状態を表すプロパティのラップ値(Value))

#### ステートの値をラップしたジェスチャーとそれをリセットするためのトランザクションを提供するクロージャから派生したビューのステートを作成

    GestureState(wrappedValue: ジェスチャーの状態を表すプロパティのラップ値(Value)) {
        Transactionを提供するクロージャー
    }

    GestureState(wrappedValue: ジェスチャーの状態を表すプロパティのラップ値(Value), reset: Transactionを提供するクロージャー)

#### ステートの値をラップしたジェスチャーから派生したビュー・ステートを作成しそれをリセットするためのトランザクションを作成

    GestureState(wrappedValue: ジェスチャーの状態を表すプロパティのラップ値(Value), resetTransaction: ビューの更新のためのメタデータを提供するトランザクション(Transaction))

### 例

#### 基本的な使い方

    struct SimpleLongPressGestureView: View {
        @GestureState var isDetectingLongPress = false
        var longPress: some Gesture {
            LongPressGesture(minimumDuration: 3)
                .updating($isDetectingLongPress) { currentState, gestureState, transaction in
                    gestureState = currentState
                }
        }
        var body: some View {
            Circle()
                .fill(self.isDetectingLongPress ? Color.red : Color.green)
                .frame(width: 100, height: 100, alignment: .center)
                .gesture(longPress)
        }
    }

### 宣言

    @propertyWrapper @frozen struct GestureState<Value>

### プロパティ

| 名前             | 型                   | 説明                 |
| -------------- | ------------------- | ------------------ |
| wrappedValue   | Value               | プロパティで参照されるラップされた値 |
| projectedValue | GestureState<Value> | ジェスチャーの状態を表すプロパティ  |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/gesturestate>

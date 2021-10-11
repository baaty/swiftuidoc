---
layout: page
---

### 説明

ユーザーが長押しすると成功するジェスチャー

### 使い方

    LongPressGesture(minimumDuration: ジェスチャーが成功するまでに経過しなければならない長押しの最小時間(Double) = 0.5, maximumDistance: ジェスチャーが失敗するまでに移動できる最大の距離(CGFloat) = 10)

    LongPressGesture(minimumDuration: ジェスチャーが成功するまでに経過しなければならない長押しの最小時間(Double) = 0.5)

### 例

#### 基本的な使い方

    struct LongPressGestureView: View {
        @GestureState var isDetectingLongPress = false
        @State var completedLongPress = false
        var longPress: some Gesture {
            LongPressGesture(minimumDuration: 3)
                .updating($isDetectingLongPress) { currentState, gestureState,
                        transaction in
                    gestureState = currentState
                    transaction.animation = Animation.easeIn(duration: 2.0)
                }
                .onEnded { finished in
                    self.completedLongPress = finished
                }
        }
        var body: some View {
            Circle()
                .fill(self.isDetectingLongPress ?
                    Color.red :
                    (self.completedLongPress ? Color.green : Color.blue))
                .frame(width: 100, height: 100, alignment: .center)
                .gesture(longPress)
        }
    }

### 宣言

    struct LongPressGesture

### プロパティ

| 名前              | 型       | 説明                                |
| --------------- | ------- | --------------------------------- |
| minimumDuration | Double  | ジェスチャーが成功するまでに経過しなければならない長押しの最小時間 |
| maximumDistance | CGFloat | ジェスチャーが失敗するまでに移動できる最大の距離          |

### メソッド

| 名前             | 説明                                                                     |
| -------------- | ---------------------------------------------------------------------- |
| updating       | ジェスチャーの値が変更されると提供されたジェスチャーの状態プロパティを更新                                  |
| onChanged      | ジェスチャーの値が変化したときに実行するアクションを追加                                           |
| onEnded        | ジェスチャーの終了時に実行するアクションを追加                                                |
| simultaneously | 別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成                           |
| sequenced      | 別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけになる |
| exclusively    | 1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先                              |
| modifiers      | ジェスチャーとキーボードメソッドを組み合わせ                                                 |
| map            | 与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー                                    |

### メソッド詳細

#### updating

##### 意味

ジェスチャーの値が変更されると提供されたジェスチャーの状態プロパティを更新

##### 使い方

    .updating(GestureStateプロパティ(GestureState<State>)) {値(Self.Value), 状態(State), トランザクション(Transaction) in
        SwiftUIが呼び出すコールバック
    }

    .updating<State>(GestureStateプロパティ(GestureState<State>), body: SwiftUIが呼び出すコールバック)

##### 例

    LongPressGesture()
        .updating($isDragging) {_,_,_  in
            // コールバック
        }

#### onChanged

##### 意味

ジェスチャーの値が変化したときに実行するアクションを追加

##### 使い方

    .onChanged {値(Self.Value) in
        実行するアクション
    }

    .onChanged(実行するアクション)

##### 例

    LongPressGesture()
        .onChanged {_ in
            // アクション
        }

#### onEnded

##### 意味

ジェスチャーの終了時に実行するアクションを追加

##### 使い方

    .onEnded {値(Self.Value) in
        終了したときに実行するアクション
    }

    .onEnded(終了したときに実行するアクション)

##### 例

    LongPressGesture()
        .onEnded {_ in
            // アクション
        }

#### simultaneously

##### 意味

別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成

##### 使い方

    .simultaneously(with: 新しい結合されたジェスチャーを作成するためのジェスチャー(Other))

##### 例

    LongPressGesture()
        .simultaneously(with: TapGesture())

#### sequenced

##### 意味

別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけになる

##### 使い方

    .sequenced(before: 連続した新しいジェスチャーを作成したいジェスチャー(Other))

##### 例

    LongPressGesture()
        .sequenced(before: TapGesture())

#### exclusively

##### 意味

1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先

##### 使い方

    .exclusively<Other>(before: 新しい組み合わせのジェスチャー(Other))

##### 例

    LongPressGesture()
        .exclusively(before: TapGesture())

### modifiers

##### 意味

ジェスチャーとキーボードメソッドを組み合わせ

##### 使い方

    .modifiers(ユーザーが押し続ける必要のあるメソッドキーに対応するフラグのセット(EventModifiers))

##### EventModifiersの使い方

| 名前                                            | 説明                       |
| --------------------------------------------- | ------------------------ |
| .all                                          | 全て                       |
| .capsLock                                     | Caps Lock キー             |
| .command                                      | Commandキー                |
| .control                                      | Controlキー                |
| .function                                     | Functionキー               |
| .numericPad                                   | テンキー                     |
| .option                                       | Optionキー                 |
| .shift                                        | Shiftキー                  |
| EventModifiers()                              | 空のオプションセットを作成            |
| EventModifiers&lt;Sequence&gt;(Sequence)        | アイテムの有限のシーケンスから新しいセットを作成 |
| EventModifiers(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成  |
| EventModifiers(rawValue: Int)                 | 生の値から新しいセットを作成           |

##### 例

    LongPressGesture()
        .modifiers(.all)

#### map

##### 意味

与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー

##### 使い方

    .map(ジェスチャー)

##### 例

    LongPressGesture()
        .map {_ in
            // ジェスチャー
        }

### 参考サイト

<https://developer.apple.com/documentation/swiftui/longpressgesture>

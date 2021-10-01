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

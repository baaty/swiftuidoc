---
layout: page
---

### 説明

拡大動作を認識し拡大量を追跡するジェスチャー

### 使い方

    MagnificationGesture(minimumScaleDelta: 開始する前に必要な最小のスケールデルタ(CGFloat) = 0.01)

### 例

#### 基本的な使い方

    struct MagnificationGestureView: View {
        @GestureState var magnifyBy = CGFloat(1.0)
        var magnification: some Gesture {
            MagnificationGesture()
                .updating($magnifyBy) { currentState, gestureState, transaction in
                    gestureState = currentState
                }
        }
        var body: some View {
            Circle()
                .frame(width: 100 * magnifyBy,
                      height: 100 * magnifyBy,
                      alignment: .center)
                .gesture(magnification)
        }
    }

### 宣言

    struct MagnificationGesture

### プロパティ

| 名前                | 型       | 説明             |
| ----------------- | ------- | -------------- |
| minimumScaleDelta | CGFloat | 始まる前に必要な最小のデルタ |

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

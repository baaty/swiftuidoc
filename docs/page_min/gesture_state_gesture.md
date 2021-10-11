---
layout: page
---

### 説明

ジェスチャーの更新コールバックによって提供された状態を更新するジェスチャー

### 使い方

    GestureStateGesture(base: 発端となるジェスチャ(Gesture), state: GestureStateプロパティのラップされた値(GestureState<State>)) {
        ジェスチャーの値が変化したときにSwiftUIが呼び出すコールバック
    }

    GestureStateGesture(base: 発端となるジェスチャ(Gesture), state: GestureStateプロパティのラップされた値(GestureState<State>), body: ジェスチャーの値が変化したときにSwiftUIが呼び出すコールバック)

### 例

#### 基本的な使い方

    @GestureState var isDragging = false
    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }

### 宣言

    @frozen struct GestureStateGesture<Base, State> where Base : Gesture

### プロパティ

| 名前    | 型                                                                                   | 説明                                               |
| ----- | ----------------------------------------------------------------------------------- | ------------------------------------------------ |
| base  | Base                                                                                | 発端となるジェスチャー                                      |
| body  | (GestureStateGesture&lt;Base, State>.Value, inout State, inout Transaction) -> Void | 発信元のジェスチャーの値ジェスチャーの更新された状態およびトランザクションを含む更新ジェスチャー |
| state | GestureState&lt;State&gt;                                                                 | ユーザーがジェスチャーを行うことで変化する値                           |

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

---
layout: page
---

### 説明

ジェスチャーの更新コールバックによって提供された状態を更新するジェスチャー

### 使い方

    GestureStateGesture(base: 発端となるジェスチャ(Gesture), state: GestureStateプロパティのラップされた値(GestureState<State>)) {
        ジェスチャーの値が変化したときにSwiftUIが呼び出すコールバック
    }
        .メソッド

    GestureStateGesture(base: 発端となるジェスチャ(Gesture), state: GestureStateプロパティのラップされた値(GestureState<State>), body: ジェスチャーの値が変化したときにSwiftUIが呼び出すコールバック)
        .メソッド

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
| state | GestureState<State>                                                                 | ユーザーがジェスチャーを行うことで変化する値                           |

### メソッド

| 名前             | 説明                                                                     |
| -------------- | ---------------------------------------------------------------------- |
| updating       | ジェスチャーの値が変更されると提供されたジェスチャーの状態プロパティを更新                                  |
| onChanged      | ジェスチャーの値が変化したときに実行するアクションを追加                                           |
| onEnded        | ジェスチャーの終了時に実行するアクションを追加                                                |
| simultaneously | 別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成                           |
| sequenced      | 別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけになる |
| exclusively    | 1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先                              |
| modifiers      | ジェスチャーとキーボードモディファイアを組み合わせ                                              |
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

    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }
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

    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }
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

    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }
        .onEnded {_ in
            // アクション
        }

#### simultaneously

##### 意味

別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成

##### 使い方

    .simultaneously(with: 新しい結合されたジェスチャーを作成するためのジェスチャー(Other))

##### 例

    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }
        .simultaneously(with: TapGesture())

#### sequenced

##### 意味

別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけになる

##### 使い方

    .sequenced(before: 連続した新しいジェスチャーを作成したいジェスチャー(Other))

##### 例

    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }
        .sequenced(before: TapGesture())

#### exclusively

##### 意味

1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先

##### 使い方

    .exclusively<Other>(before: 新しい組み合わせのジェスチャー(Other))

##### 例

    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }
        .exclusively(before: TapGesture())

### modifiers

##### 意味

ジェスチャーとキーボードモディファイアを組み合わせ

##### 使い方

    .modifiers(ユーザーが押し続ける必要のあるモディファイアキーに対応するフラグのセット(EventModifiers))

##### フラグのセットの種類(EventModifiers)

| 名前                                              | 説明                       |
| ----------------------------------------------- | ------------------------ |
| .all                                            | 全て                       |
| .capsLock                                       | Caps Lock キー             |
| .command                                        | Commandキー                |
| .control                                        | Controlキー                |
| .function                                       | Functionキー               |
| .numericPad                                     | テンキー                     |
| .option                                         | Optionキー                 |
| .shift                                          | Shiftキー                  |
| EventModifiers()                                | 空のオプションセットを作成            |
| EventModifiers<Sequence>(Sequence) | アイテムの有限のシーケンスから新しいセットを作成 |
| EventModifiers(arrayLiteral: Self.Element...)   | 与えられた配列リテラルの要素を含むセットを作成  |
| EventModifiers(rawValue: Int)                   | 生の値から新しいセットを作成           |

##### 例

    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }
        .modifiers(.all)

#### map

##### 意味

与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー

##### 使い方

    .map {値(Self.Value) in
        // ジェスチャー
    }

    .map(ジェスチャー)

##### 例

    GestureStateGesture(base: DragGesture(), state: $isDragging) {_,_,_ in }
        .map {_ in
            // ジェスチャー
        }

### 参考サイト

<https://developer.apple.com/documentation/swiftui/gesturestategesture>

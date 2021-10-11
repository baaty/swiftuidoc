---
layout: page
---

### 説明

型が無いジェスチャー

### 使い方

    AnyGesture(Gestureの値)

### 引数の使い方

#### Gesture

| 名前                   | 説明                                    |
| -------------------- | ------------------------------------- |
| AnyGesture           | 型が無いジェスチャー                            |
| DragGesture          | ドラッグ処理                                |
| ExclusiveGesture     | 2つのジェスチャーで構成されておりどちらか一方しか成功しないジェスチャー  |
| GestureStateGesture  | ジェスチャーの更新コールバックによって提供された状態を更新するジェスチャー |
| LongPressGesture     | 与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー   |
| MagnificationGesture | 拡大動作を認識し拡大量を追跡するジェスチャー                |
| RotationGesture      | 回転動作を認識しその角度を追跡するジェスチャー               |
| SequenceGesture      | 2つのジェスチャーを連続させたジェスチャー                 |
| SimultaneousGesture  | 同時に起こりうる2つのジェスチャーを含みどちらも先行しないジェスチャー   |
| TapGesture           | 1回以上のタップを認識するジェスチャー                   |

### 例

#### 基本的な使い方

    AnyGesture(DragGesture(minimumDistance: 0, coordinateSpace: .global))

### 宣言

    @frozen struct AnyGesture&lt;Value&gt;

### プロパティ

| 名前              | 型       | 説明                                |
| --------------- | ------- | --------------------------------- |
| minimumDuration | Double  | ジェスチャーが成功するまでに経過しなければならない長押しの最小時間 |
| maximumDistance | CGFloat | ジェスチャーが失敗するまでに移動できる最大の距離          |

### メソッド

| 名前             | 説明                                                                     |
| -------------- | ---------------------------------------------------------------------- |
| updating       | ジェスチャーの値が変更されると提供されたジェスチャーの状態を更新                                       |
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

ジェスチャーの値が変更されると提供されたジェスチャーの状態を更新

##### 使い方

    .updating(AnyGestureStateプロパティ(AnyGestureState<State>)) { 引数(State) in
        SwiftUIが呼び出すコールバック
    }

    .updating(AnyGestureStateプロパティ(AnyGestureState<State>), body: SwiftUIが呼び出すコールバック)

##### 例

    AnyGesture(DragGesture(minimumDistance: 0, coordinateSpace: .global)
        .updating($dragState) { drag in
            // 更新内容
        }

#### onChanged

##### 意味

ジェスチャーの値が変化したときに実行するアクションを追加

##### 使い方

    .onChanged {
        実行するアクション
    }

    .onChanged(実行するアクション)

##### 例

    AnyGesture(DragGesture(minimumDistance: 0, coordinateSpace: .global))

#### onEnded

##### 意味

ジェスチャーの終了時に実行するアクションを追加

##### 使い方

    .onEnded {
        終了したときに実行するアクション
    }

    .onEnded(終了したときに実行するアクション)

##### 例

    AnyGesture(DragGesture(minimumDistance: 0, coordinateSpace: .global)
        .onEnded {
            // 実行するアクション
        }

#### simultaneously

##### 意味

別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成

##### 使い方

    .simultaneously(with: 新しい結合されたジェスチャーを作成するためのジェスチャー(Other))

#### sequenced

##### 意味

別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけになる

##### 使い方

    .sequenced(before: 連続した新しいジェスチャーを作成したいジェスチャー(Other))

#### exclusively

##### 意味

1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先

##### 使い方

    .exclusively<Other>(before: 新しい組み合わせのジェスチャー(Other))

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
| EventModifiers&lt;Sequence&gt;(Sequence)            | アイテムの有限のシーケンスから新しいセットを作成 |
| EventModifiers(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成  |
| EventModifiers(rawValue: Int)                 | 生の値から新しいセットを作成           |

#### map

##### 意味

与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー

##### 使い方

    .map(ジェスチャー)

### 参考サイト

<https://developer.apple.com/documentation/swiftui/anygesture>

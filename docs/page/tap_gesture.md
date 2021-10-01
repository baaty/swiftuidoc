---
layout: page
---

### 説明

1回以上のタップを認識するジェスチャー

### 使い方

    TapGesture(count: タップ数(Int) = 1)

### 例

#### 基本的な使い方

    TapGesture()

### 宣言

    struct TapGesture

### プロパティ

| 名前    | 型   | 説明           |
| ----- | --- | ------------ |
| count | Int | 必要なタップイベントの数 |

### メソッド

| 名前             | 説明                                                                           |
| -------------- | ---------------------------------------------------------------------------- |
| updating       | ジェスチャーの値が変更されると提供されたジェスチャー・ステート・プロパティを更新                                     |
| onEnded        | ジェスチャーの終了時に実行するアクション                                                         |
| simultaneously | あるジェスチャーと別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成                        |
| sequenced      | あるジェスチャーと別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけ |
| exclusively    | 2つのジェスチャーを排他的に組み合わせて1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先                |
| modifiers      | ジェスチャーとキーボードメソッドを組み合わせ                                                       |
| map            | 与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー                                          |

### メソッド詳細

#### updating

##### 意味

ジェスチャーの値が変更されると提供されたジェスチャー・ステート・プロパティを更新

##### 使い方

    .updating(GestureStateプロパティへのバインディング(GestureState<State>)) {値(Self.Value), 状態(State), トランザクション(Transaction) in
        ジェスチャーの値が変更されるとSwiftUIが呼び出すコールバック
    }

    .updating(GestureStateプロパティへのバインディング(GestureState<State>), body: ジェスチャーの値が変更されるとSwiftUIが呼び出すコールバック)

##### 例

    TapGesture()
        .updating($isDragging) {_,_,_  in
            // コールバック
        }

#### onEnded

##### 意味

ジェスチャーの終了時に実行するアクション

##### 使い方

    .onEnded {値(Self.Value) in
        実行するアクション
    }

    .onEnded(実行するアクション)

##### 例

    TapGesture()
        .onEnded {_ in
            // アクション
        }

#### simultaneously

##### 意味

あるジェスチャーと別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成

##### 使い方

    .simultaneously(with: 新しい結合されたジェスチャーを作成するためのジェスチャー(Other))

##### 例

    TapGesture()
        .simultaneously(with: TapGesture())

#### sequenced

##### 意味

あるジェスチャーと別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけ

##### 使い方

    .sequenced(before: 連続した新しいジェスチャーを作成したいジェスチャー(Other))

##### 例

    TapGesture()
        .sequenced(before: TapGesture())

#### exclusively

##### 意味

2つのジェスチャーを排他的に組み合わせて1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先

##### 使い方

    .exclusively(before: 自分のジェスチャーと組み合わせて新しい組み合わせのジェスチャーを作る(Other))

##### 例

    TapGesture()
        .exclusively(before: TapGesture())

#### modifiers

##### 意味

ジェスチャーとキーボードメソッドを組み合わせ

##### 使い方

    .modifiers(ユーザーが押し続ける必要のあるメソッドキーに対応するフラグのセット(EventModifiers))

##### 例

    TapGesture()
        .modifiers(.all)

#### map

##### 意味

与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー

##### 使い方

    .map(ジェスチャー)

##### 例

    TapGesture()
        .map {_ in
            // ジェスチャー
        }

### 参考サイト

<https://developer.apple.com/documentation/swiftui/tapgesture>

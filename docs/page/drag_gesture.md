---
layout: page
---

### 説明

ドラッグ処理

### 使い方

    DragGesture(minimumDistance: ジェスチャーが成功するための最小のドラッグ距離(CGFloat) = 10, coordinateSpace: ドラッグの位置の座標空間(CoordinateSpace) = .local)

### 引数の使い方

#### CoordinateSpace

| 名前                  | 説明        |
| ------------------- | --------- |
| .global             | Global座標　 |
| .local              | Local座標　  |
| .named(AnyHashable) |           |

### 例

#### 基本的な使い方

    struct DragGestureView: View {
        @State var isDragging = false
        var drag: some Gesture {
            DragGesture()
                .onChanged { _ in self.isDragging = true }
                .onEnded { _ in self.isDragging = false }
        }
        var body: some View {
            Circle()
                .fill(self.isDragging ? Color.red : Color.blue)
                .frame(width: 100, height: 100, alignment: .center)
                .gesture(drag)
        }
    }

### 宣言

    struct DragGesture

### プロパティ

| 名前              | 型               | 説明                      |
| --------------- | --------------- | ----------------------- |
| minimumDistance | CGFloat         | ジェスチャーが成功するまでのドラッグの最小距離 |
| coordinateSpace | CoordinateSpace | 位置情報の値を受け取る座標空間         |

### メソッド

| 名前             | 説明                                                                     |
| -------------- | ---------------------------------------------------------------------- |
| updating       | ジェスチャーの値が変更されると提供されたジェスチャーの状態プロパティを更新                                  |
| onChanged      | ジェスチャーの値が変化したときに実行するアクションを追加                                           |
| onEnded        | ジェスチャーの終了時に実行するアクションを追加                                                |
| simultaneously | 別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成                           |
| sequenced      | 別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけになる |
| exclusively    | 1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先                              |
| modifiers      | ジェスチャーとキーボードメソッドを組み合わせ                                              |
| map            | 与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー                                    |

### メソッド詳細

#### updating

##### 意味

ジェスチャーの値が変更されると提供されたジェスチャーの状態プロパティを更新

##### 使い方

    .updating<State>(GestureStateプロパティ(GestureState<State>)) {
        SwiftUIが呼び出すコールバック
    }

    .updating<State>(GestureStateプロパティ(GestureState<State>), body: SwiftUIが呼び出すコールバック)

##### 例

    DragGesture()

#### onChanged

##### 意味

ジェスチャーの値が変化したときに実行するアクションを追加

##### 使い方

    .onChanged { プロパティ(State) in
        実行するアクション
    }

    .onChanged(実行するアクション)

##### 例

    DragGesture()
        .onChanged { _ in
            // アクション
        }

#### onEnded

##### 意味

ジェスチャーの終了時に実行するアクションを追加

##### 使い方

    .onEnded { 値(Self.Value) in
        終了したときに実行するアクション
    }

    .onEnded(終了したときに実行するアクション)

##### 例

    DragGesture()
        .onEnded { _ in
            // アクション
        }

#### simultaneously

##### 意味

別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成

##### 使い方

    .simultaneously(with: 新しい結合されたジェスチャーを作成するためのジェスチャー(Other))

##### 例

    DragGesture()
        .simultaneously(with: DragGesture())

#### sequenced

##### 意味

別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけになる

##### 使い方

    .sequenced(before: 連続した新しいジェスチャーを作成したいジェスチャー(Other))

##### 例

    DragGesture()
        .sequenced(before: DragGesture())

#### exclusively

##### 意味

1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先

##### 使い方

    .exclusively<Other>(before: 新しい組み合わせのジェスチャー(Other))

##### 例

    DragGesture()
        .exclusively(before: DragGesture())

### modifiers

##### 意味

ジェスチャーとキーボードメソッドを組み合わせ

##### 使い方

    .modifiers(ユーザーが押し続ける必要のあるメソッドキーに対応するフラグのセット(EventModifiers))

##### EventModifiersの使い方

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

    DragGesture()
        .modifiers(.all)

#### map

##### 意味

与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー

##### 使い方

    .map(ジェスチャー)

##### 例

    DragGesture()
        .map { _ in
            // ジェスチャー
        }

### 参考サイト

<https://developer.apple.com/documentation/swiftui/draggesture>

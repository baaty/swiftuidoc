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
| .named(AnyHashable) | named          |

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
| modifiers      | ジェスチャーとキーボードメソッドを組み合わせ                                                 |
| map            | 与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー                                    |

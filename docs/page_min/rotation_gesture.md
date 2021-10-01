---
layout: page
---

### 説明

回転動作を認識しその角度を追跡するジェスチャー

### 使い方

    RotationGesture(minimumAngleDelta: 角度(Angle) = .degrees(1))

### 引数の使い方

#### Angle

| 名前               | 説明      |
| ---------------- | ------- |
| .degrees(Double) | 度を指定    |
| .radians(Double) | ラジアンを指定 |

### 例

#### 基本的な使い方

    struct RotationGestureView: View {
        @State var angle = Angle(degrees: 0.0)
        var rotation: some Gesture {
            RotationGesture()
                .onChanged { angle in
                    self.angle = angle
                }
        }
        var body: some View {
            Rectangle()
                .frame(width: 200, height: 200, alignment: .center)
                .rotationEffect(self.angle)
                .gesture(rotation)
        }
    }

### 宣言

    struct RotationGesture

### プロパティ

| 名前                | 型     | 説明                      |
| ----------------- | ----- | ----------------------- |
| minimumAngleDelta | Angle | ジェスチャーが成功するまでに必要な最小のデルタ |

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

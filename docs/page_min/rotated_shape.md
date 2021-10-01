---
layout: page
---

### 説明

回転トランスフォームが適用された図形

### 使い方

    RotatedShape(shape: シェイプ(Content), angle: 角度(Angle), anchor: 開始位置(UnitPoint) = .center)

### 引数の使い方

##### Angleの使い方

| 名前               | 説明      |
| ---------------- | ------- |
| .degrees(Double) | 度を指定    |
| .radians(Double) | ラジアンを指定 |

##### UnitPointの使い方

| 名前                                | 説明         |
| --------------------------------- | ---------- |
| .bottom                           | 下          |
| .bottomLeading                    | 左下         |
| .bottomTrailing                   | 右下         |
| .center                           | 中央        |
| .leading                          | 左          |
| .top                              | 上          |
| .topLeading                       | 左上         |
| .topTrailing                      | 右上         |
| .trailing                         | 右          |
| .zero                             | 0          |
| UnitPoint()                       | 作成         |
| UnitPoint(x: CGFloat, y: CGFloat) | xとyを指定して作成 |

### 例

#### 基本的な使い方

    RotatedShape(shape: Circle(), angle: .degrees(45))

### 宣言

    @frozen struct RotatedShape<Content> where Content : Shape

### プロパティ

| 名前             | 型                                   | 説明              |
| -------------- | ----------------------------------- | --------------- |
| anchor         | UnitPoint                           | 開始位置            |
| angle          | Angle                               | 角度              |
| animatableData | ScaledShape<Content>.AnimatableData | アニメーションするためのデータ |
| shape          | Content                             | 図形              |

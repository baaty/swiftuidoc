---
layout: page
---

### 説明

ユニットポイント

### 使い方

    UnitPoint()

    UnitPoint(x: X値(CGFloat), y: Y値(CGFloat))

### 例

#### 基本的な使い方

    UnitPoint()

### 宣言

    @frozen struct UnitPoint

### プロパティ

| 名前             | 型                        | 説明              |
| -------------- | ------------------------ | --------------- |
| bottom         | UnitPoint                | 下               |
| bottomLeading  | UnitPoint                | 左下              |
| bottomTrailing | UnitPoint                | 右下              |
| center         | UnitPoint                | 真ん中             |
| leading        | UnitPoint                | 左               |
| top            | UnitPoint                | 上               |
| topLeading     | UnitPoint                | 左上              |
| topTrailing    | UnitPoint                | 右上              |
| trailing       | UnitPoint                | 右               |
| zero           | UnitPoint                | 0               |
| animatableData | UnitPoint.AnimatableData | アニメーションするためのデータ |
| hashValue      | Int                      | ハッシュ値           |
| x              | CGFloat                  | X座標             |
| y              | CGFloat                  | Y座標             |

### メソッド

| 名前   | 説明                   |
| ---- | -------------------- |
| hash | 与えられたハッシャーに入力してハッシュ化 |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/unitpoint>

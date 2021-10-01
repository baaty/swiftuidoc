---
layout: page
---

### 説明

幾何学的な角度

### 使い方

#### 引数なしで作成

    Angle()
        .メソッド

#### 角度を指定して作成

    Angle(degrees: 角度(Double))
        .メソッド

#### ラジアンを指定して作成

    Angle(radians: ラジアン(Double))
        .メソッド

### 例

#### 基本的な使い方

    Angle()

#### 角度を指定して作成

    Angle(degrees: 45)

#### ラジアンを指定して作成

    Angle(radians: 0.78)

### 宣言

    @frozen struct Angle

### プロパティ

| 名前 ｜ 型         | 説明     |                 |
| -------------- | ------ | --------------- |
| zero           | Angle  | ゼロ              |
| animatableData | Double | アニメーションするためのデータ |
| degrees        | Double | 度               |
| hashValue      | Int    | ハッシュ値           |
| radians        | Double | ラジアン            |

### メソッド

| 名前      | 説明                   |
| ------- | -------------------- |
| degrees | 度                    |
| radians | ラジアン                 |
| hash    | 与えられたハッシャーに入力してハッシュ化 |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/angle>
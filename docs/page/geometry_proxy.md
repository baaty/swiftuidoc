---
layout: page
---

### 説明

コンテナビューのサイズと座標空間（アンカー解像度用）にアクセスするためのプロキシ

### 使い方

    GeometryProxy()

### 例

#### 基本的な使い方

    let geometryProxy: GeometryProxy

### 宣言

    struct GeometryProxy

### プロパティ

| 名前             | 型          | 説明                   |
| -------------- | ---------- | -------------------- |
| safeAreaInsets | EdgeInsets | コンテナビューのセーフエリアのインセット |
| size           | CGSize     | コンテナビューのサイズ          |

### メソッド

| 名前    | 説明                          |
| ----- | --------------------------- |
| frame | コンテナビューの境界線の矩形を定義された座標空間に変換 |

### メソッド詳細

#### frame

##### 意味

コンテナビューの境界線の矩形を定義された座標空間に変換

##### 使い方

    .frame(in: 座標空間(CoordinateSpace))

##### CoordinateSpaceの使い方

| 名前                  | 説明    |
| ------------------- | ----- |
| .global             | グローバル |
| .local              | ローカル  |
| .named(AnyHashable) |       |

##### 例

    let geometryProxy: GeometryProxy
    geometryProxy.frame(in: .global)

### 参考サイト

<https://developer.apple.com/documentation/swiftui/geometryproxy>

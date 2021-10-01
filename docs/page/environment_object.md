---
layout: page
---

### 説明

親ビューや祖先ビューから提供されるobservableオブジェクトのプロパティラッパータイプ

### 使い方

    EnvironmentObject()
        .メソッド

### 例

#### 基本的な使い方

    @EnvironmentObject var store : Store

### 宣言

    @frozen @propertyWrapper struct EnvironmentObject<ObjectType> where ObjectType : ObservableObject

### プロパティ

| 名前             | 型                                  | 説明                 |
| -------------- | ---------------------------------- | ------------------ |
| wrappedValue   | ObjectType                         | 環境オブジェクトが参照する基本的な値 |
| projectedValue | ObservedObject<ObjectType>.Wrapper | プロパティへのバインディングを作成  |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/environmentobject>

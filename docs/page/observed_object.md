---
layout: page
---

### 説明

外部からのデータを管理するプロパティラッパー

### 使い方

#### 初期値なし

    @ObservedObject var 変数名: 型

#### 初期値あり

    @ObservedObject var 変数名: 型 = 初期値

### 例

#### 基本的な使い方

    @ObservedObject var accessory: Accessory

### 宣言

    @propertyWrapper @frozen struct ObservedObject<ObjectType> where ObjectType : ObservableObject

### プロパティ

| 名前             | 型                                  | 説明                                               |
| -------------- | ---------------------------------- | ------------------------------------------------ |
| wrappedValue   | ObjectType                         | 観測されたオブジェクトが参照する基本的な値                            |
| projectedValue | ObservedObject<ObjectType>.Wrapper | 観測されたオブジェクトの投影で動的なメンバー検索を使用してそのプロパティへのバインディングを作成 |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/observedobject>

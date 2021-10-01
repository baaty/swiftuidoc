---
layout: page
---

### 説明

オブザーバブル・オブジェクトを購読しオブザーバブル・オブジェクトが変更されるとビューを無効にするプロパティ・ラッパー型

### 使い方

#### ラップされた初期値を持つ観測オブジェクトを作成

    ObservedObject(wrappedValue: 初期値(ObjectType))
        .メソッド

#### 初期値を持つ観測オブジェクトを作成

    ObservedObject(initialValue: 初期値(ObjectType))
        .メソッド

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

---
layout: page
---

### 説明

observableオブジェクトをインスタンス化するプロパティラッパー

### 使い方

    @StateObject var 変数名: 型

### 例

#### 基本的な使い方

    @StateObject var hoge : HogeObject = HogeObject()

### 宣言

    @frozen @propertyWrapper struct StateObject&lt;ObjectType&gt; where ObjectType : ObservableObject

### プロパティ

| 名前             | 型                                  | 説明                 |
| -------------- | ---------------------------------- | ------------------ |
| wrappedValue   | ObjectType                         | 環境オブジェクトが参照する基本的な値 |
| projectedValue | ObservedObject&lt;ObjectType&gt;.Wrapper | プロパティへのバインディングを作成  |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/stateobject>

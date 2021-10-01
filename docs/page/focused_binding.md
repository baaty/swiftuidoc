---
layout: page
---

### 説明

フォーカスされたビューまたはその祖先の1つから状態バインディングを観察し自動的にアンラップするための便利なプロパティラッパー

### 使い方

    FocusedBinding(フォーカス値を読み取るためのキーパス(KeyPath<FocusedValues, Binding<Value>?>))

### 例

#### 基本的な使い方

    FocusedBinding<Value>

### 宣言

    @propertyWrapper struct FocusedBinding<Value>

### プロパティ

| 名前             | 型                  | 説明                                             |
| -------------- | ------------------ | ---------------------------------------------- |
| wrappedValue   | Value?             | フォーカスされたビュー階層の現在のスコープと状態を考慮したフォーカスキーのアンラップされた値 |
| projectedValue | Binding&lt;Value?> | オプション値へのバインディング                                |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/focusedbinding>

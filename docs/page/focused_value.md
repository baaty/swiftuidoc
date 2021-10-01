---
layout: page
---

### 説明

フォーカスされたビューまたはその先祖の1つから値を観察するためのプロパティラッパー

### 使い方

    FocusedValue(フォーカス値を読み取るためのキーパス(KeyPath<FocusedValues, Value?>))

### 例

#### 基本的な使い方

    FocusedValue<Value>

### 宣言

    @propertyWrapper struct FocusedValue<Value>

### プロパティ

| 名前           | 型      | 説明                                     |
| ------------ | ------ | -------------------------------------- |
| wrappedValue | Value? | フォーカスされたビュー階層の現在のスコープと状態を考慮したフォーカスキーの値 |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/focusedvalue>

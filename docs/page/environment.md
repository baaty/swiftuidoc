---
layout: page
---

### 説明

ビューの環境から値を読み取るプロパティラッパー

### 使い方

    Environment(キーパス(KeyPath<EnvironmentValues, Value>))
        .メソッド

### 例

#### 基本的な使い方

    @Environment(\.colorScheme) var colorScheme: ColorScheme
    if colorScheme == .dark { // Checks the wrapped value.
        DarkContent()
    } else {
        LightContent()
    }

### 宣言

    @frozen @propertyWrapper struct Environment<Value>

### プロパティ

| 名前           | 型     | 説明           |
| ------------ | ----- | ------------ |
| wrappedValue | Value | 環境プロパティの現在の値 |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/environment>

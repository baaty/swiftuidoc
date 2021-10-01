---
layout: page
---

### 説明

UserDefaultsの値を反映しそのユーザーデフォルトの値が変更されたときにビューを無効にするプロパティのラッパータイプ

### 使い方

#### UserDefaultsを読み書きできるプロパティを作成

    AppStorage("デフォルトストアで値を読み書きするためのキー", store: デフォルトのストア(UserDefaults) = nil)
        .メソッド

#### 文字列ユーザーのデフォルトを読み書きできるプロパティを作成

    AppStorage(wrappedValue: デフォルト値(Value), "デフォルトストアで値を読み書きするためのキー", store: デフォルトのストア(UserDefaults) = nil)
        .メソッド

### 例

#### 基本的な使い方

    AppStorage(wrappedValue: true, "boolean", store:  UserDefaults())

### 宣言

    @frozen @propertyWrapper struct AppStorage<Value>

### プロパティ

| 名前             | 型              | 説明                |
| -------------- | -------------- | ----------------- |
| wrappedValue   | Value          | 基本的な値             |
| projectedValue | Binding<Value> | フォーカスキーのアンラップされた値 |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/appstorage>

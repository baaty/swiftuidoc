---
layout: page
---

### 説明

UserDefaultsの値を反映しそのユーザーデフォルトの値が変更されたときにビューを無効にするプロパティラッパー

### 使い方

#### UserDefaultsを読み書きできるプロパティを作成

    AppStorage("デフォルトストアで値を読み書きするためのキー", store: デフォルトのストア(UserDefaults) = nil)

#### 文字列ユーザーのデフォルトを読み書きできるプロパティを作成

    AppStorage(wrappedValue: デフォルト値(Value), "デフォルトストアで値を読み書きするためのキー", store: デフォルトのストア(UserDefaults) = nil)

### 例

#### 基本的な使い方

    AppStorage(wrappedValue: true, "boolean", store:  UserDefaults())

### 宣言

    @frozen @propertyWrapper struct AppStorage&lt;Value&gt;

### プロパティ

| 名前             | 型              | 説明                |
| -------------- | -------------- | ----------------- |
| wrappedValue   | Value          | 基本的な値             |
| projectedValue | Binding&lt;Value&gt; | フォーカスキーのアンラップされた値 |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

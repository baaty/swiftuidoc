---
layout: page
---

### 説明

シーンごとの永続的なストレージに読み書きするプロパティラッパー

### 使い方

#### 任意の文字列を保存・復元できるプロパティを作成

    SceneStorage("値の保存と復元に使用されるキー")

#### URLの保存・復元が可能なプロパティを作成

    SceneStorage(wrappedValue: デフォルト値(Value), "値の保存と復元に使用されるキー")

### 例

#### 基本的な使い方

    @SceneStorage("hoge") var hoge = ""

### 宣言

    @frozen @propertyWrapper struct SceneStorage<Value>

### プロパティ

| 名前             | 型              | 説明                |
| -------------- | -------------- | ----------------- |
| wrappedValue   | Value          | 基本的な値             |
| projectedValue | Binding<Value> | フォーカスキーのアンラップされた値 |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

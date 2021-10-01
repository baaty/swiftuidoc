---
layout: page
---

### 説明

AppKitからのデリゲートを提供するためにAppで使用されるプロパティラッパー

### 使い方

    NSApplicationDelegateAdaptor(使用するNSApplicationDelegateのタイプ(DelegateType.Type) = DelegateType.self)

### 例

#### 基本的な使い方

    @NSApplicationDelegateAdaptor var 変数名: 型

### 例

#### 基本的な使い方

    @NSApplicationDelegateAdaptor var appDelegate: AppDelegate

### 宣言

    @propertyWrapper struct NSApplicationDelegateAdaptor<DelegateType> where DelegateType : NSObject, DelegateType : NSApplicationDelegate

### プロパティ

| 名前             | 型                                    | 説明                                               |
| -------------- | ------------------------------------ | ------------------------------------------------ |
| projectedValue | ObservedObject<DelegateType>.Wrapper | 観測されたオブジェクトの投影で動的なメンバー検索を使用してそのプロパティへのバインディングを作成 |
| wrappedValue   | DelegateType                         | 基礎となるデレゲート                                       |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

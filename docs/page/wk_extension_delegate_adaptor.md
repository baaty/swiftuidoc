---
layout: page
---

### 説明

WatchKitからのデリゲートを提供するためにAppで使用されるプロパティラッパー

### 使い方

    WKExtensionDelegateAdaptor(WKExtensionDelegateのタイプ(DelegateType.Type) = DelegateType.self)

### 例

#### 基本的な使い方

    @WKExtensionDelegateAdaptor(ExtensionDelegate.self) var extensionDelegate

### 宣言

    @propertyWrapper struct WKExtensionDelegateAdaptor&lt;DelegateType&gt; where DelegateType : NSObject, DelegateType : WKExtensionDelegate

### プロパティ

| 名前             | 型                                    | 説明                                               |
| -------------- | ------------------------------------ | ------------------------------------------------ |
| projectedValue | ObservedObject&lt;DelegateType&gt;.Wrapper | 観測されたオブジェクトの投影で動的なメンバー検索を使用してそのプロパティへのバインディングを作成 |
| wrappedValue   | DelegateType                         | 基礎となるデレゲート                                       |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/wkextensiondelegateadaptor>

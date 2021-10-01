---
layout: page
---

### 説明

WatchKitからのデリゲートを提供するためにAppで使用されるプロパティ・ラッパー

### 使い方

    WKExtensionDelegateAdaptor(WKExtensionDelegateのタイプ(DelegateType.Type) = DelegateType.self)
        .メソッド

### 例

#### 基本的な使い方

    @WKExtensionDelegateAdaptor(ExtensionDelegate.self) var extensionDelegate

### 宣言

    @propertyWrapper struct WKExtensionDelegateAdaptor<DelegateType> where DelegateType : NSObject, DelegateType : WKExtensionDelegate

### プロパティ

| 名前             | 型                                    | 説明                                               |
| -------------- | ------------------------------------ | ------------------------------------------------ |
| projectedValue | ObservedObject<DelegateType>.Wrapper | 観測されたオブジェクトの投影で動的なメンバー検索を使用してそのプロパティへのバインディングを作成 |
| wrappedValue   | DelegateType                         | 基礎となるデレゲート                                       |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/wkextensiondelegateadaptor>
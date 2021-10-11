---
layout: page
---

### 説明

UIKitからのデリゲートを提供するためにAppで使用されるプロパティラッパー

### 使い方

    UIApplicationDelegateAdaptor(UIApplicationDelegateのタイプ(DelegateType.Type) = DelegateType.self)

### 例

#### 基本的な使い方

    @UIApplicationDelegateAdaptor(AppDelegate.self) var appDelegate

### 宣言

    @propertyWrapper struct UIApplicationDelegateAdaptor&lt;DelegateType&gt; where DelegateType : NSObject, DelegateType : UIApplicationDelegate

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

<https://developer.apple.com/documentation/swiftui/uiapplicationdelegateadaptor>

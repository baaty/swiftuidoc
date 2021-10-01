---
layout: page
---

### 説明

UIKitからのデリゲートを提供するためにAppで使用されるプロパティ・ラッパー

### 使い方

    UIApplicationDelegateAdaptor(UIApplicationDelegateのタイプ(DelegateType.Type) = DelegateType.self)
        .メソッド

### 例

#### 基本的な使い方

    @UIApplicationDelegateAdaptor(AppDelegate.self) var appDelegate

### 宣言

    @propertyWrapper struct UIApplicationDelegateAdaptor<DelegateType> where DelegateType : NSObject, DelegateType : UIApplicationDelegate

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

<https://developer.apple.com/documentation/swiftui/uiapplicationdelegateadaptor>

---
layout: page
---

### 説明

SwiftUIのビュー階層をホストするAppKitのビューコントローラークラス

### 使い方

#### 指定されたSwiftUIビューをラップするホスティングコントローラオブジェクトを作成

    NSHostingController {
        ルートビュー(Content)
    }

    NSHostingController(rootView: ルートビュー(Content))

#### アーカイブと指定されたSwiftUIビューからホスティングコントローラオブジェクトを作成

    NSHostingController(coder: 初期化時に使用するデコーダ(NSCoder)) {
        ルートビュー(Content)
    }

    NSHostingController(coder: 初期化時に使用するデコーダ(NSCoder), rootView: ルートビュー(Content))

#### 指定されたnibファイルの内容からホスティングコントローラオブジェクトを作成

    NSHostingController(nibName: nibファイルの名前(NSNib.Name)?, bundle: nibファイルを検索するバンドル(Bundle)?)

#### 指定されたアーカイブのコンテンツからホスティングコントローラオブジェクトを作成

    NSHostingController(coder: 初期化時に使用するデコーダー(NSCoder))

### 例

#### 基本的な使い方

    NSHostingController()

### プロパティ

| 名前         | 型                              | 説明     |
| ---------- | ------------------------------ | ------ |
| rootView   | Content                        | ルートビュー |
| identifier | NSUserInterfaceItemIdentifier? | 識別子    |

### メソッド

| 名前           | 説明          |
| ------------ | ----------- |
| sizeThatFits | 最も適したサイズを計算 |

### メソッド詳細

#### sizeThatFits

##### 意味

最も適したサイズを計算

##### 使い方

    .sizeThatFits(in: 新しいサイズ(CGSize))

##### CGSizeの使い方

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

##### 例

    NSHostingController()
        .sizeThatFits(in: CGSize())

### 宣言

    class NSHostingController&lt;Content&gt; where Content : View

### 参考サイト

<https://developer.apple.com/documentation/swiftui/nshostingcontroller>

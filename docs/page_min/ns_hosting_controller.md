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

---
layout: page
---

### 説明

SwiftUIのビュー階層を管理するUIKitのビューコントローラー

### 使い方

#### 指定されたSwiftUIビューをラップするホスティングコントローラオブジェクトを作成

    UIHostingController(rootView: ルートビュー(Content))
        .メソッド

#### アーカイブと指定されたSwiftUIビューからホスティングコントローラオブジェクトを作成

    UIHostingController(coder: 初期化時に使用するデコーダー(NSCoder), rootView: ルートビュー(Content))
        .メソッド

#### 指定されたnibファイルの内容からホスティングコントローラオブジェクトを作成

    UIHostingController(nibName: UIKitのビューコントローラーを含むnibファイル名(String)?, bundle: nibファイルを検索するバンドル(Bundle)?)
        .メソッド

#### 指定されたアーカイブのコンテンツからホスティングコントローラオブジェクトを作成

    UIHostingController(coder: 初期化時に使用するデコーダー(NSCoder))
        .メソッド

### 宣言

    class UIHostingController<Content> where Content : View

### プロパティ

| 名前                                | 型                    | 説明                                               |
| --------------------------------- | -------------------- | ------------------------------------------------ |
| rootView                          | Content              | ルートビュー                                           |
| preferredStatusBarStyle           | UIStatusBarStyle     | ビューコントローラのステータスバーのスタイルを指定                        |
| preferredStatusBarUpdateAnimation | UIStatusBarAnimation | このビューコントローラのステータスバーを隠したり表示したりする際に使用するアニメーションスタイル |
| prefersStatusBarHidden            | Bool                 | ビューコントローラがステータスバーを隠すか                            |
| childForStatusBarHidden           | UIViewController?    |                                                  |
| preferredUserInterfaceStyle       | UIUserInterfaceStyle | このビューコントローラの優先インターフェーススタイル                       |
| keyCommands                       | [UIKeyCommand]?      |                                                  |

### メソッド

| 名前                            | 説明                                     |
| ----------------------------- | -------------------------------------- |
| loadView                      |                                        |
| viewWillAppear                | ビューコントローラにそのビューがビュー階層に追加されようとしていることを通知 |
| viewDidAppear                 | ビューコントローラにそのビューがビュー階層に追加されたことを通知       |
| viewWillDisappear             | ビューコントローラにそのビューがビュー階層から削除されることを通知      |
| preferredContentSizeDidChange |                                        |
| willMove                      |                                        |
| didMove                       |                                        |
| viewWillTransition            |                                        |
| viewWillLayoutSubviews        |                                        |
| target                        |                                        |
| sizeThatFits                  | 現在のビューに最も適したサイズを計算                     |

### 例

#### 基本的な使い方

    UIHostingController(rootView: HomeView())

### 参考サイト

<https://developer.apple.com/documentation/swiftui/uihostingcontroller>

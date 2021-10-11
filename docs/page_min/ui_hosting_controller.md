---
layout: page
---

### 説明

SwiftUIのビュー階層を管理するUIKitのビューコントローラークラス

### 使い方

#### 指定されたSwiftUIビューをラップするホスティングコントローラオブジェクトを作成

    UIHostingController(rootView: ルートビュー(Content))

#### アーカイブと指定されたSwiftUIビューからホスティングコントローラオブジェクトを作成

    UIHostingController(coder: 初期化時に使用するデコーダー(NSCoder), rootView: ルートビュー(Content))

#### 指定されたnibファイルの内容からホスティングコントローラオブジェクトを作成

    UIHostingController(nibName: UIKitのビューコントローラーを含むnibファイル名(String)?, bundle: nibファイルを検索するバンドル(Bundle)?)

#### 指定されたアーカイブのコンテンツからホスティングコントローラオブジェクトを作成

    UIHostingController(coder: 初期化時に使用するデコーダー(NSCoder))

### 例

#### 基本的な使い方

    UIHostingController(rootView: HomeView())

### 宣言

    class UIHostingController&lt;Content&gt; where Content : View

### プロパティ

| 名前                                | 型                    | 説明                                               |
| --------------------------------- | -------------------- | ------------------------------------------------ |
| rootView                          | Content              | ルートビュー                                           |
| preferredStatusBarStyle           | UIStatusBarStyle     | ビューコントローラのステータスバーのスタイルを指定                        |
| preferredStatusBarUpdateAnimation | UIStatusBarAnimation | このビューコントローラのステータスバーを隠したり表示したりする際に使用するアニメーションスタイル |
| prefersStatusBarHidden            | Bool                 | ビューコントローラがステータスバーを隠すか                            |
| childForStatusBarHidden           | UIViewController?    | ステータスバーを隠すための子ビュー                                |
| preferredUserInterfaceStyle       | UIUserInterfaceStyle | このビューコントローラの優先インターフェーススタイル                       |
| keyCommands                       | [UIKeyCommand]?      | キーコマンド                                           |

### メソッド

| 名前                            | 説明                       |
| ----------------------------- | ------------------------ |
| loadView                      | ビューをロード                  |
| viewWillAppear                | ビュー階層に追加されようとしていることを通知   |
| viewDidAppear                 | ビュー階層に追加されたことを通知         |
| viewWillDisappear             | ビュー階層から削除されることを通知        |
| preferredContentSizeDidChange | コンテンスサイズの変化              |
| willMove                      | 変更されようとしていることを通知         |
| didMove                       | 追加された後、または削除された後に通知      |
| viewWillTransition            | サイズが変更されようとしているときに通知     |
| viewWillLayoutSubviews        | サブビューをレイアウトしようとしていることを通知 |
| target                        | アクションに反応するビューコントローラー     |
| sizeThatFits                  | 現在のビューに最も適したサイズを計算       |

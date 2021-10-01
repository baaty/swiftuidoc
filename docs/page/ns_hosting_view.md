---
layout: page
---

### 説明

SwiftUIのビュー階層をホストするAppKitビュークラス

### 使い方

#### 指定されたSwiftUIビューをラップするホスティングビューオブジェクトを作成

    NSHostingView(rootView: ルートビュー(Content))

#### 指定されたアーカイブのコンテンツから、ホスティングビューオブジェクトを作成

    NSHostingView(coder: 初期化時に使用するデコーダー(NSCoder))

#### 指定されたフレーム矩形を持つ新しく割り当てられたAppKitビューを初期化

    NSHostingView(frame: 新しいビュー・オブジェクトのフレーム矩形を指定(NSRect))

### 例

#### 基本的な使い方

    NSHostingView(rootView: contentView)

### 宣言

    class NSHostingView<Content> where Content : View

### プロパティ

| 名前                            | 型                                | 説明                                         |
| ----------------------------- | -------------------------------- | ------------------------------------------ |
| rootView                      | Content                          | ルートビュー                                     |
| userInterfaceLayoutDirection  | NSUserInterfaceLayoutDirection   | レイアウト方向を指定                                 |
| isFlipped                     | Bool                             | ビューが反転した座標系を使用するか                          |
| layerContentsRedrawPolicy     | NSView.LayerContentsRedrawPolicy | ビューのレイヤーのコンテンツ再描画のポリシー                     |
| acceptsFirstResponder         | Bool                             | ファーストレスポンダのステータスを受け入れるか                    |
| canBecomeKeyView              | Bool                             | キービューになれるか                                 |
| needsPanelToBecomeKey         | Bool                             | キーボード入力やナビゲーションを処理する前にパネルをキーウィンドウにする必要があるか |
| intrinsicContentSize          | NSSize                           | 受信したビューの自然なサイズでビュー自体の特性のみを考慮               |
| firstBaselineOffsetFromTop    | CGFloat                          | ビューの位置合わせ用の長方形の頂点とその最上部のベースラインとの間の距離       |
| lastBaselineOffsetFromBottom  | CGFloat                          | ビューの位置合わせ用の長方形の底辺と最下部のベースラインとの間の距離         |
| accessibilityFocusedUIElement | Any?                             | フォーカスを持つアクセシビリティ階層の最深部の子孫                  |

### メソッド

| 名前                               | 説明                                                              |
| -------------------------------- | --------------------------------------------------------------- |
| updateConstraints                | ビューの制約条件を更新                                                     |
| layout                           | 制約条件付きレイアウトシステムと協調してレイアウト                                       |
| mouseDown                        | マウスの左ボタンを押したことを通知                                               |
| mouseUp                          | マウスの左ボタンを離したことを通知                                               |
| otherMouseDown                   | 左右以外のマウスボタンを押したことを通知                                            |
| otherMouseUp                     | 左右以外のマウスボタンを離したことを通知                                            |
| rightMouseDown                   | マウスの右ボタンを押したことを通知                                               |
| rightMouseUp                     | マウスの右ボタンを離したことを通知                                               |
| mouseEntered                     | カーソルがトラッキング用の矩形に入ったことを通知                                        |
| mouseExited                      | カーソルがトラッキング用の矩形から外れたことを通知                                       |
| mouseDragged                     | 左ボタンを押しながらマウスを動かしたことを通知                                         |
| otherMouseDragged                | 左右以外のボタンを押してマウスを動かしたことを通知                                       |
| rightMouseDragged                | 右ボタンを押しながらマウスを動かしたことを通知                                         |
| touchesBegan                     | ビューやウィンドウで1つ以上の新しいタッチが発生したことを通知                                 |
| touchesCancelled                 | システムイベントによりタッチシーケンスがキャンセルされた場合に通知                               |
| touchesEnded                     | 景色や窓から1本以上の指が上がったときに通知                                          |
| touchesMoved                     | 関連するビューで1本以上の指が動いたときに通知                                         |
| magnify                          | マグニファイジェスチャーイベント用のマスク                                           |
| rotate                           | ローテートジェスチャーイベント用のマスク                                            |
| scrollWheel                      | マウスのスクロールホイールが移動したことを通知                                         |
| draggingSession                  | 画面上でドラッグが動いたときに呼び出される                                           |
| menu                             | サブクラスによってオーバーライドされ与えられたマウスダウンイベントに対するコンテキスト依存のポップアップメニュー        |
| responds                         | 指定されたセレクタに応答するか                                                 |
| forwardingTarget                 | 認識されなかったメッセージが最初に指示されるべきオブジェクト                                  |
| viewWillMove                     | スーパービューが指定されたスーパービューに変更されようとしていることを通知                           |
| viewDidMoveToWindow              | 新しいビュー階層に追加されたことをビューに通知                                         |
| viewDidMoveToSuperview           | スーパービューが変更されたことをビューに通知                                          |
| viewDidChangeBackingProperties   | ビューのバッキングストアのプロパティが変更されたときに応答                                   |
| viewDidChangeEffectiveAppearance | 外観モードのプロパティが変更されたときに応答                                          |
| renewGState                      | ビューのグラフィックス・ステート・オブジェクトがある場合それを無効                               |
| setFrameSize                     | ビューのフレーム矩形のサイズを指定された寸法に設定しスーパービューの座標系に影響を与えることなくスーパービュー内でサイズを変更 |
| hitTest                          | 指定された点を含むビュー階層の最も遠い子孫                                           |
| accessibilityChildren            | アクセシビリティー階層の子アクセシビリティー要素                                        |
| accessibilityHitTest             | 指定されたポイントを含むアクセシビリティ階層の最深部の子孫                                   |
| validateUserInterfaceItem        | 有効にするかどうか                                                       |
| observeValue                     | 指定されたキーパスの値が変更された場合観察対象のオブジェクトに通知                               |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/nshostingview>

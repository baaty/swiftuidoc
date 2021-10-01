---
layout: page
---

### 説明

SwiftUIのビュー階層をホストするAppKitビュー

### 使い方

#### 指定されたSwiftUIビューをラップするホスティングビューオブジェクトを作成

    NSHostingView(rootView: ルートビュー(Content))
        .メソッド

#### 指定されたアーカイブのコンテンツから、ホスティングビューオブジェクトを作成

    NSHostingView(coder: 初期化時に使用するデコーダー(NSCoder))
        .メソッド

#### 指定されたフレーム矩形を持つ新しく割り当てられたAppKitビューを初期化

    NSHostingView(frame: 新しいビュー・オブジェクトのフレーム矩形を指定(NSRect))
        .メソッド

### 例

#### 基本的な使い方

    NSHostingView(rootView: contentView)

### 宣言

    class NSHostingView<Content> where Content : View

### プロパティ

| 名前                            | 型                                | 説明     |
| ----------------------------- | -------------------------------- | ------ |
| rootView                      | Content                          | ルートビュー |
| userInterfaceLayoutDirection  | NSUserInterfaceLayoutDirection   |        |
| isFlipped                     | Bool                             |        |
| layerContentsRedrawPolicy     | NSView.LayerContentsRedrawPolicy |        |
| acceptsFirstResponder         | Bool                             |        |
| canBecomeKeyView              | Bool                             |        |
| needsPanelToBecomeKey         | Bool                             |        |
| intrinsicContentSize          | NSSize                           |        |
| firstBaselineOffsetFromTop    | CGFloat                          |        |
| lastBaselineOffsetFromBottom  | CGFloat                          |        |
| accessibilityFocusedUIElement | Any?                             |        |

### メソッド

| 名前                               | 説明  |
| -------------------------------- | --- |
| updateConstraints                |     |
| layout                           |     |
| mouseDown                        |     |
| mouseUp                          |     |
| otherMouseDown                   |     |
| otherMouseUp                     |     |
| rightMouseDown                   |     |
| rightMouseUp                     |     |
| mouseEntered                     |     |
| mouseExited                      |     |
| mouseDragged                     |     |
| otherMouseDragged                |     |
| rightMouseDragged                |     |
| touchesBegan                     |     |
| touchesCancelled                 |     |
| touchesEnded                     |     |
| touchesMoved                     |     |
| magnify                          |     |
| rotate                           |     |
| scrollWheel                      |     |
| draggingSession                  |     |
| menu                             |     |
| responds                         |     |
| forwardingTarget                 |     |
| viewWillMove                     |     |
| viewDidMoveToWindow              |     |
| viewDidMoveToSuperview           |     |
| viewDidChangeBackingProperties   |     |
| viewDidChangeEffectiveAppearance |     |
| renewGState                      |     |
| setFrameSize                     |     |
| hitTest                          |     |
| accessibilityChildren            |     |
| accessibilityHitTest             |     |
| validateUserInterfaceItem        |     |
| observeValue                     |     |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/nshostingview>

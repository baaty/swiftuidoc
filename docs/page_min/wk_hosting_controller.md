---
layout: page
---

### 説明

SwiftUIのビュー階層をホストするWatchKitインターフェースコントローラクラス

### 使い方

    WKHostingController()

### 例

#### 基本的な使い方

    class HostingController: WKHostingController<ContentView> {
        override var body: ContentView {
            return ContentView()
        }
    }

### 宣言

    class WKHostingController<Body> where Body : View

### プロパティ

| 名前   | 型    | 説明                              |
| ---- | ---- | ------------------------------- |
| body | Body | インターフェイスコントローラに表示するビュー階層のルートビュー |

### メソッド

| 名前                 | 説明                                       |
| ------------------ | ---------------------------------------- |
| updateBodyIfNeeded | 更新が保留されている場合インターフェイスコントローラのビューのセットを直ちに更新 |
| setNeedsBodyUpdate | 現在のSwiftUIのビューを無効にし次のサイクルで更新を開始          |

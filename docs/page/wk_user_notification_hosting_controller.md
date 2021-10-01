---
layout: page
---

### 説明

SwiftUIのビュー階層をホストするWatchKitのユーザー通知インターフェースコントローラクラス

### 使い方

    WKUserNotificationHostingController()

### 例

#### 基本的な使い方

    class NotificationController: WKUserNotificationHostingController<NotificationView> {
        override var body: NotificationView {
            return NotificationView()
        }
    }

### 宣言

    class WKUserNotificationHostingController<Body> where Body : View

### 参考サイト

<https://developer.apple.com/documentation/swiftui/wkusernotificationhostingcontroller>

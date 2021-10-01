---
layout: page
---

### 説明

ストロークスタイル

### 使い方

    StrokeStyle(lineWidth: 幅(CGFloat) = 1, lineCap: ラインキャップ(CGLineCap) = .butt, lineJoin: ラインジョイン(CGLineJoin) = .miter, miterLimit: マイターリミット(CGFloat) = 10, dash: ダッシュ([CGFloat]) = [CGFloat](), dashPhase: ダッシュケース(CGFloat) = 0)

### 例

#### 基本的な使い方

    StrokeStyle()

### 宣言

    @frozen struct StrokeStyle

### プロパティ

| 名前             | 型                          | 説明              |
| -------------- | -------------------------- | --------------- |
| animatableData | StrokeStyle.AnimatableData | アニメーションするためのデータ |
| dash           | [CGFloat]                  | ダッシュ            |
| dashPhase      | CGFloat                    | ダッシュケース         |
| lineCap        | CGLineCap                  | ラインキャップ         |
| lineJoin       | CGLineJoin                 | ラインジョイン         |
| lineWidth      | CGFloat                    | 幅               |
| miterLimit     | CGFloat                    | マイターリミット        |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/strokestyle>

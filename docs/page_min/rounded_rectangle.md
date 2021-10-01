---
layout: page
---

### 説明

角の丸い長方形でそれを含むビューのフレーム内に配置

### 使い方

    RoundedRectangle(cornerRadius: 半径(CGFloat), style: スタイル(RoundedCornerStyle) = .circular)

    RoundedRectangle(cornerSize: サイズ(CGSize), style: スタイル(RoundedCornerStyle) = .circular)

### 例

#### 基本的な使い方

    RoundedRectangle(cornerSize: CGSize())

### 宣言

    @frozen struct RoundedRectangle

### プロパティ

| 名前             | 型                     | 説明              |
| -------------- | --------------------- | --------------- |
| animatableData | CGSize.AnimatableData | アニメーションするためのデータ |
| cornerSize     | CGSize                | コーナーサイズ         |
| style          | RoundedCornerStyle    | スタイル            |

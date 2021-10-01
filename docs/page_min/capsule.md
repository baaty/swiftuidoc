---
layout: page
---

### 説明

カプセル形状を描画

### 使い方

    Capsule(style: コーナータイプを指定(RoundedCornerStyle) = .circular)

### 引数の使い方

#### RoundedCornerStyle

| 名前          | 説明               |
| ----------- | ---------------- |
| .circular   | 1/4円の丸みを帯びた長方形の角 |
| .continuous | 連続した曲面が角を丸く      |

### 例

#### 基本的な使い方

    Capsule()

### 宣言

    @frozen struct Capsule

### プロパティ

| 名前             | 型                   | 説明              |
| -------------- | ------------------- | --------------- |
| animatableData | EmptyAnimatableData | アニメーションするためのデータ |
| style          | RoundedCornerStyle  | スタイル            |

---
layout: page
---

### 説明

プレビューを実行するシミュレータデバイス

### 使い方

#### 与えられた値で初期化されたインスタンスを作成し

    PreviewDevice(extendedGraphemeClusterLiteral: 新しいインスタンスの値(Self.StringLiteralType))

#### 与えられた値で初期化されたインスタンスを作成

    PreviewDevice(unicodeScalarLiteral: 新しいインスタンスの値(Self.ExtendedGraphemeClusterLiteralType))

#### 与えられた文字列の値で初期化されたインスタンスを作成

    PreviewDevice(stringLiteral: 新しいインスタンスの値(String))

#### 指定された生の値を持つ新しいインスタンスを作成

    PreviewDevice(rawValue: 新しいインスタンスに使用する生の値(String))

### 例

#### 基本的な使い方

    PreviewDevice(rawValue: "hoge")

### 宣言

    struct PreviewDevice

### プロパティ

| 名前       | 型      | 説明         |
| -------- | ------ | ---------- |
| rawValue | String | 生タイプの対応する値 |

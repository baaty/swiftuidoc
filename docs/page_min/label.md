---
layout: page
---

### 説明

ラベルは画像とテキストを並べて表示するビュー

### 使い方

#### アイコンのイメージと文字列から生成されるタイトルを持つラベルを作成

    Label(ラベルのタイトル(StringProtocol), image: 画像名(String))

#### アイコンのイメージとローカライズされた文字列から生成されたタイトルを持つラベルを作成

    Label(ローカライズされた文字列キー(LocalizedStringKey), image: 画像名(String))

#### システムアイコンのイメージとローカライズされた文字列から生成されたタイトルを持つラベルを作成

    Label(ローカライズされた文字列キー(LocalizedStringKey), systemImage: 画像名(String))

#### システムアイコンの画像と文字列から生成されたタイトルを持つラベルを作成

    Label(ラベルのタイトル(StringProtocol), systemImage: 画像名(String))

#### カスタムのタイトルとアイコンを持つラベルを作成

    Label(title: {
        ラベルのタイトル(Title)
    }) {
        アイコン(Icon)
    }

    Label(title: ラベルのタイトル, icon: アイコン)

#### スタイルの構成を表すラベルを作成

    Label(ラベルのスタイル(LabelStyleConfiguration))

### 例

#### ラベルとアイコン

    Label("アイコン付きラベル", systemImage: "bolt.fill")

#### ラベルと画像

    Label("画像付きラベル", image: "hoge")

#### 色付きアイコン

    Label("色付きアイコンラベル", systemImage: "bolt.fill")
        .listItemTint(.yellow)

#### 背景の色を変える

    Label("色付きアイコンラベル", systemImage: "bolt.fill")

### 宣言

    struct Label<Title, Icon> where Title : View, Icon : View

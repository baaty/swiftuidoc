---
layout: page
---

### 説明

タブを使用して複数の子ビューを切り替えることができるコンテナビュー

### 使い方

#### 基本的な使い方

    TabView() {
        コンテンツ
    }

    TabView(content: コンテンツ)

#### Selectionの値に関連付けられたコンテンツを選択するインスタンスを作成

    TabView(selection: $タブの状態変数(Binding<SelectionValue>)?) {
        コンテンツ
    }

    TabView(selection: $タブの状態変数(Binding<SelectionValue>)?, content: コンテンツ)

### 例

#### 基本的な使い方

    TabView {
        Text("First View")
            .tabItem({ Text("First") })
        Text("Second View")
            .tabItem({ Text("Second") })
    }

### 宣言

    struct TabView<SelectionValue, Content> where SelectionValue : Hashable, Content : View

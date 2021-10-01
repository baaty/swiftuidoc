---
layout: page
---

### 説明

スクロールを制御するための機能を提供するビュー

### 使い方

    ScrollViewReader { 引数(ScrollViewProxy) in
        コンテンツ(Content)
    }

    ScrollViewReader(content: コンテンツ)

### 引数の使い方

| 名前 | 説明 |
|-----|------|
| ScrollViewProxy.scrollTo(_ id: ID, anchor: UnitPoint? = nil) | 識別子を持つ子ビューまでスクロール |


### 例

#### ボタンでスクロール

    ScrollViewReader { scrollViewProxy in
        Button("一番下に移動") {
            scrollViewProxy.scrollTo(20)
        }
        ScrollView {
            ForEach(1..<21) { index in
                Text(index)
            }
        }
        Button("一番上に移動") {
            scrollViewProxy.scrollTo(1)
        }
    }

#### 指定したアンカーまでスクロール

    ScrollViewReader { scrollViewProxy in
        Button("一番下に移動") {
            scrollViewProxy.scrollTo(20, anchor: .top)
        }
        ScrollView {
            ForEach(1..<21) { index in
                Text(index)
            }
        }
        Button("一番上に移動") {
            scrollViewProxy.scrollTo(20, anchor: .bottom)
        }
    }

#### アニメーションあり

    ScrollViewReader { scrollViewProxy in
        Button("一番下に移動") {
            withAnimation { scrollViewProxy.scrollTo(20) }
        }
        ScrollView {
            ForEach(1..<21) { index in
                Text(index)
            }
        }
        Button("一番上に移動") {
            withAnimation { scrollViewProxy.scrollTo(1) }
        }
    }

### 宣言

    @frozen struct ScrollViewReader<Content> where Content : View

### プロパティ

| 名前      | 型       | 説明                  |
| ------- | ------- | ------------------- |
| content | Content | 読者のコンテンツを作るビュー・ビルダー |

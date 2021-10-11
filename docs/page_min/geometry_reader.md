---
layout: page
---

### 説明

子ビューのサイズや位置を取得するコンテンツを定義するコンテナビュー

### 使い方

    GeometryReader(content: コンテンツ)

### 例

#### 基本的な使い方

    GeometryReader {
        // 子ビュー
    }

#### 子ビューのサイズを取得

    GeometryReader { geometryProxy in
        VStack(spacing: 24) {
            Text("幅: \(geometryProxy.size.width)")
            Text("高さ: \(geometryProxy.size.height)")
        }
    }

#### 子ビューの位置を指定

    GeometryReader { geometryProxy in
        VStack(spacing: 24) {
            Text("位置")
                .position(x: geometryProxy.size.width/5, y: geometryProxy.size.height/5)
        }
    }

### 宣言

    @frozen struct GeometryReader&lt;Content&gt; where Content : View

### プロパティ

| 名前      | 型                          | 説明    |
| ------- | -------------------------- | ----- |
| content | (GeometryProxy) -> Content | コンテンツ |

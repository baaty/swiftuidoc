---
layout: page
---

### 説明

伸縮するスペースを作るビュー

### 使い方

    Spacer(minLength: 最小幅(CGFloat) = nil)

### 例

#### 基本的な使い方

    HStack {
        Image(systemName: "clock")
        Spacer()
        Text("Time")
    }

#### 最小幅を指定

    HStack {
        Image(systemName: "clock")
        Spacer(minLength: 0)
        Text("Time")
    }

#### 均等に配置

    HStack {
        Spacer()
        Text("中央にテキスト")
        Spacer()
    }

#### 幅を指定

    HStack {
        Image(systemName: "clock")
        Spacer()
            .frame(width: 8)
        Text("Time")
    }

### 宣言

    @frozen struct Spacer

### プロパティ

| 名前        | 型       | 説明       |
| --------- | ------- | -------- |
| minLength | CGFloat | 縮小できる最小幅 |

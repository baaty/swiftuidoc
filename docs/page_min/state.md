---
layout: page
---

### 説明

SwiftUIで管理されている値を他のビューと双方向で読み書きできるプロパティラッパー

### 使い方

#### 初期値のない状態を作成

    @State var 変数名: 型

    State()

#### 初期値を持つ状態を作成

    @State var 変数名: 型 = 初期値

    State(initialValue: 初期値(Value))

#### ラップされた初期値を持つステートを作成

    State(wrappedValue: 初期のラップドバリュー(Value))

### 例

#### 基本的な使い方

    struct PlayerView: View {
        var episode: Episode
        @State private var isPlaying: Bool = false
        var body: some View {
            VStack {
                Text(episode.title)
                Text(episode.showTitle)
                PlayButton(isPlaying: $isPlaying)
            }
        }
    }

### 宣言

    @frozen @propertyWrapper struct State&lt;Value&gt;

### プロパティ

| 名前             | 型              | 説明               |
| -------------- | -------------- | ---------------- |
| wrappedValue   | Value          | ステート変数が参照する基礎的な値 |
| projectedValue | Binding&lt;Value&gt; | 状態の値へのバインディング    |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

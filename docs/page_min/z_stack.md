---
layout: page
---

### 説明

子ビューを重ねて配置するコンテナビュー

### 使い方

    ZStack(alignment: 配置(Alignment) = .center) {
        コンテンツ(Content)
    }

    ZStack(alignment: 配置(Alignment) = .center, content: コンテンツ)

#### 引数の使い方

##### Alignment

| 名前              | 説明   |
| --------------- | ---- |
| .bottom         | 下寄せ  |
| .bottomLeading  | 左下寄せ |
| .bottomTrailing | 右下寄せ |
| .center         | 中央寄せ |
| .leading        | 左寄せ  |
| .top            | 上寄せ  |
| .topLeading     | 左上寄せ |
| .topTrailing    | 右寄せ上 |
| .trailing       | 右寄せ  |

### 例

#### 基本的な使い方

    ZStack {
        Color.yellow
        Text("テキスト")
    }

#### 右下に寄せる

    ZStack(alignment: .bottomTrailing) {
        Color.yellow
        Text("テキスト")
    }

#### 画像にテキストを重ねる

    ZStack {
        Image("hoge")
            .resizable()
            .scaledToFit()
        Rectangle()
            .fill(Color.white.opacity(0.8))
            .frame(maxWidth: .infinity, maxHeight: 40)
        Text("重ねるテキスト")
    }

#### セーフエリアのエッジを無視

    ZStack(alignment: .bottomLeading) {
        Color.yellow
            .ignoresSafeArea()
        Text("テキスト")
    }

### 宣言

    @frozen struct ZStack&lt;Content&gt; where Content : View

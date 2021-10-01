---
layout: page
---

### 説明

値を他のビューと双方向で読み書きできるプロパティラッパー

### 使い方

#### 作成

    @Binding var 変数名: 型

#### バインディング値からの読み込みを行うクロージャとバインディング値への書き込み時にトランザクションを適用するクロージャを持つバインディングを作成

    Binding(
        get: {
            バインディングの値を取得するためのクロージャー
        }, set: {
            バインディング値を設定するためのクロージャー
        }
    )

### 例

#### 基本的な使い方

    struct PlayButton: View {
        @Binding var isPlaying: Bool
        var body: some View {
            Button(action: {
                self.isPlaying.toggle()
            }) {
                Image(systemName: isPlaying ? "pause.circle" : "play.circle")
            }
        }
    }

### 宣言

    @frozen @propertyWrapper @dynamicMemberLookup struct Binding<Value>

### プロパティ

| 名前             | 型              | 説明                  |
| -------------- | -------------- | ------------------- |
| wrappedValue   | Value          | バインディング変数が参照する基本的な値 |
| projectedValue | Binding<Value> | バインディング値の投影でバインディング |
| transaction    | Transaction    | トランザクション            |

### メソッド

| 名前          | 説明                              |
| ----------- | ------------------------------- |
| update      | 保存されている値の基礎となる値を更新              |
| animation   | バインディングの値が変化したときに実行するアニメーションを指定 |
| transaction | トランザクションを指定                     |

### メソッド詳細

#### update

##### 意味

保存されている値の基礎となる値を更新

##### 使い方

    .update()

##### 例

    @Binding var isPlaying: Bool
    isPlaying
        .update()

#### animation

##### 意味

バインディングの値が変化したときに実行するアニメーションを指定

##### 使い方

    .animation(実行されるアニメーション・シーケンス(Animation)? = .default)

##### 例

    @Binding var isPlaying: Bool
    isPlaying
        .animation()

#### transaction

##### 意味

トランザクションを指定

##### 使い方

    .transaction(トランザクション(Transaction))

##### 例

    @Binding var isPlaying: Bool
    isPlaying
        .transaction {_ in }

### 参考サイト

<https://developer.apple.com/documentation/swiftui/binding>

---
layout: page
---

### 説明

現在の状態処理の更新のコンテキスト

### 使い方

#### トランザクションを作成

    Transaction()
        .メソッド

#### トランザクションを作成しそのアニメーションプロパティを割り当てる

    Transaction(animation: 状態が変化したときに実行するアニメーション(Animation))
        .メソッド

### 例

#### 基本的な使い方

    Transaction()

### 宣言

    @frozen struct Transaction

### プロパティ

| 名前                 | 型          | 説明                            |
| ------------------ | ---------- | ----------------------------- |
| animation          | Animation? | 現在の状態変化に関連するアニメーションがあればそれを表示  |
| disablesAnimations | Bool       | ビューがアニメーションを無効にするか            |
| isContinuous       | Bool       | トランザクションが一連の値を生成するアクションに由来するか |

### メソッド

| 名前              | 説明                           |
| --------------- | ---------------------------- |
| withTransaction | 指定されたトランザクションでクロージャーを実行しその結果 |

### メソッド詳細

#### withTransaction

##### 意味

指定されたトランザクションでクロージャーを実行しその結果

##### 使い方

    .withTransaction(スレッドの現在のトランザクションとして設定されたトランザクションのインスタンス(Transaction)) {
        実行するためのクロージャー
    }

    .withTransaction(スレッドの現在のトランザクションとして設定されたトランザクションのインスタンス(Transaction), 実行するためのクロージャー)

### 参考サイト

<https://developer.apple.com/documentation/swiftui/transaction>

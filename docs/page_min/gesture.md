---
layout: page
---

### 説明

一連のイベントをジェスチャーにマッチさせその状態ごとに値のストリームを返すインスタンス

### 使い方

    Gesture()

### 例

#### 基本的な使い方

    let gesture: Gesture

### 宣言

    protocol Gesture

### プロパティ

| 名前              | 型       | 説明                                |
| --------------- | ------- | --------------------------------- |
| minimumDuration | Double  | ジェスチャーが成功するまでに経過しなければならない長押しの最小時間 |
| maximumDistance | CGFloat | ジェスチャーが失敗するまでに移動できる最大の距離          |

### メソッド

| 名前             | 説明                                                                     |
| -------------- | ---------------------------------------------------------------------- |
| updating       | ジェスチャーの値が変更されると提供されたジェスチャーの状態プロパティを更新                                  |
| onChanged      | ジェスチャーの値が変化したときに実行するアクションを追加                                           |
| onEnded        | ジェスチャーの終了時に実行するアクションを追加                                                |
| simultaneously | 別のジェスチャーを組み合わせて両方のジェスチャーを同時に認識する新しいジェスチャーを作成                           |
| sequenced      | 別のジェスチャーを連続させて新しいジェスチャーを作成すると最初のジェスチャーが成功した後に2番目のジェスチャーがイベントを受け取るだけになる |
| exclusively    | 1つのジェスチャーだけが成功する新しいジェスチャーを作成し最初のジェスチャーを優先                              |
| modifiers      | ジェスチャーとキーボードメソッドを組み合わせ                                                 |
| map            | 与えられたクロージャーをジェスチャーにマッピングした結果のジェスチャー                                    |

---
layout: page
---

### 説明

type-erasedの変遷

### 宣言

    @frozen struct AnyTransition

### プロパティ

| 名前                     | 型             | 説明                                                     |
| ---------------------- | ------------- | ------------------------------------------------------ |
| AnyTransition.identity | AnyTransition | 入力ビューを修正せずに出力ビューとして返すトランジション                           |
| AnyTransition.opacity  | AnyTransition | 挿入時には透明から不透明へ取り出し時には不透明から透明へと変化                        |
| AnyTransition.scale    | AnyTransition | スケール                                                   |
| AnyTransition.slide    | AnyTransition | リーディングエッジからインすることで挿入しトレーリングエッジに向かってアウトすることで除去するトランジション |

### メソッド

| 名前                      | 説明                                      |
| ------------------------ | --------------------------------------- |
| AnyTransition.asymmetric | 挿入と削除で異なるトランジションを使用する複合トランジション          |
| AnyTransition.modifier   | アクティブメソッドとアイデンティティメソッドの間で定義されているトランジション |
| AnyTransition.move       | ビューの指定された辺に向かってビューを遠ざけるトランジション          |
| AnyTransition.offset     | オフセット                                   |
| AnyTransition.scale      | スケール                                    |
| animation                | アニメーションを付加                                        |
| combined                 | 両方のトランジションを適用した結果である新しいトランジション          |

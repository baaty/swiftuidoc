---
layout: page
---

### 説明

フェッチリクエストを行いCore Dataストアから結果を取得するプロパティラッパー

### 使い方

#### パラメータに基づいてフェッチ・リクエストを定義することでインスタンスを作成

    FetchRequest(entity: モデル化されたオブジェクトの種類(NSEntityDescription), sortDescriptors: フェッチされた結果のソート順を定義([NSSortDescriptor]), predicate: フェッチされた結果に対するフィルタを定義(NSPredicate) = nil, animation: 結果を変更する際に使用するアニメーション(Animation) = nil)

#### パラメータに基づいてフェッチ・リクエストを定義することでインスタンスを作成

    FetchRequest(sortDescriptors: フェッチされた結果のソート順を定義([NSSortDescriptor]), predicate: フェッチされた結果に対するフィルタを定義(NSPredicate) = nil, animation: 結果を変更する際に使用するアニメーション(Animation) = nil)

#### フェッチ・リクエストからインスタンスを作成

    FetchRequest(fetchRequest: 結果を生成するために使用されたリクエスト(NSFetchRequest<Result>), animation: 結果を変更する際に使用するアニメーション(Animation) = nil)

    FetchRequest(fetchRequest: NSFetchRequest<Result>, transaction: 結果を変更する際に使用されるトランザクション(Transaction))

### 例

#### 基本的な使い方

    FetchRequest(sortDescriptors: [NSSortDescriptor])

### 宣言

    @propertyWrapper struct FetchRequest<Result> where Result : NSFetchRequestResult

### プロパティ

| 名前           | 型                      | 説明                  |
| ------------ | ---------------------- | ------------------- |
| wrappedValue | FetchedResults<Result> | フェッチリクエストのフェッチされた結果 |

### メソッド

| 名前     | 説明  |
| ------ | --- |
| update | 更新  |

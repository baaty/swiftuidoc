---
layout: page
---

### 説明

FetchedResultsコレクションタイプはフェッチリクエストの実行結果

### 使い方

    var X: FetchedResults<NSNumber>()

### 引数について

#### NSFetchRequestResultで使えるタイプ

-   NSObjectProtocol
-   NSDictionary
-   NSManagedObject
-   NSManagedObjectID
-   NSNumber

### 例

#### 基本的な使い方

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]

### 宣言

    struct FetchedResults<Result> where Result : NSFetchRequestResult

### プロパティ

| 名前                  | 型                                   | 説明                                                    |
| ------------------- | ----------------------------------- | ----------------------------------------------------- |
| count               | Int                                 | コレクションの要素数                                            |
| endIndex            | Int                                 | 最後の有効な添え字の引数よりも1つ大きい位置                                |
| first               | Self.Element?                       | コレクションの最初の要素                                          |
| isEmpty             | Bool                                | コレクションが空であるかどうか                                       |
| last                | Self.Element?                       | コレクションの最後の要素                                          |
| lazy                | LazySequence&lt;Self&gt;                  | このシーケンスと同じ要素を含むがmapやfilterなどのいくつかの操作が遅延的に実装されているシーケンス |
| publisher           | Publishers.Sequence&lt;Self, Never&gt; | パブリッシャー                                               |
| startIndex          | Int                                 | 空ではないコレクションの最初の要素の位置                                  |
| underestimatedCount | Int                                 | コレクションの要素数以下の値                                        |

### メソッド

| 名前                               | 説明                                                      |
| -------------------------------- | ------------------------------------------------------- |
| allSatisfy                       | シーケンスの各要素が与えられた述語を満たすか                                  |
| clip                             | 現在のグラフィックコンテキストのクリッピングパスをこの矩形のリストのグラフィカルユニオンと交差させることで変更 |
| compactMap                       | 与えられた変換を呼び出した結果（非nil）を含む配列                              |
| contains                         | シーケンスに指定された要素が含まれているか                                   |
| difference                       | 与えられたコレクションからこのコレクションの順序付き要素を生成するために必要な差                |
| drop                             | predicateがtrueを返している間の要素をスキップして残りの要素                    |
| dropFirst                        | 指定された数の初期要素を除くすべての要素を含むサブシーケンス                          |
| dropLast                         | 指定された数の最終要素以外を含むサブシーケンス                                 |
| elementsEqual                    | このシーケンスと別のシーケンスが同じ要素を同じ順序で含んでいるか                        |
| enumerated                       | nは0から始まる連続した整数を表しxはシーケンスの要素                             |
| fill                             | 現在のNSGraphicsContext内の矩形のリストをその矩形に関連付けられた色で塗りつぶす        |
| filter                           | 与えられた述語を満たすシーケンスの要素を順番に並べた配列                            |
| first                            | 与えられた述語を満たすシーケンスの最初の要素                                  |
| firstIndex                       | コレクション内で指定した値が出現する最初のインデックス                             |
| flatMap                          | 与えられた変換をこのシーケンスの各要素で呼び出した結果を連結した配列                      |
| forEach                          | for-inループと同じ順序でシーケンスの各要素に対して与えられたクロージャ                  |
| formIndex                        | 指定されたインデックスを指定された距離だけオフセット                              |
| index                            | 定されたインデックスから指定された距離だけ離れたインデックス                          |
| joined                           | このシーケンスの配列の要素を連結                                        |
| last                             | 与えられた述語を満足させるシーケンスの最後の要素                                |
| lastIndex                        | 指定した値がコレクション内で最後に出現したインデックス                             |
| lexicographicallyPrecedes        | 辞書的順序でシーケンスが別のシーケンスより前にあるか                              |
| makeIterator                     | コレクションの要素を表すイテレータ                                       |
| map                              | 与えられたクロージャをシーケンスの要素にマッピングした結果を含む配列                      |
| max                              | シーケンスの最大要素                                              |
| min                              | シーケンス内の最小要素                                             |
| prefix                           | コレクションの初期要素を含む指定された最大長までのサブシーケンス                        |
| randomElement                    | コレクションのランダムな要素                                          |
| reduce                           | 与えられたクロージャを使用してシーケンスの要素を結合した結果                          |
| reversed                         | コレクションの要素を逆順に表示するビュー                                    |
| shuffled                         | シーケンスの要素をシャッフル                                          |
| sorted                           | シーケンスの要素をソート                                            |
| split                            | 与えられた述語を満たす要素を含まない可能な限り長いコレクションの部分列を順に返す                |
| starts                           | シーケンスの初期要素が別のシーケンスの要素と同じか                               |
| suffix                           | コレクションの最後の要素を含む指定された最大長までのサブシーケンス                       |
| withContiguousStorageIfAvailable | body(p)を呼び出す                                            |

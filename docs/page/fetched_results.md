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

### メソッド詳細

#### allSatisfy

##### 意味

シーケンスの各要素が与えられた述語を満たすか

##### 使い方

    .allSatisfy {要素(Self.Element) in
        条件(Void)
    }

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    cast.allSatisfy{_ in
        // 条件
    }

#### clip

##### 意味

現在のグラフィックコンテキストのクリッピングパスをこの矩形のリストのグラフィカルユニオンと交差させることで変更

##### 使い方

    .clip()

#### compactMap

##### 意味

与えられた変換を呼び出した結果（非nil）を含む配列

##### 使い方

    .compactMap {要素(Self.Element) in
        // 変換
    }

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    cast.compactMap {_ in
        // 変換
    }

#### contains

##### 意味

シーケンスに指定された要素が含まれているか

##### 使い方

    .contains(要素(Self.Element))

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    cast.contains("Marlon")

#### difference

##### 意味

与えられたコレクションからこのコレクションの順序付き要素を生成するために必要な差

##### 使い方

    .difference(from: 状態(BidirectionalCollection))

#### drop

##### 意味

predicateがtrueを返している間の要素をスキップして残りの要素

##### 使い方

    .drop{要素(Self.Element) in
        // 処理
    }

#### dropFirst

##### 意味

指定された数の初期要素を除くすべての要素を含むサブシーケンス

##### 使い方

    .dropFirst(コレクションの先頭からドロップする要素の数(Int = 1))

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    cast.dropFirst(1)

#### dropLast

##### 意味

指定された数の最終要素以外を含むサブシーケンス

##### 使い方

    .dropLast(コレクションの最後にドロップする要素の数(Int))

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    cast.dropLast(1)

#### elementsEqual

##### 意味

このシーケンスと別のシーケンスが同じ要素を同じ順序で含んでいるか

##### 使い方

    .elementsEqual(比較するためのシーケンス(OtherSequence))

##### 例

    let a = 1...3
    let b = 1...10
    a.elementsEqual(b)

#### enumerated

##### 意味

nは0から始まる連続した整数を表しxはシーケンスの要素

##### 使い方

    .enumerated()

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    cast.enumerated()

#### fill

##### 意味

現在のNSGraphicsContext内の矩形のリストをその矩形に関連付けられた色で塗りつぶす

##### 使い方

    .fill(using: NSCompositingOperation = NSGraphicsContext.current?.compositingOperation ?? .sourceOver)

#### filter

##### 意味

与えられた述語を満たすシーケンスの要素を順番に並べた配列

##### 使い方

    .filter {
        要素を戻り値の配列に含めるか(Self.Element)
    }

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    cast.filter { $0.count < 5 }

#### first

##### 意味

与えられた述語を満たすシーケンスの最初の要素

##### 使い方

    .first(where: 要素がマッチしているかどうか)

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    if let firstNegative = cast.first(where: { $0 < 0 }) {
        print("The first negative number is \(firstNegative).")
    }

#### firstIndex

##### 意味

コレクション内で指定した値が出現する最初のインデックス

##### 使い方

    .firstIndex(of: コレクション内で検索する要素(Self.Element))

##### 例

    var students = ["Ben", "Ivy", "Jordell", "Maxime"]
    if let i = students.firstIndex(of: "Maxime") {
        students[i] = "Max"
    }
    print(students)
    // Prints "["Ben", "Ivy", "Jordell", "Max"]"

#### flatMap

##### 意味

与えられた変換をこのシーケンスの各要素で呼び出した結果を連結した配列

##### 使い方

    .flatMap(クロージャ((Self.Element) throws -> SegmentOfResult))

##### 例

    let flatMapped = numbers.flatMap { Array(repeating: $0, count: $0) }
    // [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]

#### forEach

##### 意味

for-inループと同じ順序でシーケンスの各要素に対して与えられたクロージャ

##### 使い方

    .forEach {要素(Self.Element) in
        // 処理
     }

##### 例

    let numberWords = ["one", "two", "three"]
    numberWords.forEach { word in
        print(word)
    }

#### formIndex

##### 意味

指定されたインデックスを指定された距離だけオフセット

##### 使い方

    .formIndex(コレクションの有効なインデックス(Self.Index), offsetBy: オフセット(Int))

#### joined

##### 意味

このシーケンスの配列の要素を連結

##### 使い方

    .joined()

    .joined(separator: このシーケンスの各要素の間に挿入するシーケンス(Separator))

    .joined(separator: シーケンス内の各要素の間に挿入する文字列(String) = "")

##### 例

    let ranges = [0..<3, 8..<10, 15..<17]
    for index in ranges.joined() {
        print(index, terminator: " ")
    }
    // Prints: "0 1 2 8 9 15 16"

#### last

##### 意味

与えられた述語を満足させるシーケンスの最後の要素

##### 使い方

    .last(where: 要素がマッチしているかどうか((Self.Element) throws -> Bool))

##### 例

    let numbers = [3, 7, 4, -2, 9, -6, 10, 1]
    if let lastNegative = numbers.last(where: { $0 < 0 }) {
        print("The last negative number is \(lastNegative).")
    }
    // Prints "The last negative number is -6."

#### lastIndex

##### 意味

指定した値がコレクション内で最後に出現したインデックス

##### 使い方

    .lastIndex(of: コレクション内で検索する要素(Self.Element))

    .lastIndex(where: 渡された要素がマッチしているか((Self.Element) throws -> Bool))

##### 例

    var students = ["Ben", "Ivy", "Jordell", "Ben", "Maxime"]
    if let i = students.lastIndex(of: "Ben") {
        students[i] = "Benjamin"
    }
    print(students)
    // Prints "["Ben", "Ivy", "Jordell", "Benjamin", "Max"]"

#### lexicographicallyPrecedes

##### 意味

辞書的順序でシーケンスが別のシーケンスより前にあるか

##### 使い方

    .lexicographicallyPrecedes(比較するためのシーケンス(OtherSequence))

    .lexicographicallyPrecedes(比較するためのシーケンス(OtherSequence), by: 最初の引数が2番目の引数の前に並べられるべきであれば真((Self.Element, Self.Element) throws -> Bool))

##### 例

    let a = [1, 2, 2, 2]
    let b = [1, 2, 3, 4]
    print(a.lexicographicallyPrecedes(b))
    // Prints "true"

#### makeIterator

##### 意味

コレクションの要素を表すイテレータ

##### 使い方

    .makeIterator()

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    cast.makeIterator()

#### map

##### 意味

与えられたクロージャをシーケンスの要素にマッピングした結果を含む配列

##### 使い方

    .map<T>(同じまたは異なる型の変換された値((Self.Element) throws -> T))

##### 例

    let cast = ["Vivien", "Marlon", "Kim", "Karl"]
    let lowercaseNames = cast.map { $0.lowercased() }
    // 'lowercaseNames' == ["vivien", "marlon", "kim", "karl"]

#### max

##### 意味

シーケンスの最大要素

##### 使い方

    .max()

    .max(by: 最初の引数が2番目の引数の前に並べられるべきであれば真((Self.Element, Self.Element) throws -> Bool))

##### 例

    let heights = [67.5, 65.7, 64.3, 61.1, 58.5, 60.3, 64.9]
    let greatestHeight = heights.max()
    print(greatestHeight)
    // Prints "Optional(67.5)"

#### min

##### 意味

シーケンス内の最小要素

##### 使い方

    .min()

    .min(by: 最初の引数が2番目の引数の前に並べられるべきであれば真((Self.Element, Self.Element) throws -> Bool))

##### 例

    let heights = [67.5, 65.7, 64.3, 61.1, 58.5, 60.3, 64.9]
    let lowestHeight = heights.min()
    print(lowestHeight)
    // Prints "Optional(58.5)"

#### prefix

##### 意味

コレクションの初期要素を含む指定された最大長までのサブシーケンス

##### 使い方

    .prefix(最大長(Int))

    .prefix(through: 含める最後の要素のインデックス(Self.Index))

    .prefix(upTo: 部分列の過去の終わりのインデックス(Self.Index))

    .prefix(while: クロージャ((Self.Element) throws -> Bool))

##### 例

    let numbers = [1, 2, 3, 4, 5]
    print(numbers.prefix(2))
    // Prints "[1, 2]"

#### randomElement

##### 意味

コレクションのランダムな要素

##### 使い方

    .randomElement()

    .randomElement(using: 乱数発生器(inout T))

##### 例

    let names = ["Zoey", "Chloe", "Amani", "Amaia"]
    let randomName = names.randomElement()!
    // randomName == "Amani"

    let names = ["Zoey", "Chloe", "Amani", "Amaia"]
    let randomName = names.randomElement(using: &myGenerator)!
    // randomName == "Amani"

#### reduce

##### 意味

与えられたクロージャを使用してシーケンスの要素を結合した結果

##### 使い方

    .reduce(クロージャーが最初に実行されるときにnextPartialResultに渡される(Result), 累積値とシーケンスの要素を結合して新しい累積値にするクロージャ((Result, Self.Element) throws -> Result))

    reduce<Result>(into: 初期の累積値として使用する値(Result), 累積値をシーケンスの要素で更新するクロージャー((inout Result, Self.Element) throws -> ()))

##### 例

    let numbers = [1, 2, 3, 4]
    let numberSum = numbers.reduce(0, { x, y in
        x + y
    })
    // numberSum == 10

    let letters = "abracadabra"
    let letterCount = letters.reduce(into: [:]) { counts, letter in
        counts[letter, default: 0] += 1
    }
    // letterCount == ["a": 5, "b": 2, "r": 2, "c": 1, "d": 1]

#### reversed

##### 意味

コレクションの要素を逆順に表示するビュー

##### 使い方

    .reversed()

##### 例

    let word = "Backwards"
    for char in word.reversed() {
        print(char, terminator: "")
    }
    // Prints "sdrawkcaB"

#### shuffled

##### 意味

シーケンスの要素をシャッフル

##### 使い方

    .shuffled()

    .shuffled(using: シーケンスをシャッフルする際に使用する乱数発生器(RandomNumberGenerator))

##### 例

    let numbers = 0...9
    let shuffledNumbers = numbers.shuffled()
    // shuffledNumbers == [1, 7, 6, 2, 8, 9, 4, 3, 5, 0]

    let numbers = 0...9
    let shuffledNumbers = numbers.shuffled(using: &myGenerator)
    // shuffledNumbers == [8, 9, 4, 3, 2, 6, 7, 0, 5, 1]

#### sorted

##### 意味

シーケンスの要素をソート

##### 使い方

    .sorted()

    .sorted(by: 最初の引数が2番目の引数の前に並べられるべきであれば真((Self.Element, Self.Element) throws -> Bool))

##### 例

    let students: Set = ["Kofi", "Abena", "Peter", "Kweku", "Akosua"]
    let sortedStudents = students.sorted()
    print(sortedStudents)
    // Prints "["Abena", "Akosua", "Kofi", "Kweku", "Peter"]"

    let students: Set = ["Kofi", "Abena", "Peter", "Kweku", "Akosua"]
    let descendingStudents = students.sorted(by: >)
    print(descendingStudents)
    // Prints "["Peter", "Kweku", "Kofi", "Akosua", "Abena"]"

#### split

##### 意味

与えられた述語を満たす要素を含まない可能な限り長いコレクションの部分列を順に返す

##### 使い方

    .split(maxSplits: コレクションを分割する最大回数(Int) = Int.max, omittingEmptySubsequences: falseで空のサブシーケンスが結果(Bool) = true, whereSeparator: コレクションをその要素で分割するか((Self.Element) throws -> Bool))

    .split(separator: 分割されるべき要素(Self.Element), maxSplits: コレクションを分割する最大回数(Int) = Int.max, omittingEmptySubsequences: falseで空のサブシーケンスが結果(Bool) = true)

##### 例

    let line = "BLANCHE:   I don't want realism. I want magic!"
    print(line.split(whereSeparator: { $0 == " " }))
    // Prints "["BLANCHE:", "I", "don\'t", "want", "realism.", "I", "want", "magic!"]"

    let line = "BLANCHE:   I don't want realism. I want magic!"
    print(line.split(separator: " "))
    // Prints "["BLANCHE:", "I", "don\'t", "want", "realism.", "I", "want", "magic!"]"

#### starts

##### 意味

シーケンスの初期要素が別のシーケンスの要素と同じか

##### 使い方

    .starts(with: 比較するためのシーケンス(PossiblePrefix))

    .starts(with: 比較するためのシーケンス(PossiblePrefix), by: 2つの引数が等価であれば真((Self.Element, PossiblePrefix.Element) throws -> Bool))

##### 例

    let a = 1...3
    let b = 1...10
    print(b.starts(with: a))
    // Prints "true"

#### suffix

##### 意味

コレクションの最後の要素を含む指定された最大長までのサブシーケンス

##### 使い方

    .zsuffix(最大長(Int))

    .suffix(from: サブシーケンスを開始するインデックス(Self.Index))

##### 例

    let numbers = [1, 2, 3, 4, 5]
    print(numbers.suffix(2))
    // Prints "[4, 5]"

    let numbers = [10, 20, 30, 40, 50, 60]
    if let i = numbers.firstIndex(of: 40) {
        print(numbers.suffix(from: i))
    }
    // Prints "[40, 50, 60]"

#### withContiguousStorageIfAvailable

##### 意味

body(p)を呼び出す

##### 使い方

    .withContiguousStorageIfAvailable(body((UnsafeBufferPointer<Self.Element>) throws -> R))

### 参考サイト

<https://developer.apple.com/documentation/swiftui/fetchedresults>

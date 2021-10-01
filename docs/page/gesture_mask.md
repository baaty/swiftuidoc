---
layout: page
---

### 説明

ジェスチャーをビューに追加することでビューとそのサブビューで認識される他のジェスチャーへの影響を制御するオプション

### 使い方

#### 生タイプの対応する値

    GestureMask()
        .メソッド

#### アイテムの有限のシーケンスから新しいセットを作成

    GestureMask(新しいセットのメンバーとして使用する要素(Sequence))
        .メソッド

#### 与えられた配列リテラルの要素を含むセットを作成

    GestureMask(arrayLiteral: 新しいセットの要素のリスト(Self.Element...))
        .メソッド

#### 与えられた生の値から新しいオプションセットを作成

    GestureMask(rawValue: オプションセットの生の値(UInt32))
        .メソッド

### 例

#### 基本的な使い方

    GestureMask()

### 宣言

    @frozen struct GestureMask

### プロパティ

| 名前        | 型           | 説明                                    |
| --------- | ----------- | ------------------------------------- |
| all       | GestureMask | すべてのジェスチャーを有効                         |
| gesture   | GestureMask | 追加されたジェスチャーを有効にしサブビュー階層のすべてのジェスチャーを無効 |
| subviews  | GestureMask | サブビュー階層のすべてのジェスチャーを有効にし追加されたジェスチャーを無効 |
| none      | GestureMask | すべてのジェスチャーを無効                         |
| isEmpty   | Bool        | セットに要素がないかどうか                         |
| rawValue | UInt32      | 生タイプの対応する値                            |

### メソッド

| 名前                      | 説明                                                           |
| ----------------------- | ------------------------------------------------------------ |
| contains                | 指定された要素がオプションセットのメンバーであるか　                                   |
| isDisjoint              | セットが指定されたセットと共通のメンバーを持たないか                                   |
| update                  | 与えられた要素をセットに挿入                                               |
| insert                  | 与えられた要素がまだメンバーになっていない場合オプションセットに追加                           |
| subtract                | 与えられたセットの要素をこのセットから削除                                        |
| subtracting             | 与えられたセットの中に存在しない要素を含む新しいセット                                  |
| remove                  | 与えられた要素とその要素に包含されるすべての要素を削除                                  |
| formUnion               | 別のセットの要素をこのオプションセットに挿入                                       |
| union                   | このセットに含まれる要素与えられたセットに含まれる要素あるいはその両方に含まれる要素の新しいオプションセット       |
| formIntersection        | このオプションセットの中で与えられたセットにも存在しないすべての要素を削除                        |
| intersection            | このセットと指定されたセットの両方に含まれる要素のみを持つ新しいオプションセット                     |
| formSymmetricDifference | このセットをこのセットか与えられたセットのいずれかに含まれるが両方には含まれないすべての要素を含む新しいセットで置き換え |
| symmetricDifference     | このセットか与えられたセットに含まれるが両方には含まれない要素を持つ新しいオプションセット                |
| isSubset                | セットが別のセットのサブセットであるか                                          |
| isStrictSubset          | このセットが指定されたセットの厳密なサブセットであるか                                  |
| isSuperset              | セットが指定されたセットのスーパーセットであるか                                     |
| isStrictSuperset        | このセットが指定されたセットの厳密なスーパーセットであるか                                |

### メソッド詳細

#### contains

##### 意味

指定された要素がオプションセットのメンバーであるか

##### 使い方

    .contains(オプションセットに求められる要素(Self))

##### 例

    GestureMask()
        .contains(gestureMask)

#### isDisjoint

##### 意味

セットが指定されたセットと共通のメンバーを持たないか

##### 使い方

    .isDisjoint(with: 現在のセットと同じタイプのセット(Self))

##### 例

    GestureMask()
        .isDisjoint(with: gestureMask)

#### update

##### 意味

与えられた要素をセットに挿入

##### 使い方

    .update(with: 現在のセットと同じタイプのセット(Self.Element))

##### 例

    GestureMask()
        .update(with: gestureMask)

#### insert

##### 意味

与えられた要素がまだメンバーになっていない場合オプションセットに追加

##### 使い方

    .insert(挿入する要素(Self.Element))

##### 例

    GestureMask()
        .insert(gestureMask.Element)

#### subtract

##### 意味

与えられたセットの要素をこのセットから削除

##### 使い方

    .subtract(現在のセットと同じタイプのセット(Self))

##### 例

    GestureMask()
        .subtract(gestureMask)

#### subtracting

##### 意味

与えられたセットの中に存在しない要素を含む新しいセット

##### 使い方

    .subtracting(現在のセットと同じタイプのセット(Self))

##### 例

    GestureMask()
        .subtracting(gestureMask)

#### remove

##### 意味

与えられた要素とその要素に包含されるすべての要素を削除

##### 使い方

    .remove(削除するセットの要素(Self.Element))

##### 例

    GestureMask()
        .remove(gestureMask.Element)

#### formUnion

##### 意味

別のセットの要素をこのオプションセットに挿入

##### 使い方

    .formUnion(オプションセット(Self))

##### 例

    GestureMask()
        .formUnion(gestureMask)

#### union

##### 意味

このセットに含まれる要素与えられたセットに含まれる要素あるいはその両方に含まれる要素の新しいオプションセット

##### 使い方

    .union(オプションセット(Self))

##### 例

    GestureMask()
        .union(gestureMask)

#### formIntersection

##### 意味

このオプションセットの中で与えられたセットにも存在しないすべての要素を削除

##### 使い方

    .formIntersection(オプションセット(Self))

##### 例

    GestureMask()
        .formIntersection(gestureMask)

#### intersection

##### 意味

このセットと指定されたセットの両方に含まれる要素のみを持つ新しいオプションセット

##### 使い方

    .intersection(オプションセット(Self))

##### 例

    GestureMask()
        .intersection(gestureMask)

#### formSymmetricDifference

##### 意味

このセットをこのセットか与えられたセットのいずれかに含まれるが両方には含まれないすべての要素を含む新しいセットで置き換え

##### 使い方

    .formSymmetricDifference(オプションセット(Self))

##### 例

    GestureMask()
        .formSymmetricDifference(gestureMask)

#### symmetricDifference

##### 意味

このセットか与えられたセットに含まれるが両方には含まれない要素を持つ新しいオプションセット

##### 使い方

    .symmetricDifference(オプションセット(Self))

##### 例

    GestureMask()
        .symmetricDifference(gestureMask)

#### isSubset

##### 意味

セットが別のセットのサブセットであるか

##### 使い方

    .isSubset(of: 現在のセットと同じタイプのセット(Self))

##### 例

    GestureMask()
        .isSubset(of: gestureMask)

#### isStrictSubset

##### 意味

このセットが指定されたセットの厳密なサブセットであるか

##### 使い方

    .isStrictSubset(of: 現在のセットと同じタイプのセット(Self))

##### 例

    GestureMask()
        .isStrictSubset(of: gestureMask)

#### isSuperset

##### 意味

セットが指定されたセットのスーパーセットであるか

##### 使い方

    .isSuperset(of: 現在のセットと同じタイプのセット(Self))

##### 例

    GestureMask()
        .isSuperset(of: gestureMask)

#### isStrictSuperset

##### 意味

このセットが指定されたセットの厳密なスーパーセットであるか

##### 使い方

    .isStrictSuperset(of: 現在のセットと同じタイプのセット(Self))

##### 例

    GestureMask()
        .isStrictSuperset(of: gestureMask)

### 参考サイト

<https://developer.apple.com/documentation/swiftui/gesturemask>

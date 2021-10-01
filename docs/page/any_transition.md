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

| 名前                       | 説明                                      |
| ------------------------ | --------------------------------------- |
| AnyTransition.asymmetric | 挿入と削除で異なるトランジションを使用する複合トランジション          |
| AnyTransition.modifier   | アクティブメソッドとアイデンティティメソッドの間で定義されているトランジション |
| AnyTransition.move       | ビューの指定された辺に向かってビューを遠ざけるトランジション          |
| AnyTransition.offset     | オフセット                                   |
| AnyTransition.scale      | スケール                                    |
| animation                | アニメーションを付加                              |
| combined                 | 両方のトランジションを適用した結果である新しいトランジション          |

### メソッド詳細

#### asymmetric

##### 意味

表示と非表示で異なるトランジションを使用する複合トランジション

##### 使い方

    .asymmetric(insertion: 追加するトランジション(AnyTransition), removal: 削除するトランジション(AnyTransition))

##### 例

    let insertion = AnyTransition.opacity
    let removal = AnyTransition.identity
    AnyTransition.asymmetric(insertion: insertion, removal: removal)

#### modifier

##### 意味

アクティブメソッドとアイデンティティメソッドの間で定義されているトランジション

##### 使い方

    .modifier(active: アクティブメソッド(ViewModifier), identity: アイデンティティメソッド(ViewModifier))

##### 例

    AnyTransition.modifier(active: AnimationModifier(opacity: 0, yOffset: 100), identity: AnimationModifier(opacity: 0, yOffset: 100))

#### move

##### 意味

ビューの指定された辺に向かってビューを遠ざけるトランジション

##### 使い方

    .move(edge: 辺(Edge))

##### 例

    AnyTransition.move(edge: .trailing)

#### offset

##### 意味

オフセット

##### 使い方

    .offset(オフセット(CGSize))

    .offset(x: X(CGFloat) = 0, y: Y(CGFloat) = 0)

##### CGSizeの使い方

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

##### 例

    AnyTransition.offset(CGSize(width: 20, height: 25))

#### scale

##### 意味

スケール

##### 使い方

    .scale(scale: スケール(CGFloat), anchor: 開始位置(UnitPoint) = .center)

##### UnitPointの使い方

| 名前                                | 説明         |
| --------------------------------- | ---------- |
| .bottom                           | 下          |
| .bottomLeading                    | 左下         |
| .bottomTrailing                   | 右下         |
| .center                           | 中央         |
| .leading                          | 左          |
| .top                              | 上          |
| .topLeading                       | 左上         |
| .topTrailing                      | 右上         |
| .trailing                         | 右          |
| .zero                             | 0          |
| UnitPoint()                       | 作成         |
| UnitPoint(x: CGFloat, y: CGFloat) | xとyを指定して作成 |

##### 例

    AnyTransition.scale(scale: 1)

#### animation

##### 意味

アニメーションを付加

##### 使い方

    .animation(アニメーショn(Animation)?)

##### 例

    let transition = AnyTransition.identity
    transition.animation(.default)

#### combined

##### 意味

両方のトランジションを適用した結果である新しいトランジション

##### 使い方

    .combined(with: トランジション効果(AnyTransition))

##### 例

    let transition = AnyTransition.identity
    transition.combined(with: hoge)

### 参考サイト

<https://developer.apple.com/documentation/swiftui/anytransition>

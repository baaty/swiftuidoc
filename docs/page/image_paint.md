---
layout: page
---

### 説明

画像の一部分を繰り返して形状を埋めるシェイプスタイル

### 使い方

    ImagePaint(image: 画像(Image), sourceRect: ソース画像のどの部分を描画するかを定義(CGRect) = CGRect(x: 0, y: 0, width: 1, height: 1), scale: 拡大率(CGFloat) = 1)
        .メソッド

### 引数の使い方

#### Image

| 名前                                                                          | 説明                                                             |
| --------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Image(String, bundle: Bundle?)                                              | コントロールのコンテンツとして使用できるラベル付きの画像を作成                                |
| Image(String, bundle: Bundle?, label: Text)                                 | コントロールのコンテンツとして使用できる指定されたラベル付きの画像を作成                           |
| Image(CGImage, scale: CGFloat, orientation: Image.Orientation, label: Text) | Core Graphicsのイメージ・インスタンスに基づいてコントロールのコンテンツとして使用可能なラベル付きイメージを作成 |
| Image(decorative: String, bundle: Bundle?)                                  | ラベルのない装飾的な画像を作成                                                |
| Image(decorative: CGImage, scale: CGFloat, orientation: Image.Orientation)  | Core Graphicsのイメージインスタンスに基づいてラベルのない装飾的なイメージを作成                 |
| Image(systemName: String)                                                   | システムシンボルイメージを作成                                                |
| Image(uiImage: UIImage)                                                     | UIKitのイメージインスタンスからSwiftUIのイメージを作成                              |
| Image(nsImage: NSImage)                                                     | AppKitのイメージインスタンスからSwiftUIのイメージを作成                             |

### 例

#### 基本的な使い方

    ImagePaint(image: Image("hoge"))

### 宣言

    @frozen struct ImagePaint

#### プロパティ

| 名前         | 型       | 説明                         |
| ---------- | ------- | -------------------------- |
| image      | Image   | 描画される画像                    |
| scale      | CGFloat | 描画中の画像に適用されるスケールファクター      |
| sourceRect | CGRect  | 描画するソースイメージの量を定義する単位空間の長方形 |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/imagepaint>

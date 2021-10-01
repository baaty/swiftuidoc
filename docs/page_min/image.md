---
layout: page
---

### 説明

画像を表示するビュー  
アセットカタログに登録されている画像やシステムに登録されているアイコンを表示

### 使い方

#### コントロールのコンテンツとして使用できるラベル付きの画像を作成

    Image("画像名", bundle: 検索用のバンドル(Bundle) = nil)

#### コントロールのコンテンツとして使用できる指定されたラベル付きの画像を作成

    Image("画像名", bundle: 検索用のバンドル(Bundle) = nil, label: ラベル(Text))

#### Core Graphicsのイメージ・インスタンスに基づいてコントロールのコンテンツとして使用可能なラベル付きイメージを作成

    Image(ベースとなるグラフィックイメージ(CGImage), scale: 画像の拡大率(CGFloat), orientation: 画像の向き(Image.Orientation) = .up, label: ラベル(Text))

#### ラベルのない装飾的な画像を作成

    Image(decorative: "画像名", bundle: 検索用のバンドル(Bundle) = nil)

#### Core Graphicsのイメージインスタンスに基づいてラベルのない装飾的なイメージを作成

    Image(decorative cgImage: グラフィックイメージ(CGImage), scale: 画像の拡大率(CGFloat), orientation: 画像の向き(Image.Orientation) = .up)

#### システムシンボルイメージを作成

    Image(systemName: "システムシンボルイメージの名前")

#### UIKitのイメージインスタンスからSwiftUIのイメージを作成

    Image(uiImage: UIKitイメージ(UIImage))

#### AppKitのイメージインスタンスからSwiftUIのイメージを作成

    Image(nsImage: AppKitイメージ(NSImage))

### 引数の使い方

#### CGImage

| 名前                                                                                                                                                                                                                                                              | 説明                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ |
| CGImage(width: Int, height: Int, bitsPerComponent: Int, bitsPerPixel: Int, bytesPerRow: Int, space: CGColorSpace, bitmapInfo: CGBitmapInfo, provider: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool, intent: CGColorRenderingIntent) | ビットマップイメージを作成                  |
| CGImage(jpegDataProviderSource: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool, intent: CGColorRenderingIntent)                                                                                                                       | JPEGエンコードされたデータを用いてビットマップ画像を作成 |
| CGImage(pngDataProviderSource: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool, intent: CGColorRenderingIntent)                                                                                                                        | PNGエンコードされたデータを用いてビットマップ画像を作成  |

#### Image.Orientation

| 名前                                 | 説明                      |
| ---------------------------------- | ----------------------- |
| .down                              | 180°回転                  |
| .downMirrored                      | 垂直に反転                   |
| .left                              | 反時計回りに90°回転             |
| .leftMirrored                      | 時計回りに90°回転させ水平方向に反転     |
| .right                             | 時計回りに90°回転              |
| .ightMirrored                      | 反時計回りに90°回転し水平方向に反転     |
| .up                                | 意図する表示方向と一致　            |
| .upMirrored                        | 水平に反転　                  |
| Image.Orientation(rawValue: UInt8) | 指定された生の値を持つ新しいインスタンスを作成 |

#### UIImage

| 名前                                                                          | 説明                                                              |
| --------------------------------------------------------------------------- | --------------------------------------------------------------- |
| UIImage?(named: String, in: Bundle?, compatibleWith: UITraitCollection?)    | 指定されたtrait collectionと互換性のある指定されたimage assetを使ってimage objectを作成 |
| UIImage?(named: String, in: Bundle?, with: UIImage.Configuration?)          | 指定された構成に適合した指定されたイメージアセットを使用してイメージオブジェクトを作成                     |
| UIImage?(named: String)                                                     | 指定された名前のアセットからイメージオブジェクトを作成                                     |
| UIImage(imageLiteralResourceName: String)                                   | 指定されたリソースのイメージオブジェクト                                            |
| UIImage?(systemName: String, withConfiguration: UIImage.Configuration?)     | 指定された設定のシステムシンボルイメージを含むイメージオブジェクトを作成                            |
| UIImage?(systemName: String, compatibleWith: UITraitCollection?)            | 指定された形質に適したシステムシンボルイメージを含むイメージオブジェクトを作成                         |
| UIImage?(systemName: String)                                                | システムシンボルの画像を含むイメージオブジェクトを作成                                     |
| UIImage?(contentsOfFile: String)                                            | 指定されたファイルの内容を持つイメージオブジェクトを初期化                                   |
| UIImage?(data: Data)                                                        | 指定されたデータを持つイメージオブジェクトを初期化                                       |
| UIImage?(data: Data, scale: CGFloat)                                        | 指定されたデータとスケールファクターを持つイメージオブジェクトを初期化                             |
| UIImage(cgImage: CGImage)                                                   | 指定されたQuartz画像参照を持つイメージオブジェクトを初期化                                |
| UIImage(cgImage: CGImage, scale: CGFloat, orientation: UIImage.Orientation) | 指定されたスケールとオリエンテーションファクターを持つイメージオブジェクトを初期化                       |
| UIImage(ciImage: CIImage)                                                   | 指定されたCore Imageオブジェクトを持つイメージオブジェクトを初期化                          |
| UIImage(ciImage: CIImage, scale: CGFloat, orientation: UIImage.Orientation) | 指定されたCore Imageオブジェクトとプロパティを持つイメージオブジェクトを初期化                    |

#### NSImage

| 名前                                                                                                                              | 説明                                             |
| ------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| NSImage?(named: NSImage.Name)                                                                                                   | イメージオブジェクト                                     |
| NSImage(imageLiteralResourceName: String)                                                                                       | 初期化されたイメージを作成                                  |
| NSImage?(systemSymbolName: String, accessibilityDescription: String?)                                                           | システムシンボル名とアクセシビリティの説明を持つシンボルイメージを作成            |
| NSImage(size: NSSize, flipped drawingHandlerShouldBeCalledWithFlippedContext: Bool, drawingHandler: @escaping (NSRect) -> Bool) | 指定されたブロックを使ってコンテンツが描画されるイメージオブジェクトを作成          |
| NSImage?(byReferencingFile: String)                                                                                             | 指定されたファイルを使用してイメージオブジェクトを初期化                   |
| NSImage(byReferencing: URL)                                                                                                     | 指定されたURLを使用してイメージオブジェクトを初期化                    |
| NSImage?(contentsOfFile: String)                                                                                                | 指定されたファイルの内容を持つイメージオブジェクトを初期化                  |
| NSImage?(contentsOf: URL)                                                                                                       | 指定されたURLのコンテンツを持つイメージオブジェクトを初期化                |
| NSImage?(data: Data)                                                                                                            | 与えられた画像データを使って画像オブジェクトを初期化                     |
| NSImage?(dataIgnoringOrientation: Data)                                                                                         | 与えられた画像データを用いてEXIFオリエンテーションタグを無視した画像オブジェクトを初期化 |
| NSImage(cgImage: CGImage, size: NSSize)                                                                                         | 与えられた画像の内容を使って新しい画像を作成                         |
| NSImage?(pasteboard: NSPasteboard)                                                                                              | 指定されたペーストボードのデータを持つイメージオブジェクトを初期化              |
| NSImage(coder: NSCoder)                                                                                                         | アンアーカイバのデータからイメージオブジェクトを初期化                    |
| NSImage(size: NSSize)                                                                                                           | 指定された寸法の画像オブジェクトを初期化                           |

### 例

#### 基本的な使い方

    Image("画像名")

#### 画像のサイズを変更

    Image("画像名")
        .resizable()
        .frame(width: 80, height: 80)

#### 丸い画像

    Image("画像名")
        .clipShape(Circle())

#### アイコン

    Image(systemName: "suit.heart.fill")

#### 複数カラーアイコン

    Image(systemName: "timer")
        .renderingMode(.original)

### 宣言

    @frozen struct Image

### メソッド

| 名前            | 説明                |
| ------------- | ----------------- |
| resizable     | リサイズするモードを設定      |
| renderingMode | レンダリングモードを設定      |
| interpolation | 品質レベルを指定          |
| antialiased   | アンチエイリアスを適用するかどうか |

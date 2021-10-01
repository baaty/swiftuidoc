---
layout: page
---

### 説明

カラー

### 使い方

#### CGColorのインスタンスから色を作成

    Color(色(CGColor))

#### NSColorのインスタンスから色を作成

    Color(色(NSColor))

#### UIColorのインスタンスから色を作成

    Color(色(UIColor))

#### 名前付きのカラーを作成

    Color(名前(String), bundle: バンドルの中のカラー(Bundle) = nil)

#### RGB

    Color(カラースペース(Color.RGBColorSpace) = .sRGB, red: 赤(Double), green: 緑(Double), blue: 青(Double), opacity: 透明度(Double) = 1)

#### ホワイトポイント

    Color(_カラースペース(Color.RGBColorSpace) = .sRGB, white: ホワイトポイント(Double), opacity: 透明度(Double) = 1)

#### 彩度

    Color(hue: 色合い(Double), saturation: 彩度(Double), brightness: 明るさ(Double), opacity: 透明度(Double) = 1)

### 引数の使い方

#### CGColor

| 名前                                                                                                   | 説明                                    |
| ---------------------------------------------------------------------------------------------------- | ------------------------------------- |
| CGColor(genericCMYKCyan: CGFloat, magenta: CGFloat, yellow: CGFloat, black: CGFloat, alpha: CGFloat) | CMYKカラースペースの色を作成                      |
| CGColor(gray: CGFloat, alpha: CGFloat)                                                               | グレースケールで色を作成                          |
| CGColor(genericGrayGamma2_2Gray: CGFloat, alpha: CGFloat)                                            | ガンマランプが2.2のグレースケールの色を作成               |
| CGColor(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)                                 | RGB色空間で色を作成                           |
| CGColor(srgbRed: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)                             | sRGB色空間の色を作成                          |
| CGColor(colorSpace: CGColorSpace, components: UnsafePointer<CGFloat>)                                | アルファを含む強度値のリストと関連する色空間を用いて色を作成        |
| CGColor(patternSpace: CGColorSpace, pattern: CGPattern, components: UnsafePointer<CGFloat>)          | アルファを含む強度値のリストパターン色空間およびパターンを使用して色を作成 |

#### NSColor

| 名前                          | 説明                             |
| --------------------------- | ------------------------------ |
| NSColor(from: NSPasteboard) | ペーストボードにあるカラーデータからカラーオブジェクトを作成 |

#### UIColor

| 名前                                                                              | 説明                                             |
| ------------------------------------------------------------------------------- | ---------------------------------------------- |
| UIColor(white: CGFloat, alpha: CGFloat)                                         | 指定された透明度とグレースケール値を使ってカラーオブジェクトを作成             |
| UIColor(hue: CGFloat, saturation: CGFloat, brightness: CGFloat, alpha: CGFloat) | 指定された透明度とHSB色空間の成分値を使ってカラーオブジェクトを作成           |
| UIColor(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)            | 指定された透明度とRGB成分の値を使ってカラーオブジェクトを作成              |
| UIColor(displayP3Red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)   | Display P3の色空間で指定された透明度とRGB成分の値でカラーオブジェクトを作成  |
| UIColor(named: String)                                                          | 指定されたアセットの情報を使ってカラーオブジェクトを作成                   |
| UIColor(named: String, in: Bundle?, compatibleWith: UITraitCollection?)         | 指定されたアセットを使用して指定された特性コレクションと互換性のあるカラーオブジェクトを作成 |
| UIColor(dynamicProvider: (UITraitCollection) -> UIColor)                        | 指定されたブロックを使用してカラーデータを動的に生成するカラーオブジェクトを作成       |
| UIColor(Color)                                                                  | SwiftUIの色をカプセル化したカラーオブジェクトを作成                  |
| UIColor(ciColor: CIColor)                                                       | Core Imageのカラーをカプセル化したカラーオブジェクトを作成             |
| UIColor(cgColor: CGColor)                                                       | 指定されたQuartzカラーリファレンスを使用してカラーオブジェクトを作成          |
| UIColor(patternImage: UIImage)                                                  | 指定されたイメージオブジェクトを使ってカラーオブジェクトを作成                |

### 例

#### 基本的な使い方

    Color("background")

### 宣言

    @frozen struct Color

### プロパティ

| 名前          | 型        | 説明                           |
| ----------- | -------- | ---------------------------- |
| primary     | Color    | メインカラー                       |
| secondary   | Color    | サブカラー                        |
| accentColor | Color    | システムまたはアプリのアクセントカラー          |
| black       | Color    | 黒色                           |
| blue        | Color    | 青色                           |
| brown       | Color    | 茶色                           |
| clear       | Color    | 透明色                          |
| cyan        | Color    | シアン色                         |
| gray        | Color    | 灰色                           |
| green       | Color    | 緑色                           |
| indigo      | Color    | インディゴ色                       |
| mint        | Color    | ミント色                         |
| orange      | Color    | オレンジ色                        |
| pink        | Color    | ピンク色                         |
| purple      | Color    | 紫色                           |
| red         | Color    | 赤色                           |
| teal        | Color    | ティール色                        |
| white       | Color    | 白色                           |
| yellow      | Color    | 黄色                           |
| description | String   | インスタンスのテキスト表現                |
| hashValue   | Int      | ハッシュ値                        |
| cgColor     | CGColor? | CGColorが作成できる場合はそのCGColorを返す |

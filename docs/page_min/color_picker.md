---
layout: page
---

### 説明

色を選択するためのコントロール

### 使い方

#### タイトル文字列から生成されたテキストラベルを持つカラーピッカーを作成

    ColorPicker(カラーピッカーのタイトル(StringProtocol または LocalizedStringKey), selection: Colorを含む変数へのバインディング(Binding<Color または CGColor>), supportsOpacity: 透明度を調整できるかどうか(Bool) = true)

#### タイトル文字列キーから生成されたテキストラベルを持つカラーピッカーを作成

    ColorPicker(selection: Colorを含む変数へのバインディング(Binding<Color または CGColor>), supportsOpacity: 透明度を調整できるかどうか(Bool) = true) {
        ラベル
    }

    ColorPicker(selection: Colorを含む変数へのバインディング(Binding<Color または CGColor>), supportsOpacity: 透明度を調整できるかどうか(Bool) = true, label: ラベル)

### 引数の使い方

#### Color

| 名前                                                                                                | 説明                  |
| ------------------------------------------------------------------------------------------------- | ------------------- |
| .primary                                                                                          | メインカラー              |
| .secondary                                                                                        | サブカラー               |
| .accentColor                                                                                      | システムまたはアプリのアクセントカラー |
| .black                                                                                            | 黒色                  |
| .blue                                                                                             | 青色                  |
| .brown                                                                                            | 茶色                  |
| .clear                                                                                            | 透明色                 |
| .cyan                                                                                             | シアン色                |
| .gray                                                                                             | 灰色                  |
| .green                                                                                            | 緑色                  |
| .indigo                                                                                           | インディゴ色              |
| .mint                                                                                             | ミント色                |
| .orange                                                                                           | オレンジ色               |
| .pink                                                                                             | ピンク色                |
| .purple                                                                                           | 紫色                  |
| .red                                                                                              | 赤色                  |
| .teal                                                                                             | ティール色               |
| .white                                                                                            | 白色                  |
| .yellow                                                                                           | 黄色                  |
| Color(Color.RGBColorSpace = .sRGB, red: Double, green: Double, blue: Double, opacity: Double = 1) | 個別作成                |
| Color(Color.RGBColorSpace = .sRGB, white: Double, opacity: Double = 1)                            | 個別作成                |
| Color(hue: Double, saturation: Double, brightness: Double, opacity: Double = 1)                   | 個別作成                |

#### CGColor

| 名前                                                                                                        | 説明                 |
| --------------------------------------------------------------------------------------------------------- | ------------------ |
| CGColor(genericCMYKCyan: CGFloat, magenta: CGFloat, yellow: CGFloat, black: CGFloat, alpha: CGFloat) | CMYKカラースペース        |
| CGColor(gray: CGFloat, alpha: CGFloat)                                                                    | グレースケール            |
| CGColor(genericGrayGamma2_2Gray: CGFloat, alpha: CGFloat)                                                 | ガンマランプが2.2のグレースケール |
| CGColor(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)                                      | RGBカラースペース         |
| CGColor(srgbRed: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)                                  | sRGBカラースペース        |
| CGColor(colorSpace: CGColorSpace, components: UnsafePointer<CGFloat>)                                     | alpha値を含むカラー       |
| CGColor(patternSpace: CGColorSpace, pattern: CGPattern, components: UnsafePointer<CGFloat>)               | アルファ値を含むリストパターン色空間 |

### 例

#### 基本的な使い方

    @State private var bgColor = Color.yellow
    var body: some View {
        VStack {
            ColorPicker("カラーピッカー", selection: $bgColor)
        }
    }

#### 透明度を変更できない

    @State private var bgColor = Color.yellow
    var body: some View {
        VStack {
            ColorPicker("カラーピッカー", selection: $bgColor, supportsOpacity: false)
        }
    }

### 宣言

    struct ColorPicker<Label> where Label : View

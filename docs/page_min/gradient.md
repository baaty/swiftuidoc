---
layout: page
---

### 説明

グラデーションの設定

### 使い方

#### 色の配列からグラデーションを作成

    Gradient(colors: カラー([Color]))

#### カラーストップの配列からグラデーションを作成

    Gradient(stops: カラーストップ([Gradient.Stop]))

### Colorの使い方

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
| Color(String, bundle: Bundle? = nil)                                                              | 色のカスタマイズ            |
| Color(hue: Double, saturation: Double, brightness: Double, opacity: Double = 1)                   | 色のカスタマイズ            |
| Color(Color.RGBColorSpace = .sRGB, white: Double, opacity: Double = 1)                            | 色のカスタマイズ            |
| Color(Color.RGBColorSpace = .sRGB, red: Double, green: Double, blue: Double, opacity: Double = 1) | 色のカスタマイズ            |
| Color(uiColor: UIColor)                                                                           | 色のカスタマイズ            |
| Color(nsColor: NSColor)                                                                           | 色のカスタマイズ            |
| Color(cgColor: CGColor)                                                                           | 色のカスタマイズ            |

### 例

#### 基本的な使い方

    Gradient(colors: [.black, .blue])

### 宣言

    @frozen struct Gradient

### プロパティ

| 名前    | 型               | 説明         |
| ----- | --------------- | ---------- |
| stops | [Gradient.Stop] | カラーストップの配列 |

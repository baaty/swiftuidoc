---
layout: page
---

### 説明

Canvasモード

### 使い方

#### Canvasの作成と設定

    Canvas(opaque: 完全に不透明か(Bool) = false, colorMode: カラーモード(ColorRenderingMode) = .nonLinear, rendersAsynchronously: 親ビューに非同期的に表示できるか(Bool) = false) { 描画先と状態(GraphicsContext), サイズ(CGSize) in
        描画を行うためのクロージャ(Void)
    }

    Canvas(opaque: 完全に不透明か(Bool) = false, colorMode: カラーモード(ColorRenderingMode) = .nonLinear, rendersAsynchronously: 親ビューに非同期的に表示できるか(Bool) = false, renderer: 描画を行うためのクロージャ((描画先と状態(GraphicsContext), サイズ(CGSize)) -> Void))

#### 子ビューを提供するCanvasを作成と設定

    Canvas(opaque: 完全に不透明か(Bool) = false, colorMode: カラーモード(ColorRenderingMode) = .nonLinear, rendersAsynchronously: 親ビューに非同期的に表示できるか(Bool) = false) { 描画先と状態(GraphicsContext), サイズ(CGSize) in
        描画を行うためのクロージャ(Void)

    } symbols: {
        コールバックで使用できる子ビュー(Symbols)
    }

    Canvas(opaque: 完全に不透明か(Bool) = false, colorMode: カラーモード(ColorRenderingMode) = .nonLinear, rendersAsynchronously: 親ビューに非同期的に表示できるか(Bool) = false, renderer: 描画を行うためのクロージャ((描画先と状態(GraphicsContext), サイズ(CGSize)) -> Void), symbols: コールバックで使用できる子ビュー(() -> Symbols))

### 引数の使い方

#### ColorRenderingMode

| 名前              | 説明                 |
| --------------- | ------------------ |
| .extendedLinear | 拡張された線形のsRGB作業用色空間 |
| .linear         | 直線的なsRGBの作業用色空間    |
| .nonLinear      | 非線形のsRGB作業用色空間     |

#### CGSize

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

### 例

#### 基本的な使い方

    Canvas { context, size in
        context.stroke(
            Path(ellipseIn: CGRect(origin: .zero, size: size)),
            with: .color(.green),
            lineWidth: 4)
    }
        .frame(width: 300, height: 200)
        .border(Color.blue)

#### 子ビューあり

    Canvas { context, size in
        if let mark = context.resolveSymbol(id: SymbolID.mark) {
            for rect in rects {
                context.draw(mark, in: rect)
            }
        }
    } symbols: {
        mark.tag(SymbolID.mark)
    }
        .frame(width: 300, height: 200)
        .border(Color.blue)

### 宣言

    struct Canvas<Symbols> where Symbols : View

### プロパティ

| 名前                    | 型                                       | 説明               |
| --------------------- | --------------------------------------- | ---------------- |
| isOpaque              | Bool                                    | 完全に不透明か          |
| colorMode             | ColorRenderingMode                      | カラーモード           |
| symbols               | Symbols                                 | コールバックで使用できる子ビュー |
| rendersAsynchronously | Bool                                    | 親ビューに非同期的に表示できるか |
| renderer              | (inout GraphicsContext, CGSize) -> Void | 描画を行うためのクロージャ    |

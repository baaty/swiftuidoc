---
layout: page
---

### 説明

放射状グラデーション

### 使い方

    RadialGradient(gradient: グラデーション構造体(Gradient), center: 中心(UnitPoint), startRadius: 開始半径(CGFloat), endRadius: 終了半径(CGFloat))

### 引数の使い方

#### Gradient

| 名前                               | 説明                     |
| -------------------------------- | ---------------------- |
| Gradient(colors: [Color])        | 色の配列からグラデーションを作成       |
| Gradient(stops: [Gradient.Stop]) | カラーストップの配列からグラデーションを作成 |

#### UnitPoint

| 名前                                | 説明         |
| --------------------------------- | ---------- |
| .bottom                           | 下          |
| .bottomLeading                    | 左下         |
| .bottomTrailing                   | 右下         |
| .center                           | 中央        |
| .leading                          | 左          |
| .top                              | 上          |
| .topLeading                       | 左上         |
| .topTrailing                      | 右上         |
| .trailing                         | 右          |
| .zero                             | 0          |
| UnitPoint()                       | 作成         |
| UnitPoint(x: CGFloat, y: CGFloat) | xとyを指定して作成 |

### 例

#### 基本的な使い方

    RadialGradient(gradient: Gradient(colors: [.red]), center:.bottom, startRadius: 0, endRadius: 10)

### 宣言

    @frozen struct RadialGradient

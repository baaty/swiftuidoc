---
layout: page
---

### 説明

パスで構成された線を描画

### 使い方

#### 空のパスを作成

    Path()

#### 空のパスを作成しクロージャを実行して初期要素を追加

    Path {
        コールバック
    }

    Path(コールバック)

#### コピーからパスを作成

    Path(パス(CGMutablePath))

#### 不変のシェイプパスからパスを作成

    Path(パス(CGPath))

#### 以前のPath.stringRepresentationの呼び出しの結果から初期化

    Path(文字列(String))

#### 与えられた矩形のパスを作成

    Path(矩形(CGRect))

#### 与えられた矩形に内接する楕円のパスを作成

    Path(ellipseIn: 矩形(CGRect))

#### 与えられた丸みを帯びた四角形のパスを作成

    Path(roundedRect: 丸みを帯びた矩形(CGRect), cornerRadius: 半径(CGFloat), style: スタイル(RoundedCornerStyle) = .circular)

    Path(roundedRect: 丸みを帯びた矩形(CGRect), cornerSize: サイズ(CGSize), style: スタイル(RoundedCornerStyle) = .circular)

### 例

#### 基本的な使い方

    Path()

### プロパティ

| 名前             | 型                   | 説明                         |
| -------------- | ------------------- | -------------------------- |
| animatableData | EmptyAnimatableData | アニメーションするためのデータ            |
| boundingRect   | CGRect              | すべてのパスを含む矩形                |
| cgPath         | CGPath              | パス内の要素を表す不変のパス             |
| currentPoint   | CGPoint?            | パスの最後のポイント                 |
| description    | String              | パスを再作成する際に使用される可能性のあるパスの説明 |
| isEmpty        | Bool                | 空かどうか                      |

### メソッド

| 名前             | 説明                          |
| -------------- | --------------------------- |
| addArc         | 半径と角度で指定した円の弧をパスに追加         |
| addCurve       | 三次ベジエ曲線をパスに追加               |
| addEllipse     | パスに楕円を追加                    |
| addLine        | 現在の点から指定した点までの直線パスを追加       |
| addLines       | パスに一連の接続された直線パスを追加          |
| addPath        | 与えられたパスのコピーをこのパスに追加         |
| addQuadCurve   | 指定された終点と制御点を持つ二次ベジエ曲線をパスに追加 |
| addRect        | パスに長方形のサブパスを追加              |
| addRects       | 矩形のサブパスの列をパスに追加             |
| addRelativeArc | 半径と角度の差で指定した円の弧をパスに追加       |
| addRoundedRect | パスに丸みを帯びた矩形を追加              |
| applying       | パスに対してアフィン変換を適用             |
| closeSubpath   | 現在のサブパスを閉じて完了               |
| contains       | パスに指定したポイントが含まれているか         |
| forEach        | パスの各要素でボディを呼び出し             |
| move           | 指定されたポイントで新しいサブパスを開始        |
| offsetBy       | (dx, dy)だけ平行移動させたパス         |
| strokedPath    | パスのストロークされたコピー              |
| trimmedPath    | パスの部分的なコピー                  |

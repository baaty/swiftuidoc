---
layout: page
---

### 説明

テキストを表示するビュー

### 使い方

#### キーで指定されたローカライズされたコンテンツを表示するテキストビューを作成

    Text(ローカライズされた文字列キー(LocalizedStringKey), tableName: "ローカライズ用のkey-valueファイル名" = nil, bundle: バンドル名(Bundle) = nil, comment: "key-valueに関するコンテキスト情報(StaticString)" = nil)

#### 保存されている文字列をローカライズせずに表示するテキストビューを作成

    Text(テキスト(StringProtocol))

#### ローカライズされていない文字列リテラルを表示するテキストビューを作成

    Text(verbatim: "テキスト")

#### 他のテキストとの連結に適したイメージをラップしたインスタンスを作成

    Text(画像(Image))

#### 2つの日付間の範囲をローカライズして表示するインスタンスを作成

    Text(日付の範囲指定(ClosedRange<Date>))

#### ローカライズされた時間間隔を表示するインスタンスを作成

    Text(時間間隔(DateInterval))

#### 特定のスタイルでローカライズされた日付と時刻を表示するインスタンスを作成

    Text(日付(Date), style: 日付のスタイル(Text.DateStyle))

### 引数の使い方

#### Text.DateStyle

| 名前        | 説明                          |
| --------- | --------------------------- |
| .date     | 日付を表示するスタイル                 |
| .offset   | 日付を現在からのオフセットで表示するスタイル      |
| .relative | 日付を現在からの相対値で表示するスタイル        |
| .time     | 日付の時間要素のみを表示するスタイル          |
| .timer    | 日付を今からカウントするタイマーとして表示するスタイル |

### 例

#### 直接テキストを記述

    Text("ほげ")

#### ローカライズするstringファイルなどを指定

    Text("ほげ" , tableName: Localizable.strings, bundle: bundle, comment: "コメント")

#### ローカライズしないテキストを記述

    Text(verbatim: "ほげ")

#### 保存されたテキストを記述

    let s = "ほげ"
    Text(s)

#### 画像を記述

    Text(Image("hoge"))

#### 日付の範囲を記述

    Text(Date(), style: .date)
    // 2021年9月14日

#### 時間間隔を記述

    Text(DateInterval(start: event.startDate, duration: event.duration))
    // 9:30AM - 3:30PM

### 補足

少しわかりにくいので補足しておくと、変数などに保存されたテキストは多言語化されないが、直接テキストを記述した場合は多言語化される。多言語化したくないテキストはverbatimに記述
また保存されたテキストを多言語化したい場合はLocalizedStringKeyを使う
もちろん多言語化はアプリで多言語対応している場合のみなので、ちょこっとアプリを作るだけなら気にしなくていいと思います

### 宣言

    @frozen struct Text

### メソッド

| 名前                                 | 説明                             |
| ---------------------------------- | ------------------------------ |
| font                               | フォントを設定                        |
| fontWeight                         | フォントの太さ                        |
| foregroundColor                    | テキストの色                         |
| bold                               | テキストの太さ                        |
| italic                             | イタリック                          |
| strikethrough                      | 打ち消し線                          |
| underline                          | 下線                             |
| kerning                            | 文字の間隔                          |
| tracking                           | トラッキング                         |
| baselineOffset                     | 垂直オフセット                        |
| textCase                           | 大文字・小文字を変換                     |
| allowsTightening                   | 文字間のスペースを圧縮できるかどうかを設定          |
| minimumScaleFactor                 | 使用可能なスペースに収まるように縮小する最小値を設定     |
| truncationMode                     | スペースに収まらないテキストの切り捨てモードを設定      |
| lineLimit                          | テキストの最大行数                      |
| lineSpacing                        | 行間のスペースを設定                     |
| multilineTextAlignment             | 複数行テキストの配置を設定                  |
| flipsForRightToLeftLayoutDirection | レイアウト方向が右から左の場合に水平に反転するかどうかを設定 |

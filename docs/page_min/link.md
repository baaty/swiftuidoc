---
layout: page
---

### 説明

URLに移動するためのコントロール

### 使い方

#### URLとタイトルキーで構成されたURLへの移動に使用されるコントロールを作成

    Link("URL名(StringProtocol)", destination: リンク(URL))

#### URLとタイトル文字列で構成されたURLへの移動に使用されるコントロールを作成

    Link(ローカライズされた文字列キー(LocalizedStringKey), destination: リンク(URL))

    Link(destination: リンク(URL)) {
        ラベル(Label)
    }

#### 指定されたURLに移動するためのURLとラベルで構成されるコントロールを作成

    Link(destination: リンク(URL), label: ラベル)

### 引数の使い方

#### URL

| 名前                                                                                                                                      | 説明                                              |
| --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| URL(string: String)!                                                                                                                    | 指定された文字列からURLインスタンスを作成                          |
| URL(string: String, relativeTo: URL?)!                                                                                                  | 指定された文字列から別のURLに相対するURLインスタンスを作成                |
| URL(fileURLWithPath: String)                                                                                                            | ローカルのファイルやディレクトリを参照するファイルURLを作成                 |
| URL(fileURLWithPath: String, isDirectory: Bool)                                                                                         | ローカルのファイルやディレクトリを参照するファイルURLを作成                 |
| URL(fileURLWithPath: String, relativeTo: URL?)                                                                                          | ベースURLからの相対パスでローカルのファイルまたはディレクトリを参照するファイルURLを作成 |
| URL(fileURLWithPath: String, isDirectory: Bool, relativeTo: URL?)                                                                       | ベースURLからの相対パスでローカルのファイルまたはディレクトリを参照するファイルURLを作成 |
| URL(fileURLWithFileSystemRepresentation: UnsafePointer<Int8>, isDirectory: Bool, relativeTo: URL?)                                      | パスのファイルシステム表現でローカルファイルまたはディレクトリを参照するURL         |
| URL(fileReferenceLiteralResourceName: String)                                                                                           | プレイグラウンドファイルリテラルからURLを作成                        |
| URL(resolvingBookmarkData: Data, options: URL.BookmarkResolutionOptions = \[], relativeTo: URL? = nil, bookmarkDataIsStale: inout Bool) | ブックマークデータを解決して指定された場所を参照するURLを作成                |
| URL(resolvingAliasFileAt: URL, options: URL.BookmarkResolutionOptions = \[])                                                            | エイリアスファイルを解決して指定された場所を参照するURLを作成                |
| URL(from decoder: Decoder)                                                                                                              | 符号化された表現をデコードしてURLを作成                           |
| URL(dataRepresentation: Data, relativeTo: URL?, isAbsolute: Bool = false)!                                                              | 指定されたデータの内容を使ってベースとなるURLを基準にして新しく作成されたURLを初期化   |

### 例

#### 基本的な使い方

    Link("リンクテキスト", destination: URL(string: "https://www.example.com/")!)

#### ボタン風リンク

    Link(destination: URL(string: "https://www.example.com/")!, label: {
        HStack {
            Image(systemName: "hand.thumbsup")
            Text("ボタン風リンク")
        }
            .foregroundColor(.white)
            .padding()
            .padding(.horizontal)
            .background(Capsule()
            .fill(Color.red)
            .shadow(radius: 4, y: 8))
    })

### 宣言

    struct Link<Label> where Label : View

### メソッド

| 名前              | 説明      |
| --------------- | ------- |
| font            | フォントを設定 |
| foregroundColor | 前景色     |

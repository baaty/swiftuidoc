---
layout: page
---

### 説明

アフィン変換が適用された形状

### 使い方

    TransformedShape(shape: 図形(Content), transform: アフィン変換行列(CGAffineTransform))

### 例

#### 基本的な使い方

    TransformedShape(shape: Circle(), transform: CGAffineTransform())

### 宣言

    @frozen struct TransformedShape<Content> where Content : Shape

### プロパティ

| 名前             | 型                                   | 説明              |
| -------------- | ----------------------------------- | --------------- |
| animatableData | ScaledShape<Content>.AnimatableData | アニメーションするためのデータ |
| animatableData | EmptyAnimatableData                 | アニメーションするためのデータ |
| shape          | Content                             | 図形              |
| transform      | CGAffineTransform                   | トランスフォーム        |

### ビュー共通メソッド

| 名前                                 | 説明                                                    |
| ---------------------------------- | ----------------------------------------------------- |
| accessibilityLabel                 | その内容を表すラベルを追加                                         |
| accessibilityInputLabels           | 代替入力ラベルを設定                                            |
| accessibilityLabeledPair           | アクセシビリティ要素と一致するコンテンツを表す要素をペアで設定                       |
| accessibilityValue                 | テキストによる説明を追加                                          |
| accessibilityHint                  | 実行した後に何が起こるかをユーザーに説明                                  |
| accessibilityActivationPoint       | アクティベーションが発生するポイントを指定                                 |
| accessibilityAction                | アクセシビリティアクションを追加                                      |
| accessibilityAdjustableAction      | アクセシビリティ調整可能なアクションをビューに追加                             |
| accessibilityScrollAction          | ユーザー補助のスクロールアクションをビューに追加                              |
| accessibilityElement               | 新しいアクセシビリティ要素としてラップ                                   |
| accessibilityLinkedGroup           | 複数のアクセシビリティ要素をリンク                                     |
| accessibilitySortPriority          | アクセシビリティ要素のソート優先順位を設定                                 |
| accessibilityHidden                | アクセシビリティ機能から非表示にするかどうかを指定                             |
| accessibilityAddTraits             | Traitsビューを追加                                          |
| accessibilityRemoveTraits          | Traitsビューを削除                                          |
| accessibilityIdentifier            | 指定された文字列をビューの識別に使用                                    |
| accessibilityIgnoresInvertColors   | Smart Invert Colors設定を無視するかどうかを設定                     |
| textCase                           | 大文字・小文字を変換                                            |
| allowsTightening                   | 文字間のスペースを圧縮できるかどうかを設定                                 |
| minimumScaleFactor                 | 使用可能なスペースに収まるように縮小する最小値を設定                            |
| truncationMode                     | スペースに収まらないテキストの切り捨てモードを設定                             |
| flipsForRightToLeftLayoutDirection | レイアウト方向が右から左の場合に水平に反転するかどうかを設定                        |
| lineLimit                          | テキストの最大行数                                             |
| lineSpacing                        | 行間のスペースを設定                                            |
| multilineTextAlignment             | 複数行テキストの配置を設定                                         |
| keyboardType                       | キーボードタイプを設定                                           |
| disableAutocorrection              | 自動修正を無効にするかどうかを設定                                     |
| autocapitalization                 | 自動大文字を適用するかどうかを設定                                     |
| textContentType                    | テキストコンテンツタイプを設定                                       |
| labelsHidden                       | コントロールのラベルを非表示                                        |
| defaultWheelPickerItemHeight       | デフォルトのホイールスタイルのピッカーアイテムの高さを設定                         |
| horizontalRadioGroupLayout         | ラジオグループスタイルピッカーのスタイルが水平方向に配置されるように設定                  |
| controlSize                        | コントロールのサイズを設定                                         |
| listRowInsets                      | リストの行にインセットを適用                                        |
| listRowBackground                  | カスタムの背景ビューをリストの行アイテムの背後に配置                            |
| listItemTint                       | Tint効果を設定                                             |
| navigationTitle                    | ナビゲーションのタイトルを設定                                       |
| navigationSubtitle                 | ナビゲーションのサブタイトルを設定                                     |
| navigationBarHidden                | ナビゲーションバーを非表示                                         |
| navigationBarBackButtonHidden      | ビューのナビゲーションバーの戻るボタンを非表示                               |
| navigationBarTitleDisplayMode      | タイトル表示モードを設定                                          |
| toolbar                            | ツールバーやナビゲーションバーに入力されたビューを表示                           |
| tabItem                            | タブバーに表示するビューを指定                                       |
| help                               | ヘルプテキストを追加                                            |
| contextMenu                        | コンテキストメニューをビューに追加                                     |
| statusBar                          | ステータスバーの可視性を設定                                        |
| touchBar                           | タッチバーを設定                                              |
| touchBarItemPrincipal              | タッチバーに特別な意味を持つ主要なビューを設定                               |
| touchBarCustomizationLabel         | ビューの機能を識別するユーザーに表示される文字列を設定                           |
| touchBarItemPresence               | ユーザーがカスタマイズしたビューの動作を設定                                |
| buttonStyle                        | ボタンのスタイル                                              |
| menuStyle                          | メニューのスタイルを設定                                          |
| pickerStyle                        | ピッカーのスタイルを設定                                          |
| datePickerStyle                    | 日付ピッカーのスタイルを設定                                        |
| textFieldStyle                     | テキストフィールドのスタイルを設定                                     |
| toggleStyle                        | トグルのスタイルを設定                                           |
| listStyle                          | リストのスタイルを設定                                           |
| navigationViewStyle                | ナビゲーションビューのスタイルを設定                                    |
| tabViewStyle                       | タブのスタイル設定                                             |
| labelStyle                         | ラベルのスタイル                                              |
| progressViewStyle                  | プログレスビューのスタイルを設定                                      |
| indexViewStyle                     | インデックスビューのスタイルを設定                                     |
| groupBoxStyle                      | グループボックスのスタイルを設定                                      |
| gaugeStyle                         | ゲージのスタイルを設定                                           |
| presentedWindowStyle               | インタラクションで作成されるウィンドウのスタイルを設定                           |
| presentedWindowToolbarStyle        | インタラクションで作成されるウィンドウのツールバーのスタイルを設定                     |
| frame                              | 指定されたサイズに設定                                           |
| fixedSize                          | 最適なサイズに修正                                             |
| layoutPriority                     | 親レイアウトがこの子にスペースを配分する優先順位を設定                           |
| position                           | 親の座標空間のに配置                                            |
| offset                             | 水平および垂直のオフセット                                         |
| coordinateSpace                    | 座標空間に名前を割り当て                                          |
| alignmentGuide                     | 水平方向また垂直方向の配置を設定                                      |
| padding                            | パディング                                                 |
| overlay                            | 前にセカンダリビューを重ねる                                        |
| background                         | ビューの背景に設定                                             |
| zIndex                             | 重なり合うビューの表示順序を制御                                      |
| border                             | 指定されたスタイルと幅で境界線を追加                                    |
| accentColor                        | アクセントカラーを設定                                           |
| preferredColorScheme               | 優先カラースキームを設定                                          |
| unredacted                         | リダクションを適用する理由をすべて削除                                   |
| mask                               | 指定されたビューのアルファチャネルを使用してマスク                             |
| clipped                            | 長方形のフレームに切り取る                                         |
| clipShape                          | クリッピング形状を設定                                           |
| cornerRadius                       | 指定されたコーナー半径で境界フレームを切り取る                               |
| scaledToFill                       | スケーリングしてその親を塗りつぶします                                   |
| scaledToFit                        | スケーリングして親に合わせます                                       |
| scaleEffect                        | レンダリングされた出力をアンカーポイントを基準にしてスケーリング                      |
| imageScale                         | 利用可能な相対サイズの1つに従ってビュー内の画像を拡大縮小                         |
| aspectRatio                        | 寸法を指定した値で制限                                           |
| rotationEffect                     | 指定された点を中心に回転                                          |
| rotation3DEffect                   | レンダリングされた出力を指定された回転軸を中心に3次元で回転                        |
| projectionEffect                   | レンダリングされた出力に投影変換を適用                                   |
| transformEffect                    | レンダリングされた出力にアフィン変換を適用                                 |
| blur                               | ガウスぼかしを適用                                             |
| opacity                            | 透明度を設定                                                |
| brightness                         | 指定された値だけ明るくします                                        |
| contrast                           | 類似色間のコントラストと分離を設定                                     |
| colorInvert                        | 色を反転                                                  |
| colorMultiply                      | 色乗算効果を追加                                              |
| saturation                         | 彩度を調整                                                 |
| grayscale                          | グレースケール効果を追加                                          |
| hueRotation                        | 色相回転効果を適用                                             |
| luminanceToAlpha                   | アルファ効果に輝度を追加                                          |
| shadow                             | 影を追加                                                  |
| blendMode                          | ブレンドモードを設定                                            |
| compositingGroup                   | 合成グループにラップ                                            |
| drawingGroup                       | 最終的な表示の前にコンテンツをオフスクリーンイメージに合成                         |
| animation                          | アニメーション                                               |
| transition                         | 遷移をビューに関連付けます                                         |
| matchedGeometryEffect              | 指定された識別子と名前空間を使用してジオメトリが同期したビューグループを定義                |
| hidden                             | ビューを非表示                                               |
| disabled                           | ユーザーが操作できるかどうかを制御する条件を追加                              |
| handlesExternalEvents              | 含まれるシーンが一致する外部イベントを処理できることを示す修飾子を指定                   |
| onTapGesture                       | タップジェスチャーを認識したときに実行するアクションを追加                         |
| onLongPressGesture                 | 長押しジェスチャーを認識したときに実行するアクションを追加                         |
| gesture                            | 定義されたジェスチャよりも優先順位が低いジェスチャをビューにアタッチ                    |
| highPriorityGesture                | 定義されたジェスチャよりも優先度の高いジェスチャをビューにアタッチ                     |
| simultaneousGesture                | 定義されたジェスチャーと同時に処理するジェスチャーをビューにアタッチ                    |
| transaction                        | 指定されたトランザクション変更関数をビュー内で使用されるすべてのトランザクションに適用           |
| userActivity                       | ユーザーのアクティビティタイプを広告                                    |
| onContinueUserActivity             | 指定されたアクティビティタイプを受信したときに呼び出すハンドラを登録                    |
| onCopyCommand                      | システムのコピーコマンドに応じて実行するアクションを追加                          |
| onCutCommand                       | システムのCutコマンドに応答して実行するアクションを追加                         |
| onPasteCommand                     | システムのPasteコマンドに対応して実行するアクションを追加                       |
| onDrag                             | ドラッグアンドドロップ操作のソースとしてアクティブ                             |
| itemProvider                       | 特定のデータ要素に使用されるドラッグ表現を提供するクロージャを提供                     |
| onOpenURL                          | URLを受信したときに起動するハンドラを登録                                |
| onMoveCommand                      | 矢印キーを押したときやApple TVを制御しているときになど移動コマンドに応じて実行するアクションを追加 |
| moveDisabled                       | ビュー階層が移動可能かどうかの条件を追加                                  |
| onDeleteCommand                    | システムの削除コマンドに応じて実行するアクションを追加                           |
| deleteDisabled                     | ビュー階層が削除可能かどうかの条件を追加                                  |
| pageCommand                        | ページアップやページダウンのコマンドに応じて値を範囲内でステップ                      |
| onExitCommand                      | フォーカスがあるときにexitコマンドの受信に応答してトリガーされるアクションを設定            |
| onPlayPauseCommand                 | システムの再生/一時停止コマンドに応答して実行するアクションを追加                     |
| onCommand                          | 指定されたセレクターに応答して実行するアクションを追加                           |
| onAppear                           | 表示されたときに実行するアクションを追加                                  |
| onDisappear                        | 非表示になった時に実行するアクションを追加                                 |
| onChange                           | 特定の値が変化したときにアクションを発生させるメソッドを追加                        |
| onReceive                          | 特定のパブリッシャーによって発行されたデータを検出したときに実行するアクションを追加            |
| keyboardShortcut                   | 変更したコントロールにキーボードショートカットを割り当て                          |
| onHover                            | ユーザーがポインターをビューのフレームの上または外に移動したときに実行するアクションを追加         |
| hoverEffect                        | ポインターホバー効果を適用                                         |
| focusable                          | フォーカス可能かどうかを指定し可能であればビューがフォーカスされたときに実行するアクションを追加      |
| focusedValue                       | フォーカスされたビュー階層に状態が依存する他のビューが使用するために提供する値を注入して変更        |
| prefersDefaultFocus                | ネームスペースのデフォルトでフォーカスされることを好むかどうかを設定                    |
| focusScope                         | デフォルトのフォーカス設定を制限するために使用できるフォーカススコープを作成                |
| digitalCrownRotation               | 指定されたバインディングを更新することによりデジタルクラウンの回転を追跡                  |
| allowsHitTesting                   | ヒットテスト操作に参加するかどうかを構成                                  |
| contentShape                       | ヒットテストのコンテンツ形状を定義                                     |
| actionSheet                        | アクションシートを表示                                           |
| sheet                              | シートを表示                                                |
| fullScreenCover                    | 指定したブール値へのバインディングがtrueの場合に画面をできるだけ多く覆うモーダルビューを提示      |
| alert                              | ユーザーに警告を表示                                            |
| popover                            | ポップオーバーを表示                                            |
| fileExporter                       | メモリ内の文書をディスク上のファイルに書き出すためのシステムインターフェースを提供             |
| fileImporter                       | ユーザーが複数のファイルを取り込むためのシステムインターフェースを提供                   |
| fileMover                          | ユーザーが既存のファイルを新しい場所に移動させるためのシステムインターフェースを提供            |
| tag                                | 一意のタグ値を設定                                             |
| id                                 | IDを指定されたプロキシ値にバインド                                    |
| equatable                          | 新しい値が古い値と同じ場合にビューが子ビューを更新しないようにします                    |
| defaultAppStorage                  | ビューに含まれるAppStorageが使用するデフォルトのストア                      |
| preference                         | 指定された設定の値を設定                                          |
| transformPreference                | 設定値に変換を適用                                             |
| anchorPreference                   | アンカー設定                                                |
| transformAnchorPreference          | アンカー設定の変更                                             |
| onPreferenceChange                 | 指定された設定キーの値が変更されたときに実行するアクションを追加                      |
| backgroundPreferenceValue          | 指定された設定値を使用して別のビューを最初のビューの背景として作成                     |
| overlayPreferenceValue             | 指定された設定値を使用して別のビューを最初のビューの上にオーバーレイとして作成               |
| environment                        | 指定されたキーパスの環境値を指定された値に設定                               |
| environmentObject                  | 用品ビューsubhierachyにObservableObject                     |
| transformEnvironment               | 指定された関数を使用して指定されたキーパスの環境値を変換                          |
| previewDevice                      | プレビューに使用するデバイスを設定                                     |
| previewDisplayName                 | エディターに表示されるユーザーに表示される名前を提供                            |
| previewLayout                      | プレビュー用のコンテナのサイズを上書き                                   |
| previewContext                     | プレビュー用のコンテキストを宣言                                      |
| modifier                           | 修飾子をビューに適用                                            |

### シェイプ共通メソッド

| 名前        | 説明                              |
| --------- | ------------------------------- |
| path      | パスを描画                           |
| trim      | パスとしての表現に基づいた小数の量でトリミング         |
| transform | アフィン変換を適用                       |
| size      | サイズのある長方形からパスを作成                |
| scale     | バウンディングフレームを変更することなくこの図形をスケーリング |
| rotation  | アンカーポイントを中心に指定した角度で図形を回転        |
| offset    | 指定されたサイズでこの図形の相対的な位置を変更         |
| stroke    | 輪郭を色やグラデーションで描画                 |
| fill      | 色やグラデーションで塗りつぶす                 |

### メソッド詳細

#### accessibilityLabel

##### 意味

その内容を表すラベルを追加

##### 使い方

    .accessibilityLabel("ラベル名(StringProtocol)")

    .accessibilityLabel(ラベル(Text))

    .accessibilityLabel(ローカライズされた文字列キー(LocalizedStringKey))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityLabel("ラベル")

#### accessibilityInputLabels

##### 意味

代替入力ラベルを設定

##### 使い方

    .accessibilityInputLabels(代替入力ラベルの配列([StringProtocol]))

    .accessibilityInputLabels(代替入力ラベルの配列([Text]))

    .accessibilityInputLabels(ローカライズされた文字列キーの配列([LocalizedStringKey]))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityInputLabels(["ラベル"])

#### accessibilityLabeledPair

##### 意味

アクセシビリティ要素と一致するコンテンツを表す要素をペアで設定

##### 使い方

    .accessibilityLabeledPair(role: ラベルかコンテンツ(AccessibilityLabeledPairRole), id: "識別子", in: "ネームスペース")

##### AccessibilityLabeledPairRoleの使い方

| 名前       | 説明      |
| -------- | ------- |
| .content | コンテンツ部分 |
| .label   | ラベル部分   |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityLabeledPair(role: .label, id: "hogeControls", in: hogeNamespace)

#### accessibilityValue

##### 意味

テキストによる説明を追加

##### 使い方

    .accessibilityValue("説明テキスト(StringProtocol)")

    .accessibilityValue(説明テキスト(Text))

    .accessibilityValue(ローカライズされた文字列キー(LocalizedStringKey))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityValue("hoge")

#### accessibilityHint

##### 意味

実行した後に何が起こるかをユーザーに説明

##### 使い方

    .accessibilityHint("説明テキスト(StringProtocol")

    .accessibilityHint(説明テキスト(Text))

    .accessibilityHint(ローカライズされた文字列キー(LocalizedStringKey))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityHint("説明テキスト")

#### accessibilityAction

##### 意味

アクセシビリティアクションを追加

##### 使い方

    .accessibilityAction("アクション名(StringProtocol)" = .default) {
        アクセシビリティアクション
    }

    .accessibilityAction("アクション名(StringProtocol)" = .default, アクセシビリティアクション)

    .accessibilityAction(アクション名(AccessibilityActionKind) = .default) {
        アクセシビリティアクション
    }

    .accessibilityAction(アクション名(AccessibilityActionKind) = .default, アクセシビリティアクション)

    .accessibilityAction(named: 名前(Text)) {
        カスタムアクセシビリティアクション
    }

    .accessibilityAction(named: 名前(Text), カスタムアクセシビリティアクション)

    .accessibilityAction(named: ローカライズされた文字列キー(LocalizedStringKey)) {
        カスタムアクセシビリティアクション
    }

    .accessibilityAction(named: ローカライズされた文字列キー(LocalizedStringKey), カスタムアクセシビリティアクション)

##### AccessibilityActionKindの使い方

| 名前        | 説明       |
| --------- | -------- |
| .default  | デフォルト    |
| .delete   | Delete   |
| .escape   | Escape   |
| .magicTap | MagicTap |
| .showMenu | ShowMenu |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityAction(.default) {
            // アクション
        }

#### accessibilityAdjustableAction

##### 意味

アクセシビリティ調整可能なアクションをビューに追加

##### 使い方

    .accessibilityAdjustableAction() { 調整を行う際に使用する方向指示(AccessibilityAdjustmentDirection) in
        アクセシビリティ調整可能なアクション
    }

    .accessibilityAdjustableAction(アクセシビリティ調整可能なアクション)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityAdjustableAction { _ in
            // アクション
        }

#### accessibilityScrollAction

##### 意味

ユーザー補助のスクロールアクションをビューに追加

##### 使い方

    .accessibilityScrollAction() { 辺(Edge)
        ユーザー補助のスクロールアクション
    }

    .accessibilityScrollAction(ユーザー補助のスクロールアクション)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityScrollAction { _ in
            // アクション
        }

#### accessibilityActivationPoint

##### 意味

アクティベーションが発生するポイントを指定

##### 使い方

    .accessibilityActivationPoint(アクティベーションが発生するポイント(CGPoint))

    .accessibilityActivationPoint(アクティベーションが発生するポイント(UnitPoint))

##### CGPointの使い方

| 名前                              | 説明                       |
| ------------------------------- | ------------------------ |
| CGPoint()                       | 位置(0,0)の点を作成             |
| CGPoint(x: Double, y: Double)   | 浮動小数点値で指定された座標を持つ点を作成    |
| CGPoint(x: Int, y: Int)         | 整数値で指定された座標を持つ点を作成       |
| CGPoint(x: CGFloat, y: CGFloat) | CGFloatの値で指定された座標を持つ点を作成 |
| CGPoint.zero                    | 位置(0,0)の点                |

##### UnitPointの使い方

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

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityActivationPoint(.bottom)

#### accessibilityElement

##### 意味

新しいアクセシビリティ要素としてラップ

##### 使い方

    .accessibilityElement(children: アクセシビリティ要素(AccessibilityChildBehavior) = .ignore)

##### AccessibilityChildBehaviorの使い方

| 名前       | 説明      |
| -------- | ------- |
| .combine | Combine |
| .contain | Contain |
| .ignore  | Ignore  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityElement(children: .combine)

#### accessibilityLinkedGroup

##### 意味

複数のアクセシビリティ要素をリンク

##### 使い方

    .accessibilityLinkedGroup(id: 識別子(Hashable), in: ネームスペース(Namespace.ID))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityLinkedGroup(id: "id", in: namespace)

#### accessibilitySortPriority

##### 意味

アクセシビリティ要素のソート優先順位を設定

##### 使い方

    .accessibilitySortPriority(優先順位(Double))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilitySortPriority(2)

#### accessibilityHidden

##### 意味

アクセシビリティ機能から非表示にするかどうかを指定

##### 使い方

    .accessibilityHidden(非表示にするかどうか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityHidden(true)

#### accessibilityAddTraits

##### 意味

Traitsビューを追加

##### 使い方

    .accessibilityAddTraits(Traitsビュー(AccessibilityTraits))

##### AccessibilityTraitsの使い方

| 名前                       | 説明                                      |
| ------------------------ | --------------------------------------- |
| .allowsDirectInteraction | VoiceOverユーザーが直接タッチ操作できるようにする           |
| .causesPageTurn          | VoiceOverがテキストを読み終えたときに自動的にページをめくるようにする |
| .isButton                | ボタン                                     |
| .isHeader                | コンテンツをセクションに分けるためのヘッダー                  |
| .isImage                 | 画像                                      |
| .isKeyboardKey           | キーボードのキーのように動作                          |
| .isLink                  | リンク                                     |
| .isModal                 | モーダル                                    |
| .isSearchField           | 検索エリア                                   |
| .isSelected              | 選択エリア                                   |
| .isStaticText            | ユーザーが変更できないテキスト                         |
| .isSummaryElement        | サマリー要素                                  |
| .playsSound              | 起動時に独自のサウンドを再生                          |
| .startsMediaSession      | アクティブになるとメディアセッションを開始                   |
| .updatesFrequently       | ラベルや値を頻繁に更新                             |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityAddTraits(.isButton)

#### accessibilityRemoveTraits

##### 意味

Traitsビューを削除

##### 使い方

    .accessibilityRemoveTraits(Traitsビュー(AccessibilityTraits))

##### AccessibilityTraitsの使い方

| 名前                       | 説明                                      |
| ------------------------ | --------------------------------------- |
| .allowsDirectInteraction | VoiceOverユーザーが直接タッチ操作できるようにする           |
| .causesPageTurn          | VoiceOverがテキストを読み終えたときに自動的にページをめくるようにする |
| .isButton                | ボタン                                     |
| .isHeader                | コンテンツをセクションに分けるためのヘッダー                  |
| .isImage                 | 画像                                      |
| .isKeyboardKey           | キーボードのキーのように動作                          |
| .isLink                  | リンク                                     |
| .isModal                 | モーダル                                    |
| .isSearchField           | 検索エリア                                   |
| .isSelected              | 選択エリア                                   |
| .isStaticText            | ユーザーが変更できないテキスト                         |
| .isSummaryElement        | サマリー要素                                  |
| .playsSound              | 起動時に独自のサウンドを再生                          |
| .startsMediaSession      | アクティブになるとメディアセッションを開始                   |
| .updatesFrequently       | ラベルや値を頻繁に更新                             |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityRemoveTraits(.isButton)

#### accessibilityIdentifier

##### 意味

指定された文字列をビューの識別に使用

##### 使い方

    .accessibilityIdentifier("識別子")

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityIdentifier("home")

#### accessibilityIgnoresInvertColors

##### 意味

Smart Invert Colors設定を無視するかどうかを設定

##### 使い方

    .accessibilityIgnoresInvertColors(mart Invert Colors設定を無視するかどうか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accessibilityIgnoresInvertColors(true)

#### textCase

##### 意味

大文字・小文字を変換

##### 使い方

    .textCase(変換方式(Text.Case))

    .textCase()

##### Text.Caseの使い方

| 名前         | 説明     |
| ---------- | ------ |
| .lowercase | すべて小文字 |
| .uppercase | すべて大文字 |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .textCase(.lowercase)

#### allowsTightening

##### 意味

テキストを1行に収めるために必要な場合に文字間のスペースを圧縮できるかどうかを設定

##### 使い方

    .allowsTightening(スペースを必要に応じて圧縮するか(Bool))

##### 例

    Button("テキストテキストテキスト")
        .allowsTightening(true)

#### minimumScaleFactor

##### 意味

使用可能なスペースに収まるように縮小する最小値を設定

##### 使い方

    .minimumScaleFactor(テキストスケーリングの最小値(CGFloat))

##### 補足

指定できる数値は0から1の間

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .minimumScaleFactor(0.5)

#### truncationMode

##### 意味

長すぎて使用可能なスペースに収まらないテキスト行の切り捨てモードを設定

##### 使い方

    .truncationMode(切り捨てモード(Text.TruncationMode))

##### Text.TruncationModeの使い方

| 名前      | 説明        |
| ------- | --------- |
| .head   | 行頭で切り捨て   |
| .middle | 行の途中で切り捨て |
| .tail   | 行の最後で切り捨て |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .truncationMode(.tail)

#### flipsForRightToLeftLayoutDirection

##### 意味

レイアウト方向が右から左の場合コンテンツを水平に反転するかどうかを設定

##### 使い方

    .flipsForRightToLeftLayoutDirection(水平に反転するかどうか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .flipsForRightToLeftLayoutDirection(true)

#### lineLimit

##### 意味

テキストの最大行数

##### 使い方

    .lineLimit(行数(Int))

    .lineLimit()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .lineLimit(10)

#### lineSpacing

##### 意味

行間のスペースを設定

##### 使い方

    .lineSpacing(スペース(CGFloat))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .lineSpacing(10)

#### multilineTextAlignment

##### 意味

複数行テキストの配置を設定

##### 使い方

    .multilineTextAlignment(テキスト配置の種類(TextAlignment))

##### TextAlignmentの使い方

| 名前        | 説明   |
| --------- | ---- |
| .center   | 中央寄せ |
| .leading  | 左寄せ  |
| .trailing | 右寄せ  |

##### 例

    Button("テキストテキストテキスト")
        .multilineTextAlignment(.center)

#### keyboardType

##### 意味

キーボードタイプを設定

##### 使い方

    .keyboardType(キーボードタイプ(UIKeyboardType))

##### UIKeyboardTypeの使い方

| 名前                     | 説明                     |
| ---------------------- | ---------------------- |
| .default               | デフォルト                  |
| .asciiCapable          | ASCII                  |
| .numbersAndPunctuation | 数字と句読点                 |
| .URL                   | URL                    |
| .numberPad             | PIN入力用のテンキー            |
| .phonePad              | 電話番号                   |
| .namePhonePad          | 人の名前や電話番号を入力するためのキーパッド |
| .emailAddress          | メールアドレス                |
| .decimalPad            | 数字と小数点                 |
| .twitter               | Twitterのテキスト入力用        |
| .webSearch             | Web検索用語やURL入力用         |
| .asciiCapableNumberPad | ASCIIの数字のみを出力するナンバーパッド |

##### 例

    Button("電話番号")
        .keyboardType(.phonePad)

#### disableAutocorrection

##### 意味

自動修正を無効にするかどうかを設定

##### 使い方

    .disableAutocorrection(自動修正が無効になっているか(Bool))

    .disableAutocorrection()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .disableAutocorrection(true)

#### autocapitalization

##### 意味

自動大文字を適用するかどうかを設定

##### 使い方

    .autocapitalization(自動大文字設定(UITextAutocapitalizationType))

##### UITextAutocapitalizationTypeの使い方

| 名前             | 説明                |
| -------------- | ----------------- |
| .none          | 自動大文字化を行わない       |
| .words         | 各単語の最初の文字を自動的に大文字 |
| .sentences     | 各文の最初の文字を自動的に大文字  |
| .allCharacters | すべての文字を自動的に大文字    |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .autocapitalization(UITextAutocapitalizationType.words)

#### textContentType

##### 意味

テキストコンテンツタイプを設定
ユーザーがiOSまたはtvOSデバイスでテキストを入力しているときにシステムが提案を提供するために使用

##### 使い方

    .textContentType(テキストコンテンツタイプ(UITextContentType))

    .textContentType()

##### UITextContentTypeの使い方

| 名前                   | 説明                                   |
| -------------------- | ------------------------------------ |
| .URL                 | テキスト入力エリアがURLを指定していることを期待            |
| .addressCity         | テキスト入力エリアが都市名を指定していることを期待            |
| .addressCityAndState | テキスト入力エリアが都市名を州名を指定していることを期待         |
| .addressState        | テキスト入力エリアが状態を指定していることを期待             |
| .countryName         | テキスト入力エリアが国名や地域名を指定していることを期待         |
| .creditCardNumber    | テキスト入力エリアがクレジットカード番号を指定していることを期待     |
| .emailAddress        | テキスト入力エリアがメールアドレスを指定していることを期待        |
| .familyName          | テキスト入力エリアが姓名を指定していることを期待             |
| .fullStreetAddress   | テキスト入力エリアが番地を指定していることを期待             |
| .givenName           | テキスト入力エリアが名字を指定していることを期待             |
| .jobTitle            | テキスト入力エリアが職種を指定していることを期待             |
| .location            | テキスト入力エリアがマンション名などの特定の場所を指定していることを期待 |
| .middleName          | テキスト入力エリアが名前を指定していることを期待             |
| .name                | テキスト入力エリアが名前を指定していることを期待             |
| .namePrefix          | テキスト入力エリアがDr.などの接頭語やタイトルを指定していることを期待 |
| .nameSuffix          | テキスト入力エリアがJr.などの接尾語を指定していることを期待      |
| .nickname            | テキスト入力エリアがニックネームを指定していることを期待         |
| .organizationName    | テキスト入力エリアが組織名を指定していることを期待            |
| .postalCode          | テキスト入力エリアが郵便番号を指定していることを期待           |
| .streetAddressLine1  | テキスト入力エリアが住所の1行目を指定していることを期待         |
| .streetAddressLine2  | テキスト入力エリアが住所の2行目を指定していることを期待         |
| .sublocality         | テキスト入力エリアが住所を指定していることを期待             |
| .telephoneNumber     | テキスト入力エリアが電話番号を指定していることを期待           |
| .username            | テキスト入力エリアがアカウントやログイン名を指定していることを期待    |
| .password            | テキスト入力エリアがパスワードを指定していることを期待          |
| .newPassword         | テキスト入力エリアが新しいパスワードを指定していることを期待       |
| .oneTimeCode         | テキスト入力エリアがワンタイムコードを指定していることを期待       |

##### 例

    Button("ユーザ名")
        .textContentType(.username)

#### labelsHidden

##### 意味

ラベルを非表示

##### 使い方

    .labelsHidden()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .labelsHidden()

#### defaultWheelPickerItemHeight

##### 意味

デフォルトのホイールスタイルのピッカーアイテムの高さを設定

##### 使い方

    .defaultWheelPickerItemHeight(高さ(CGFloat))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .defaultWheelPickerItemHeight(30)

#### horizontalRadioGroupLayout

##### 意味

ラジオグループスタイルピッカーのスタイルがレイアウト内のラジオボタンで水平方向に配置されるように設定

##### 使い方

    .horizontalRadioGroupLayout()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .horizontalRadioGroupLayout()

#### controlSize

##### 意味

コントロールのサイズを設定

##### 使い方

    .controlSize(コントロールサイズ(ControlSize))

##### ControlSizeの使い方

| 名前       | 説明     |
| -------- | ------ |
| .large   | 大きい    |
| .mini    | 最小     |
| .regular | デフォルト　 |
| .small   | 小さい    |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .controlSize(.small)

#### listRowInsets

##### 意味

リストの行にインセットを適用

##### 使い方

    .listRowInsets(パディング領域(EdgeInsets))

    .listRowInsets()

##### EdgeInsetsの使い方

| 名前                                                                             | 説明                                      |
| ------------------------------------------------------------------------------ | --------------------------------------- |
| EdgeInsets()                                                                   | エッジインセットを作成                                        |
| EdgeInsets(NSDirectionalEdgeInsets)                                            | 同等のNSDirectionalEdgeInsetsからエッジインセットを作成 |
| EdgeInsets(top: CGFloat, leading: CGFloat, bottom: CGFloat, trailing: CGFloat) | エッジインセットを作成                                        |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .listRowInsets(EdgeInsets(top: 16, leading: 0, bottom: 16, trailing: 0))

#### listRowBackground

##### 意味

カスタムの背景ビューをリストの行アイテムの背後に配置

##### 使い方

    .listRowBackground(背景ビュー(View))

    .listRowBackground()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .listRowBackground(Color.blue)

#### listItemTint

##### 意味

Tint効果を設定

##### 使い方

    .listItemTint(Tint効果(ListItemTint)か色(Color))

    .listItemTint()

##### ListItemTintとColorの使い方

| 名前           | 説明                  |
| ------------ | ------------------- |
| .fixed       | 明示的なカラー             |
| .preferred   | オーバーライド可能な明示的なカラー   |
| .primary     | メインカラー              |
| .secondary   | サブカラー               |
| .accentColor | システムまたはアプリのアクセントカラー |
| .black       | 黒色                  |
| .blue        | 青色                  |
| .brown       | 茶色                  |
| .clear       | 透明色                 |
| .cyan        | シアン色                |
| .gray        | 灰色                  |
| .green       | 緑色                  |
| .indigo      | インディゴ色              |
| .mint        | ミント色                |
| .orange      | オレンジ色               |
| .pink        | ピンク色                |
| .purple      | 紫色                  |
| .red         | 赤色                  |
| .teal        | ティール色               |
| .white       | 白色                  |
| .yellow      | 黄色                  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .listItemTint(.yellow)

#### navigationTitle

##### 意味

ローカライズされた文字列キーを使用してナビゲーションのタイトルを設定

##### 使い方

    .navigationTitle("タイトル名(StringProtocol")

    .navigationTitle(ローカライズされた文字列キー(LocalizedStringKey))

    .navigationTitle(タイトル(Text))

    .navigationTitle(タイトル(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .navigationTitle("Title")

#### navigationSubtitle

##### 意味

ナビゲーションのサブタイトルを設定

##### 使い方

    .navigationSubtitle("サブタイトル名(StringProtocol)")

    .navigationSubtitle(ローカライズされた文字列キー(LocalizedStringKey))

    .navigationSubtitle(サブタイトル(Text))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .navigationSubtitle("subtitle")

#### navigationBarHidden

##### 意味

ナビゲーションバーを非表示

##### 使い方

    .navigationBarHidden(非表示にするか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .navigationBarHidden(true)

#### navigationBarBackButtonHidden

##### 意味

ビューのナビゲーションバーの戻るボタンを非表示

##### 使い方

    .navigationBarBackButtonHidden(非表示にするか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .navigationBarBackButtonHidden(true)

#### navigationBarTitleDisplayMode

##### 意味

タイトル表示モードを設定

##### 使い方

    .navigationBarTitleDisplayMode(タイトルの表示に使用するスタイル(NavigationBarItem.TitleDisplayMode))

##### NavigationBarItem.TitleDisplayModeの使い方

| 名前         | 説明             |
| ---------- | -------------- |
| .automatic | 継承             |
| .inline    | 標準的な範囲内でタトルを表示 |
| .large     | 大きなタイトルを表示     |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .navigationBarTitleDisplayMode(.inline)

#### toolbar

##### 意味

ツールバーやナビゲーションバーに入力されたビューを表示

##### 使い方

    .toolbar() {
        コンテンツ(View)
    }

    .toolbar(content: コンテンツ(View))

    .toolbar() {
        コンテンツ(ToolbarContent)
    }

    .toolbar(content: コンテンツ(ToolbarContent))

    .toolbar(id: "ユニークな識別子") {
        コンテンツ(CustomizableToolbarContent)
    }

    .toolbar(id: "ユニークな識別子", content: コンテンツ(CustomizableToolbarContent))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .toolbar {
            // コンテンツ
        }

#### tabItem

##### 意味

タブバーに表示するビューを指定

##### 使い方

    .tabItem() {
        タブバーに表示するビュー(View)
    }

    .tabItem(タブバーに表示するビュー(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .tabItem {
            Label("Menu", systemImage: "list.dash")
        }

#### help

##### 意味

ヘルプテキストを追加

##### 使い方

    .help("ヘルプテキスト(StringProtocol)")

    .help(ローカライズされた文字列キー(LocalizedStringKey))

    .help(Tヘルプテキスト(Text))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .help("ヘルプテキスト")

#### contextMenu

##### 意味

コンテキストメニューをビューに追加

##### 使い方

    .contextMenu() {
        メニュー項目(View)
    }

    .contextMenu(menuItems: メニュー項目(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .contextMenu {
            // 項目
        }

#### statusBar

##### 意味

ステータスバーの可視性を設定

##### 使い方

    .statusBar(hidden: 非表示にするか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .statusBar(true)

#### touchBar

##### 意味

タッチバーが表示するコンテンツを設定

##### 使い方

    .touchBar() {
        ビューのコレクション(View)
    }

    .touchBar(content: ビューのコレクション(View))

    .touchBar() {
        ビューのコレクション(TouchBar<View>)
    }

    .touchBar(content: ビューのコレクション(TouchBar<View>))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .touchBar {
            // 項目
        }

#### touchBarItemPrincipal

##### 意味

このタッチバーに特別な意味を持つ主要なビューを設定

##### 使い方

    .touchBarItemPrincipal(目立つように表示するか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .touchBarItemPrincipal(false)

#### touchBarCustomizationLabel

##### 意味

ビューの機能を識別するユーザーに表示される文字列を設定

##### 使い方

    .touchBarCustomizationLabel(ラベル(Text))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .touchBarCustomizationLabel(Text("ボタン"))

#### touchBarItemPresence

##### 意味

ユーザーがカスタマイズしたビューの動作を設定

##### 使い方

    .touchBarItemPresence(カスタマイズ(TouchBarItemPresence))

##### TouchBarItemPresenceの使い方

| 名前        | 説明                       |
| --------- | ------------------------ |
| .default  | デフォルト                    |
| .optional | デフォルトでは非表示でカスタマイズパレットに表示 |
| .required | デフォルトでは表示でカスタマイズ中に削除できない |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .touchBarItemPresence(.required("heartsKey"))

#### buttonStyle

##### 意味

ボタンのスタイルをカスタムの外観とカスタムの相互作用動作を持つボタンスタイルに設定

##### 使い方

    .buttonStyle(スタイル(ButtonStyle))

    .buttonStyle(スタイル(PrimitiveButtonStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .buttonStyle(PlainButtonStyle())

#### menuStyle

##### 意味

メニューのスタイルを設定

##### 使い方

    .menuStyle(スタイル(MenuStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .menuStyle(DefaultMenuStyle())

#### pickerStyle

##### 意味

ピッカーのスタイルを設定

##### 使い方

    .pickerStyle(スタイル(PickerStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .pickerStyle(DefaultPickerStyle())

#### datePickerStyle

##### 意味

日付ピッカーのスタイルを設定

##### 使い方

    .datePickerStyle(スタイル(DatePickerStyle))

##### datePickerStyleの使い方

| 名前           | 説明                             |
| ------------ | ------------------------------ |
| .automatic    | デフォルトスタイル                      |
| .compact      | コンパクトなテキスト形式で表示                |
| .field        | 編集可能なフィールドに表示                  |
| .graphical    | インタラクティブなカレンダーや時計を表示           |
| .stepperField | 編集可能なフィールドに表示し選択肢を増減できるステッパーあり |
| .wheel        | スクロール可能なホイールに各コンポーネントを列として表示　  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .datePickerStyle(DefaultDatePickerStyle())

#### textFieldStyle

##### 意味

テキストフィールドのスタイルを設定

##### 使い方

    .textFieldStyle(スタイル(TextFieldStyle))

##### TextFieldStyleの使い方

| 名前                          | 説明          |
| --------------------------- | ----------- |
| PlainTextFieldStyle         | 装飾なし        |
| RoundedBorderTextFieldStyle | 丸い境界線で囲われる  |
| SquareBorderTextFieldStyle  | 四角い境界線で囲われる |
| DefaultTextFieldStyle       | デフォルト       |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .textFieldStyle(DefaultTextFieldStyle())

#### toggleStyle

##### 意味

トグルのスタイルを設定

##### 使い方

    .toggleStyle(スタイル(ToggleStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .toggleStyle(DefaultToggleStyle())

#### listStyle

##### 意味

リストのスタイルを設定

##### 使い方

    .listStyle(スタイル(ListStyle))

##### ListStyleの使い方

| 名前                                        | 説明               |
| ----------------------------------------- | ---------------- |
| .automatic                                | デフォルト            |
| .bordered                                 | 標準のボーダーを持つリスト    |
| .bordered(alternatesRowBackgrounds: Bool) | 標準のボーダーを持つリスト    |
| .carousel                                 | カルーセルリスト         |
| .elliptical                               | 楕円形のリスト          |
| .grouped                                  | グループ化されたリスト      |
| .inset                                    | インセットリスト         |
| .insetGrouped                             | インセットグループ化されたリスト |
| .plain                                    | プレーンなリスト         |
| .sidebar                                  | サイドバーリスト         |

##### 例

    List {Text("Hello world")}
        .listStyle(.carousel)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .listStyle(.carousel)

#### navigationViewStyle

##### 意味

ナビゲーションビューのスタイルを設定

##### 使い方

    .navigationViewStyle(スタイル(NavigationViewStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .navigationViewStyle(DefaultNavigationViewStyle())

#### tabViewStyle

##### 意味

タブのスタイル設定

##### 使い方

    .tabViewStyle(スタイル(TabViewStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .tabViewStyle(DefaultTabViewStyle())

#### labelStyle

##### 意味

ラベルのスタイル

##### 使い方

    .labelStyle(スタイル(LabelStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .labelStyle(DefaultLabelStyle())

#### progressViewStyle

##### 意味

プログレスビューのスタイルを設定

##### 使い方

    .progressViewStyle(スタイル(ProgressViewStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .progressViewStyle(DefaultProgressViewStyle())

#### indexViewStyle

##### 意味

インデックスビューのスタイルを設定

##### 使い方

    .indexViewStyle(スタイル(IndexViewStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .indexViewStyle(PageIndexViewStyle())

#### groupBoxStyle

##### 意味

グループボックスのスタイルを設定

##### 使い方

    .groupBoxStyle(スタイル(GroupBoxStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .groupBoxStyle(DefaultGroupBoxStyle())

#### gaugeStyle

##### 意味

ゲージのスタイルを設定

##### 使い方

    .gaugeStyle(スタイル(GaugeStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .gaugeStyle(DefaultGaugeStyle())

#### presentedWindowStyle

##### 意味

インタラクションで作成されるウィンドウのスタイルを設定

##### 使い方

    .presentedWindowStyle(スタイル(WindowStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())

#### presentedWindowToolbarStyle

##### 意味

インタラクションで作成されるウィンドウのツールバーのスタイルを設定

##### 使い方

    .presentedWindowToolbarStyle(スタイル(WindowToolbarStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .presentedWindowToolbarStyle(DefaultWindowToolbarStyle())

#### frame

##### 意味

フレームのサイズと配置位置を指定

##### 使い方

    .frame(width: 幅(CGFloat) = nil, height: 高さ(CGFloat) = nil, alignment: 配置の種類(Alignment) = .center)

    .frame(minWidth: 最小幅(CGFloat) = nil, idealWidth: 最適な幅(CGFloat) = nil, maxWidth: 最大幅(CGFloat) = nil, minHeight: 最小の高さ(CGFloat) = nil, idealHeight: 最適な高さ(CGFloat) = nil, maxHeight: 最大の高さ(CGFloat) = nil, alignment: 配置(Alignment) = nil)

    .frame()

##### Alignmentの使い方

| 名前              | 説明   |
| --------------- | ---- |
| .bottom         | 下寄せ  |
| .bottomLeading  | 左下寄せ |
| .bottomTrailing | 右下寄せ |
| .center         | 中央寄せ |
| .leading        | 左寄せ  |
| .top            | 上寄せ  |
| .topLeading     | 左上寄せ |
| .topTrailing    | 右寄せ上 |
| .trailing       | 右寄せ  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .frame(width: 200, height: 100)

#### fixedSize

##### 意味

最適なサイズに修正

##### 使い方

    .fixedSize()

    .fixedSize(horizontal: 横のはみ出しを許すか(Bool), vertical: 縦のはみ出しを許すか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .fixedSize()
        .frame(width: 200, height: 200)

#### layoutPriority

##### 意味

親レイアウトがこの子にスペースを配分する優先順位を設定 

##### 使い方

    .layoutPriority(優先度(Double))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .layoutPriority(1)

#### position

##### 意味

中心を親の座標空間の指定された点に配置

##### 使い方

    .position(中心の位置(CGPoint))

    .position(x: 中心を配置するx座標(CGFloat), y: 中心を配置するy座標(CGFloat))

##### CGPointの使い方

| 名前                              | 説明                       |
| ------------------------------- | ------------------------ |
| CGPoint()                       | 位置(0,0)の点を作成             |
| CGPoint(x: Double, y: Double)   | 浮動小数点値で指定された座標を持つ点を作成    |
| CGPoint(x: Int, y: Int)         | 整数値で指定された座標を持つ点を作成       |
| CGPoint(x: CGFloat, y: CGFloat) | CGFloatの値で指定された座標を持つ点を作成 |
| CGPoint.zero                    | 位置(0,0)の点                |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .position(CGPoint(x: 175, y: 100))

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .position(x: 175, y: 100)

#### offset

##### 意味

元の位置から表示位置を移動

##### 使い方

    .offset(オフセット(CGSize))

    .offset(x: 水平距離(CGFloat), y: 垂直距離(CGFloat))

##### CGSizeの使い方

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .offset(CGSize(width: 20, height: 25))

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .offset(x: 20, y: 50)

#### coordinateSpace

##### 意味

ビューの座標空間に名前を割り当て

##### 使い方

    .coordinateSpace(name: 識別する名前(Hashable))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .coordinateSpace(name: "stack")

#### alignmentGuide

##### 意味

ビューの水平方向、または垂直方向の配置を設定

##### 使い方

    .alignmentGuide(配置方法(HorizontalAlignment)) { 配置ガイド(ViewDimensions) in
        クロージャー(CGFloat)
    }

    .alignmentGuide(配置方法(HorizontalAlignment), computeValue: クロージャー)

    .alignmentGuide(配置方法(VerticalAlignment) { 配置ガイド(ViewDimensions) in
        クロージャー(CGFloat)
    }

    .alignmentGuide(配置方法(VerticalAlignment), computeValue: クロージャー)

##### 配置方法(HorizontalAlignment)

| 名前        | 説明  |
| --------- | --- |
| .center   | 中央 |
| .leading  | 左   |
| .trailing | 右   |

##### 配置方法(VerticalAlignment)

| 名前                 | 説明  |
| ------------------ | --- |
| .bottom            | 下   |
| .center            | 中   |
| .firstTextBaseline | 先頭の行のベースライン |
| .lastTextBaseline  | 最終の行のベースライン |
| .top               | 上   |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .alignmentGuide(.leading) { _ in  50 }

#### padding

##### 意味

指定された値で周囲に余白を追加

##### 使い方

    .padding(パディング値(CGFloat))

    .padding(パディング領域(EdgeInsets))

    .padding(位置の種類(Edge.Set) = .all, パディング値(CGFloat) = nil)

###### EdgeInsetsの使い方

| 名前                                                                             | 説明                                      |
| ------------------------------------------------------------------------------ | --------------------------------------- |
| EdgeInsets()                                                                   | エッジインセットを作成                                        |
| EdgeInsets(NSDirectionalEdgeInsets)                                            | 同等のNSDirectionalEdgeInsetsからエッジインセットを作成 |
| EdgeInsets(top: CGFloat, leading: CGFloat, bottom: CGFloat, trailing: CGFloat) | エッジインセットを作成                                        |

##### Edge.Setの使い方

| 名前          | 説明  |
| ----------- | --- |
| .all        | すべて |
| .bottom     | 下   |
| .horizontal | 水平  |
| .leading    | 左   |
| .top        | 上   |
| .trailing   | 右   |
| .vertical   | 垂直  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .padding(10.0)

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .padding(EdgeInsets(top: 0, leading: 20, bottom: 20, trailing: 0))

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .padding(.bottom)

#### ignoresSafeArea

##### 意味

##### 使い方

    .ignoresSafeArea(無視されるエリア(SafeAreaRegions) = .all, edges: 位置(Edge.Set) = .all)

##### SafeAreaRegionsの使い方

| 名前         | 説明                                   |
| ---------- | ------------------------------------ |
| .all       | すべて                                  |
| .container | ユーザーインターフェース内のデバイスやコンテナによって定義される安全領域 |
| .keyboard  | ソフトウェアキーボードの現在の範囲と一致するセーフエリア         |

##### Edge.Setの使い方

| 名前          | 説明  |
| ----------- | --- |
| .all        | すべて |
| .bottom     | 下   |
| .horizontal | 水平  |
| .leading    | 左   |
| .top        | 上   |
| .trailing   | 右   |
| .vertical   | 垂直  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .ignoresSafeArea(edges: .bottom)

#### overlay

##### 意味

前に別のビューを重ねて配置

##### 使い方

    .overlay(alignment: 重ねるビューの配置位置(Alignment) = .center) {
        配置するビュー(View)
    }

    .overlay(配置するビュー(View), alignment: 重ねるビューの配置位置(Alignment) = .center)

##### Alignmentの使い方

| 名前              | 説明   |
| --------------- | ---- |
| .bottom         | 下寄せ  |
| .bottomLeading  | 左下寄せ |
| .bottomTrailing | 右下寄せ |
| .center         | 中央寄せ |
| .leading        | 左寄せ  |
| .top            | 上寄せ  |
| .topLeading     | 左上寄せ |
| .topTrailing    | 右寄せ上 |
| .trailing       | 右寄せ  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .overlay(
            Text("hoge")
        )

#### background

##### 意味

指定されたビューに背後を設定

##### 使い方

    .background(alignment: 配置の種類(Alignment) = .center) {
        コンテンツ(View)
    }

    .background(コンテンツ(View), alignment: 配置の種類(Alignment) = .center)        

##### Alignmentの使い方

| 名前              | 説明   |
| --------------- | ---- |
| .bottom         | 下寄せ  |
| .bottomLeading  | 左下寄せ |
| .bottomTrailing | 右下寄せ |
| .center         | 中央寄せ |
| .leading        | 左寄せ  |
| .top            | 上寄せ  |
| .topLeading     | 左上寄せ |
| .topTrailing    | 右寄せ上 |
| .trailing       | 右寄せ  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .background(
            Text("hoge")
        )

#### zIndex

##### 意味

重なり合うビューの表示順序を制御

##### 使い方

    .zIndex(順序(Double))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .zIndex(1)

#### border

##### 意味

指定されたスタイルと幅で境界線を追加

##### 使い方

    .border(スタイル(ShapeStyle), width: 太さ(CGFloat))

##### ShapeStyleの使い方

| 名前                                                                                                                 | 説明                         |
| ------------------------------------------------------------------------------------------------------------------ | -------------------------- |
| Color.primary                                                                                                      | メインカラー                     |
| Color.secondary                                                                                                    | サブカラー                      |
| Color.accentColor                                                                                                  | システムまたはアプリのアクセントカラー        |
| Color.black                                                                                                        | 黒色                         |
| Color.blue                                                                                                         | 青色                         |
| Color.brown                                                                                                        | 茶色                         |
| Color.clear                                                                                                        | 透明色                        |
| Color.cyan                                                                                                         | シアン色                       |
| Color.gray                                                                                                         | 灰色                         |
| Color.green                                                                                                        | 緑色                         |
| Color.indigo                                                                                                       | インディゴ色                     |
| Color.mint                                                                                                         | ミント色                       |
| Color.orange                                                                                                       | オレンジ色                      |
| Color.pink                                                                                                         | ピンク色                       |
| Color.purple                                                                                                       | 紫色                         |
| Color.red                                                                                                          | 赤色                         |
| Color.teal                                                                                                         | ティール色                      |
| Color.white                                                                                                        | 白色                         |
| Color.yellow                                                                                                       | 黄色                         |
| Color(String, bundle: Bundle? = nil)                                                                               | 色のカスタマイズ                   |
| Color(hue: Double, saturation: Double, brightness: Double, opacity: Double = 1)                                    | 色のカスタマイズ                   |
| Color(Color.RGBColorSpace = .sRGB, white: Double, opacity: Double = 1)                                             | 色のカスタマイズ                   |
| Color(Color.RGBColorSpace = .sRGB, red: Double, green: Double, blue: Double, opacity: Double = 1)                  | 色のカスタマイズ                   |
| Color(uiColor: UIColor)                                                                                            | 色のカスタマイズ                   |
| Color(nsColor: NSColor)                                                                                            | 色のカスタマイズ                   |
| Color(cgColor: CGColor)                                                                                            | 色のカスタマイズ                   |
| Gradient(colors: [Color])                                                                                          | カラーグラデーション                 |
| Gradient(stops: [Gradient.Stop])                                                                                   | カラーグラデーション                 |
| AngularGradient.angularGradient(Gradient, center: UnitPoint, startAngle: Angle, endAngle: Angle)                   | 円形グラデーション                  |
| AngularGradient.angularGradient(colors: [Color], center: UnitPoint, startAngle: Angle, endAngle: Angle)            | 円形グラデーション                  |
| AngularGradient.angularGradient(stops: [Gradient.Stop], center: UnitPoint, startAngle: Angle, endAngle: Angle)     | 円形グラデーション                  |
| AngularGradient.conicGradient(Gradient, center: UnitPoint, angle: Angle = .zero)                                   | 円形グラデーション                  |
| AngularGradient.conicGradient(colors: [Color], center: UnitPoint, angle: Angle = .zero)                            | 円形グラデーション                  |
| AngularGradient.conicGradient(stops: [Gradient.Stop], center: UnitPoint, angle: Angle = .zero)                     | 円形グラデーション                  |
| LinearGradient.linearGradient(Gradient, startPoint: UnitPoint, endPoint: UnitPoint)                                | 直線的なグラデーション                |
| LinearGradient.linearGradient(colors: [Color], startPoint: UnitPoint, endPoint: UnitPoint)                         | 直線的なグラデーション                |
| LinearGradient.linearGradient(stops: [Gradient.Stop], startPoint: UnitPoint, endPoint: UnitPoint)                  | 直線的なグラデーション                |
| RadialGradient.radialGradient(Gradient, center: UnitPoint, startRadius: CGFloat, endRadius: CGFloat)               | 放射状グラデーション                 |
| RadialGradient.radialGradient(colors: [Color], center: UnitPoint, startRadius: CGFloat, endRadius: CGFloat)        | 放射状グラデーション                 |
| RadialGradient.radialGradient(stops: [Gradient.Stop], center: UnitPoint, startRadius: CGFloat, endRadius: CGFloat) | 放射状グラデーション                 |
| ImagePaint(image: Image, sourceRect: CGRect = CGRect(x: 0, y: 0, width: 1, height: 1), scale: CGFloat = 1)         | 画像の一部分を繰り返して形状を埋めるシェイプスタイル |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .border(Color.purple, width: 4)

#### accentColor

##### 意味

含まれるビューのアクセントカラーを設定

##### 使い方

    .accentColor(色(Color))

    .accentColor()

##### Colorの使い方

| 名前                                                                                                | 説明                  |
| ------------------------------------------------------------------------------------------------- | ------------------- |
| Color.primary                                                                                     | メインカラー              |
| Color.secondary                                                                                   | サブカラー               |
| Color.accentColor                                                                                 | システムまたはアプリのアクセントカラー |
| Color.black                                                                                       | 黒色                  |
| Color.blue                                                                                        | 青色                  |
| Color.brown                                                                                       | 茶色                  |
| Color.clear                                                                                       | 透明色                 |
| Color.cyan                                                                                        | シアン色                |
| Color.gray                                                                                        | 灰色                  |
| Color.green                                                                                       | 緑色                  |
| Color.indigo                                                                                      | インディゴ色              |
| Color.mint                                                                                        | ミント色                |
| Color.orange                                                                                      | オレンジ色               |
| Color.pink                                                                                        | ピンク色                |
| Color.purple                                                                                      | 紫色                  |
| Color.red                                                                                         | 赤色                  |
| Color.teal                                                                                        | ティール色               |
| Color.white                                                                                       | 白色                  |
| Color.yellow                                                                                      | 黄色                  |
| Color(Color.RGBColorSpace = .sRGB, red: Double, green: Double, blue: Double, opacity: Double = 1) | 個別作成                |
| Color(Color.RGBColorSpace = .sRGB, white: Double, opacity: Double = 1)                            | 個別作成                |
| Color(hue: Double, saturation: Double, brightness: Double, opacity: Double = 1)                   | 個別作成                |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .accentColor(.purple)

#### preferredColorScheme

##### 意味

このプレゼンテーションの優先カラースキームを設定

##### 使い方

    .preferredColorScheme(カラースキーム(ColorScheme))

    .preferredColorScheme()

##### ColorSchemeの使い方

| 名前     | 説明  |
| ------ | --- |
| .dark  | ダーク |
| .light | ライト |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .preferredColorScheme(.dark)

#### redacted

##### 意味

リダクションを適用する理由を追加

##### 使い方

    .redacted(reason: リダクションを適用する理由(RedactionReasons))

##### RedactionReasonsの使い方

| 名前                                              | 説明                       |
| ----------------------------------------------- | ------------------------ |
| RedactionReasons()                              | 空のオプションセットを作成            |
| RedactionReasons(Sequence)                      | アイテムの有限のシーケンスから新しいセットを作成 |
| RedactionReasons(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成  |
| RedactionReasons(rawValue: Int)                 | 生の値から新しいセットを作成           |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .redacted(reason: RedactionReasons())

#### unredacted

##### 意味

リダクションを適用する理由をすべて削除

##### 使い方

    .unredacted()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .unredacted()

#### mask

##### 意味

指定されたビューのアルファチャネルを使用してマスク

##### 使い方

    .mask(マスク(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .mask(TransformedShape(shape: Circle(), transform: CGAffineTransform()).opacity(0.1))

#### clipped

##### 意味

長方形のフレームに切り取る

##### 使い方

    .clipped(antialiased: スムージングを適用するか(Bool) = false)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .clipped(antialiased: true)

#### clipShape

##### 意味

クリッピング形状を設定

##### 使い方

    .clipShape(クリッピング形状(Shape), style: 塗りつぶしスタイル(FillStyle))

##### Shapeの作成方法

| 名前                                                                                      | 説明                             |
| --------------------------------------------------------------------------------------- | ------------------------------ |
| Capsule(style: RoundedCornerStyle = .circular)                                          | カプセル形状はそれを含むビューのフレーム内に整列       |
| Circle()                                                                                | ビューのフレームを中心とした円                |
| ContainerRelativeShape()                                                                | 現在のコンテナ形状のインセットバージョンで置き換えられる形状 |
| Ellipse()                                                                               | 楕円はそれを含むビューのフレーム内に整列           |
| OffsetShape(shape: Content, offset: CGSize)                                             | 並進オフセット変換が適用された形状              |
| Path()                                                                                  | 任意のパスにあわせて描画                   |
| Path((inout Path))                                                                      | 任意のパスにあわせて描画                   |
| Path(CGMutablePath)                                                                     | 任意のパスにあわせて描画                   |
| Path(CGPath)                                                                            | 任意のパスにあわせて描画                   |
| Path(String)                                                                            | 任意のパスにあわせて描画                   |
| Path(CGRect)                                                                            | 任意のパスにあわせて描画                   |
| Path(ellipseIn rect: CGRect)                                                            | 任意のパスにあわせて描画                   |
| Path(roundedRect: CGRect, cornerRadius: CGFloat, style: RoundedCornerStyle = .circular) | 任意のパスにあわせて描画                   |
| Path(roundedRect: CGRect, cornerSize: CGSize, style: RoundedCornerStyle = .circular)    | 任意のパスにあわせて描画                   |
| TransformedShape(shape: Circle(), transform: CGAffineTransform())                       | 矩形の形状はそれを含むビューのフレーム内に配置        |
| RotatedShape(shape: Content, angle: Angle, anchor: UnitPoint = .center)                 | 回転トランスフォームが適用された図形             |
| RoundedRectangle(cornerRadius: CGFloat, style: RoundedCornerStyle = .circular)          | 角の丸い長方形でそれを含むビューのフレーム内に配置      |
| RoundedRectangle(cornerSize: CGSize, style: RoundedCornerStyle = .circular)             | 角の丸い長方形でそれを含むビューのフレーム内に配置      |
| ScaledShape(shape: Content, scale: CGSize, anchor: UnitPoint = .center)                 | スケールトランスフォームが適用された形状           |
| TransformedShape(shape: Content, transform: CGAffineTransform)                          | アフィン変換が適用された形状                 |

##### FillStyleの作成方法

| 名前                                                        | 説明                     |
| --------------------------------------------------------- | ---------------------- |
| FillStyle(eoFill: Bool = false, antialiased: Bool = true) | ベクトル形状をラスタライズするためのスタイル |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .clipShape(Circle())

#### cornerRadius

##### 意味

指定されたコーナー半径で境界フレームを切り取る

##### 使い方

    .cornerRadius(半径(CGFloat), antialiased: スムージングを適用するか(Bool) = true)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .cornerRadius(25)

#### scaledToFill

##### 意味

スケーリングしてその親を塗りつぶします

##### 使い方

    .scaledToFill()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .scaledToFill()

#### scaledToFit

##### 意味

スケーリングして親に合わせます

##### 使い方

    .scaledToFit()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .scaledToFit()

#### scaleEffect

##### 意味

水平方向と垂直方向の両方に指定された値でスケーリング

##### 使い方

    .scaleEffect(値(CGFloat), anchor: 開始位置(UnitPoint) = .center)

    .scaleEffect(値(CGSize), anchor: 開始位置(UnitPoint) = .center)

    .scaleEffect(x: 水平方向の値(CGFloat) = 1.0, y: 垂直方向の値(CGFloat) = 1.0, anchor: 開始位置(UnitPoint) = .center)

##### CGSizeの使い方

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

##### UnitPointの使い方

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

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .scaleEffect(2, anchor: .leading)

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .scaleEffect(CGSize(width: 0.9, height: 1.3), anchor: .leading)

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .scaleEffect(x: 0.5, y: 0.5, anchor: .bottomTrailing)

#### imageScale

##### 意味

画像スケールを設定

##### 使い方

    .imageScale(相対サイズ(Image.Scale))

##### Image.Scaleの使い方

| 名前      | 説明    |
| ------- | ----- |
| .small  | スモール  |
| .medium | ミディアム |
| .large  | ラージ   |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .imageScale(.large)

#### aspectRatio

##### 意味

寸法を指定したアスペクト比に制限

##### 使い方

    .aspectRatio(比率(CGFloat) = nil, contentMode: 親コンテキストに適合するか(ContentMode))

    .aspectRatio(サイズ(CGSize), contentMode: 親コンテキストに収まるか(ContentMode))

##### CGSizeの使い方

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

##### ContentModeの使い方

| 名前    | 説明                  |
| ----- | ------------------- |
| .fill | 枠内いっぱいに表示されるように拡大縮小 |
| .fit  | 枠内からハミ出さないように拡大縮小   |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .aspectRatio(0.75, contentMode: .fit)

#### rotationEffect

##### 意味

指定された点を中心に回転

##### 使い方

    .rotationEffect(角度(Angle), anchor: 位置(UnitPoint) = .center)

##### Angleの使い方

| 名前               | 説明      |
| ---------------- | ------- |
| .degrees(Double) | 度を指定    |
| .radians(Double) | ラジアンを指定 |

##### UnitPointの使い方

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

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .rotationEffect(.degrees(22))

#### rotation3DEffect

##### 意味

レンダリングされた出力を指定された回転軸を中心に3次元で回転

##### 使い方

    .rotation3DEffect(角度(Angle), axis: (x: x軸要素(CGFloat), y: y軸要素(CGFloat), z: z軸要素(CGFloat)), anchor: 位置(UnitPoint) = .center, anchorZ: 回転の固定位置(CGFloat) = 0, perspective: 相対消失点(CGFloat) = 1)

##### Angleの使い方

| 名前               | 説明      |
| ---------------- | ------- |
| .degrees(Double) | 度を指定    |
| .radians(Double) | ラジアンを指定 |

##### UnitPointの使い方

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

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .rotation3DEffect(.degrees(45), axis: (x: 0.0, y: 1.0, z: 0.0))

#### projectionEffect

##### 意味

レンダリングされた出力に投影変換を適用

##### 使い方

    .projectionEffect(変換条件(ProjectionTransform))

##### ProjectionTransformの使い方

| 名前                                     | 説明                   |
| -------------------------------------- | -------------------- |
| ProjectionTransform()                  | 引数なし                 |
| ProjectionTransform(CGAffineTransform) | CGAffineTransformを指定 |
| ProjectionTransform(CATransform3D)     | 　CATransform3Dを指定    |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .projectionEffect(ProjectionTransform())

#### transformEffect

##### 意味

レンダリングされた出力にアフィン変換を適用

##### 使い方

    .transformEffect(アフィン変換行列(CGAffineTransform))

##### CGAffineTransformの使い方

| 名前                                                                                          | 説明                         |
| ------------------------------------------------------------------------------------------- | -------------------------- |
| CGAffineTransform(rotationAngle: CGFloat)                                                   | 指定された回転値から構築されたアフィン変換行列    |
| CGAffineTransform(scaleX: CGFloat, y: CGFloat)                                              | 指定したスケーリング値から構築されたアフィン変換行列 |
| CGAffineTransform(translationX: CGFloat, y: CGFloat)                                        | 与えられた翻訳値から構築されたアフィン変換行列    |
| CGAffineTransform()                                                                         | アフィン変換行列                   |
| CGAffineTransform(a: CGFloat, b: CGFloat, c: CGFloat, d: CGFloat, tx: CGFloat, ty: CGFloat) | アフィン変換行列                   |
| CGAffineTransform(from decoder: Decoder)                                                    | アフィン変換行列                   |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .transformEffect(CGAffineTransform())

#### blur

##### 意味

ガウスぼかしを適用

##### 使い方

    .blur(radius: 半径(CGFloat), opaque: 透明度を許可するか(Bool) = false)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .blur(radius: 2.0)

#### opacity

##### 意味

透明度を設定

##### 使い方

    .opacity(透明度(Double))

##### 補足

透明度は0から1までの値のみ

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .opacity(0.5)

#### brightness

##### 意味

指定された値だけ明るくします

##### 使い方

    .brightness(明るさ(Double))

##### 補足

明るさは0から1までの値のみ

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .brightness(0.3)

#### contrast

##### 意味

類似した色の間のコントラストと分離を設定

##### 使い方

    .contrast(コントラストの強さ(Double))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .contrast(0.3)

#### colorInvert

##### 意味

色を反転

##### 使い方

    .colorInvert()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .colorInvert()

#### colorMultiply

##### 意味

色乗算効果を追加

##### 使い方

    .colorMultiply(色(Color))

##### Colorの使い方

| 名前                                                                                                | 説明                  |
| ------------------------------------------------------------------------------------------------- | ------------------- |
| Color.primary                                                                                     | メインカラー              |
| Color.secondary                                                                                   | サブカラー               |
| Color.accentColor                                                                                 | システムまたはアプリのアクセントカラー |
| Color.black                                                                                       | 黒色                  |
| Color.blue                                                                                        | 青色                  |
| Color.brown                                                                                       | 茶色                  |
| Color.clear                                                                                       | 透明色                 |
| Color.cyan                                                                                        | シアン色                |
| Color.gray                                                                                        | 灰色                  |
| Color.green                                                                                       | 緑色                  |
| Color.indigo                                                                                      | インディゴ色              |
| Color.mint                                                                                        | ミント色                |
| Color.orange                                                                                      | オレンジ色               |
| Color.pink                                                                                        | ピンク色                |
| Color.purple                                                                                      | 紫色                  |
| Color.red                                                                                         | 赤色                  |
| Color.teal                                                                                        | ティール色               |
| Color.white                                                                                       | 白色                  |
| Color.yellow                                                                                      | 黄色                  |
| Color(Color.RGBColorSpace = .sRGB, red: Double, green: Double, blue: Double, opacity: Double = 1) | 個別作成                |
| Color(Color.RGBColorSpace = .sRGB, white: Double, opacity: Double = 1)                            | 個別作成                |
| Color(hue: Double, saturation: Double, brightness: Double, opacity: Double = 1)                   | 個別作成                |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .colorMultiply(Color.green)

#### saturation

##### 意味

彩度を調整

##### 使い方

    .saturation(彩度(Double))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .saturation(0.3)

#### grayscale

##### 意味

グレースケール効果を追加

##### 使い方

    .grayscale(グレースケールの強度(Double))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .grayscale(0.3)

#### hueRotation

##### 意味

色相回転効果を適用

##### 使い方

    .hueRotation(角度(Angle))

##### Angleの使い方

| 名前               | 説明      |
| ---------------- | ------- |
| .degrees(Double) | 度を指定    |
| .radians(Double) | ラジアンを指定 |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .hueRotation(.degrees(10))

#### luminanceToAlpha

##### 意味

アルファ効果に輝度を追加

##### 使い方

    .luminanceToAlpha()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())    
        .luminanceToAlpha()

#### shadow

##### 意味

影を追加

##### 使い方

    .shadow(color: 影の色(Color) = Color(.sRGBLinear, white: 0, opacity: 0.33), radius: 影のサイズ(CGFloat), x: 水平位置(CGFloat) = 0, y: 垂直位置(CGFloat) = 0)

##### Colorの使い方

| 名前                                                                                                | 説明                  |
| ------------------------------------------------------------------------------------------------- | ------------------- |
| Color.primary                                                                                     | メインカラー              |
| Color.secondary                                                                                   | サブカラー               |
| Color.accentColor                                                                                 | システムまたはアプリのアクセントカラー |
| Color.black                                                                                       | 黒色                  |
| Color.blue                                                                                        | 青色                  |
| Color.brown                                                                                       | 茶色                  |
| Color.clear                                                                                       | 透明色                 |
| Color.cyan                                                                                        | シアン色                |
| Color.gray                                                                                        | 灰色                  |
| Color.green                                                                                       | 緑色                  |
| Color.indigo                                                                                      | インディゴ色              |
| Color.mint                                                                                        | ミント色                |
| Color.orange                                                                                      | オレンジ色               |
| Color.pink                                                                                        | ピンク色                |
| Color.purple                                                                                      | 紫色                  |
| Color.red                                                                                         | 赤色                  |
| Color.teal                                                                                        | ティール色               |
| Color.white                                                                                       | 白色                  |
| Color.yellow                                                                                      | 黄色                  |
| Color(Color.RGBColorSpace = .sRGB, red: Double, green: Double, blue: Double, opacity: Double = 1) | 個別作成                |
| Color(Color.RGBColorSpace = .sRGB, white: Double, opacity: Double = 1)                            | 個別作成                |
| Color(hue: Double, saturation: Double, brightness: Double, opacity: Double = 1)                   | 個別作成                |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .shadow(color: Color.gray,radius: 1.0)

#### blendMode

##### 意味

ブレンドモードを設定

##### 使い方

    .blendMode(モード(BlendMode))

##### BlendModeの使い方

| 名前               | 説明         |
| ---------------- | ---------- |
| .color           | カラー        |
| .colorBurn       | 焼き込みカラー    |
| .colorDodge      | 覆い焼きカラー    |
| .darken          | 比較(暗)      |
| .destinationOut  | 重なる部分を透過   |
| .destinationOver | 重ならない部分を透明 |
| .difference      | 差の絶対値      |
| .exclusion       | 除外         |
| .hardLight       | ハードライト     |
| .hue             | 色相         |
| .lighten         | 比較(明)      |
| .luminosity      | 輝度         |
| .multiply        | 乗算         |
| .normal          | ノーマル       |
| .overlay         | オーバーレイ     |
| .plusDarker      | 明るく        |
| .plusLighter     | 暗く         |
| .saturation      | 彩度         |
| .screen          | スクリーン      |
| .softLight       | ソフトライト     |
| .sourceAtop      | 透過         |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .blendMode(.colorBurn)

#### compositingGroup

##### 意味

合成グループにラップ

##### 使い方

    .compositingGroup()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .compositingGroup()

#### drawingGroup

##### 意味

最終的な表示の前にコンテンツをオフスクリーンイメージに合成

##### 使い方

    .drawingGroup(opaque: 不透明かどうか(Bool) = false, colorMode: フォーマット(ColorRenderingMode) = .nonLinear)

##### ColorRenderingModeの使い方

| 名前              | 説明                                          |
| --------------- | ------------------------------------------- |
| .extendedLinear | 線形のsRGB作業色空間で範囲[0,1]外の色成分値が保存               |
| .linear         | 直線的なsRGB作業色空間で色成分の値が範囲[0,1]外の場合は定義されない結果    |
| .nonLinear      | 非線形のsRGB作業用色空間で色成分の値が範囲[0,1]外の場合は定義されていない結果 |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .drawingGroup()

#### animation

##### 意味

指定されたアニメーションを設定

##### 使い方

    .animation(アニメーション(Animation))

    .animation(アニメーション(Animation), value: 変更を監視する値)

    .animation(value: 変更を監視する値(Equatable))

    .animation()

##### Animationの使い方

| 名前                                                                                                          | 説明       |
| ----------------------------------------------------------------------------------------------------------- | -------- |
| .default                                                                                                    | デフォルト    |
| .easeIn                                                                                                     | 徐々に加速    |
| .easeInOut                                                                                                  | 加速してから減速 |
| .easeOut                                                                                                    | 徐々に減速    |
| .linear                                                                                                     | 等速で変化    |
| .easeIn(duration: Double)                                                                                   | 徐々に加速    |
| .easeInOut(duration: Double)                                                                                | 加速してから減速 |
| .easeOut(duration: Double)                                                                                  | 徐々に減速    |
| .interactiveSpring(response: Double = 0.15, dampingFraction: Double = 0.86, blendDuration: Double = 0.25)   | レスポンス値の低いスプリング          |
| .interpolatingSpring(mass: Double = 1.0, stiffness: Double, damping: Double, initialVelocity: Double = 0.0) | 補間スプリングアニメーション         |
| .linear(duration: Double)                                                                                   | 等速で変化    |
| .spring(response: Double = 0.55, dampingFraction: Double = 0.825, blendDuration: Double = 0)                | 永続的なスプリングアニメーション         |
| .timingCurve(Double, Double, Double, Double, duration: Double = 0.35)                                       | タイミングカーブ         |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .animation(.default)

#### transition

##### 意味

遷移をビューに関連付けます

##### 使い方

    .transition(トランジション効果(AnyTransition))

##### AnyTransitionの使い方

| 名前                                                                    | 説明                                                     |
| --------------------------------------------------------------------- | ------------------------------------------------------ |
| .identity                                                             | 入力ビューを修正せずに出力ビューとして返すトランジション                           |
| .opacity                                                              | 挿入時には透明から不透明へ取り出し時には不透明から透明へと変化                        |
| .scale                                                                |                                                        |
| .slide                                                                | リーディングエッジからインすることで挿入しトレーリングエッジに向かってアウトすることで除去するトランジション |
| .asymmetric(insertion: AnyTransition, removal: AnyTransition)         | 挿入と削除で異なるトランジションを使用する複合トランジション                                                       |
| .modifier<ViewModifier>(active: ViewModifier, identity: ViewModifier) | アクティブモディファイアとアイデンティティモディファイアの間で定義されているトランジション                                                       |
| .move(edge: Edge)                                                     | ビューの指定されたエッジに向かってビューを遠ざけるトランジション                                                       |
| .offset(CGSize)                                                       |                                                        |
| .offset(x: CGFloat = 0, y: CGFloat = 0)                               |                                                        |
| .scale(scale: CGFloat, anchor: UnitPoint = .center)                   |                                                        |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .transition(.slide)

#### matchedGeometryEffect

##### 意味

指定された識別子と名前空間を使用してジオメトリが同期したビューグループを定義

##### 使い方

    .matchedGeometryEffect(id: "識別子(Hashable)", in: ネームスペースID(Namespace.ID), properties: ソースビューからコピーするプロパティ(MatchedGeometryProperties) = .frame, anchor: 相対的な位置(UnitPoint) = .center, isSource: 他のビューのジオメトリのソースとしてビューを使用する場合か(Bool) = true)

##### MatchedGeometryPropertiesの使い方

| 名前                                                       | 説明                       |
| -------------------------------------------------------- | ------------------------ |
| .frame                                                   | サイズと配置位置                 |
| .position                                                | ビューの位置をウィンドウ座標で表示        |
| .size                                                    | ローカル座標でのビューのサイズ          |
| MatchedGeometryProperties()                              | 空のオプションセットを作成            |
| MatchedGeometryProperties<Sequence>(Sequence)            | アイテムの有限のシーケンスから新しいセットを作成 |
| MatchedGeometryProperties(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成  |
| MatchedGeometryProperties(rawValue: UInt32)              | 与えられた生の値から新しいオプションセットを作成 |

##### 相対的なUnitPointの使い方

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

##### 例

    @Namespace var hogeNamespace
    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .matchedGeometryEffect(id: "orangeCircle", in: hogeNamespace)

#### hidden

##### 意味

非表示

##### 使い方

    .hidden()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .hidden()

#### disabled

##### 意味

ユーザーが操作できるかどうかを制御する条件を追加

##### 使い方

    .disabled(操作できるか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .disabled(false)

#### handlesExternalEvents

##### 意味

含まれるシーンが一致する外部イベントを処理できることを示す修飾子を指定

##### 使い方

    .handlesExternalEvents(preferring: 識別子(Set<String>), allowing: 識別子(Set<String>))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .handlesExternalEvents(preferring: Set(arrayLiteral: "hogeview"), allowing: Set(arrayLiteral: "hogeview"))

#### onTapGesture

##### 意味

タップジェスチャーを認識したときに実行するアクションを追加

##### 使い方

    .onTapGesture(count: タップ回数(Int) = 1) {
        実装するアクション(View)
    }

    .onTapGesture(count: タップ回数(Int) = 1, perform: 実装するアクション(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onTapGesture() {
            // アクション
        }

#### onLongPressGesture

##### 意味

長押しジェスチャーを認識したときに実行するアクションを追加

##### 使い方

    .onLongPressGesture(minimumDuration: 最小判定時間(Double) = 0.5, maximumDistance: 最大判定距離(CGFloat) = 10, pressing: 判定(Bool) = nil) {
        実行するアクション(View)
    }

    .onLongPressGesture(minimumDuration: 最小判定時間(Double) = 0.5, maximumDistance: 最大判定距離(CGFloat) = 10, pressing: 判定(Bool) = nil, perform: 実行するアクション(View))

    .onLongPressGesture(minimumDuration: 最小判定時間(Double) = 0.5, pressing: 判定(Bool) = nil) {
        実行するアクション(View)
    }

    .onLongPressGesture(minimumDuration: 最小判定時間(Double) = 0.5, pressing: 判定(Bool) = nil, perform: 実行するアクション(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onLongPressGesture(minimumDuration: 0.5) {
            // アクション
        }

#### gesture

##### 意味

カスタムジェスチャを追加

##### 使い方

    .gesture(ジェスチャ(Gesture), including: イベントのマスク(GestureMask) = .all)

##### Gestureの使い方

| 名前                                                                                                                                                               | 説明                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| AnyGesture<Gesture>(Gesture)                                                                                                                                     | 型抜きされたジェスチャー                          |
| DragGesture(minimumDistance: CGFloat = 10, coordinateSpace: CoordinateSpace = .local)                                                                            | ドラッグ処理                                |
| ExclusiveGesture(First, Second)                                                                                                                                  | 2つのジェスチャーで構成されたどちらか一方しか成功しないジェスチャー    |
| GestureStateGesture(base: Base, state: GestureState<State>, body: @escaping (GestureStateGesture&lt;Base, State>.Value, inout State, inout Transaction) -> Void) | ジェスチャーの更新コールバックによって提供された状態を更新するジェスチャー |
| LongPressGesture(minimumDuration: Double = 0.5, maximumDistance: CGFloat = 10)                                                                                   | ユーザーが長押しをすると成功するジェスチャー                |
| MagnificationGesture(minimumScaleDelta: CGFloat = 0.01)                                                                                                          | 拡大動作を認識し拡大値を追跡するジェスチャー                |
| RotationGesture(minimumAngleDelta: Angle = .degrees(1))                                                                                                          | 回転動作を認識しその回転角度を追跡するジェスチャー             |
| SequenceGesture(First, Second)                                                                                                                                   | 2つのジェスチャーを連続させたジェスチャー                 |
| SimultaneousGesture(First, Second)                                                                                                                               | 同時に起こりうる2つのジェスチャーを含みどちらも先行しないジェスチャー   |
| TapGesture(count: Int = 1)                                                                                                                                       | 1回または複数回のタップを認識するジェスチャー               |

##### GestureMaskの使い方

| 名前                                         | 説明                                    |
| ------------------------------------------ | ------------------------------------- |
| .all                                       | すべてのジェスチャーを有効                         |
| .gesture                                   | 追加されたジェスチャーを有効にしサブビュー階層のすべてのジェスチャーを無効 |
| .subviews                                  | サブビュー階層のすべてのジェスチャーを有効にし追加されたジェスチャーを無効 |
| .none                                      | すべてのジェスチャーを無効                         |
| GestureMask()                              | 空のオプションセットを作成                         |
| GestureMask<Sequence>(Sequence)            | アイテムの有限のシーケンスから新しいセットを作成              |
| GestureMask(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成               |
| GestureMask(rawValue: UInt32)              | 与えられた生の値から新しいオプションセットを作成              |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .gesture(DragGesture())

#### highPriorityGesture

##### 意味

ビューで定義されたジェスチャよりも優先度の高いジェスチャをビューにアタッチ

##### 使い方

    .highPriorityGesture(ジェスチャ(Gesture), including: イベントのマスク(GestureMask) = .all)

##### Gestureの使い方

| 名前                                                                                                                                                               | 説明                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| AnyGesture<Gesture>(Gesture)                                                                                                                                     | 型抜きされたジェスチャー                          |
| DragGesture(minimumDistance: CGFloat = 10, coordinateSpace: CoordinateSpace = .local)                                                                            | ドラッグ処理                                |
| ExclusiveGesture(First, Second)                                                                                                                                  | 2つのジェスチャーで構成されたどちらか一方しか成功しないジェスチャー    |
| GestureStateGesture(base: Base, state: GestureState<State>, body: @escaping (GestureStateGesture&lt;Base, State>.Value, inout State, inout Transaction) -> Void) | ジェスチャーの更新コールバックによって提供された状態を更新するジェスチャー |
| LongPressGesture(minimumDuration: Double = 0.5, maximumDistance: CGFloat = 10)                                                                                   | ユーザーが長押しをすると成功するジェスチャー                |
| MagnificationGesture(minimumScaleDelta: CGFloat = 0.01)                                                                                                          | 拡大動作を認識し拡大値を追跡するジェスチャー                |
| RotationGesture(minimumAngleDelta: Angle = .degrees(1))                                                                                                          | 回転動作を認識しその回転角度を追跡するジェスチャー             |
| SequenceGesture(First, Second)                                                                                                                                   | 2つのジェスチャーを連続させたジェスチャー                 |
| SimultaneousGesture(First, Second)                                                                                                                               | 同時に起こりうる2つのジェスチャーを含みどちらも先行しないジェスチャー   |
| TapGesture(count: Int = 1)                                                                                                                                       | 1回または複数回のタップを認識するジェスチャー               |

##### GestureMaskの使い方

| 名前                                         | 説明                                    |
| ------------------------------------------ | ------------------------------------- |
| .all                                       | すべてのジェスチャーを有効                         |
| .gesture                                   | 追加されたジェスチャーを有効にしサブビュー階層のすべてのジェスチャーを無効 |
| .subviews                                  | サブビュー階層のすべてのジェスチャーを有効にし追加されたジェスチャーを無効 |
| .none                                      | すべてのジェスチャーを無効                         |
| GestureMask()                              | 空のオプションセットを作成                         |
| GestureMask<Sequence>(Sequence)            | アイテムの有限のシーケンスから新しいセットを作成              |
| GestureMask(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成               |
| GestureMask(rawValue: UInt32)              | 与えられた生の値から新しいオプションセットを作成              |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .highPriorityGesture(DragGesture())

#### simultaneousGesture

##### 意味

ビューに定義されたジェスチャーと同時に処理するジェスチャーをビューにアタッチ

##### 使い方

    .simultaneousGesture(ジェスチャ(Gesture), including: イベントのマスク(GestureMask) = .all)

##### Gestureの使い方

| 名前                                                                                                                                                               | 説明                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| AnyGesture<Gesture>(Gesture)                                                                                                                                     | 型抜きされたジェスチャー                          |
| DragGesture(minimumDistance: CGFloat = 10, coordinateSpace: CoordinateSpace = .local)                                                                            | ドラッグ処理                                |
| ExclusiveGesture(First, Second)                                                                                                                                  | 2つのジェスチャーで構成されたどちらか一方しか成功しないジェスチャー    |
| GestureStateGesture(base: Base, state: GestureState<State>, body: @escaping (GestureStateGesture&lt;Base, State>.Value, inout State, inout Transaction) -> Void) | ジェスチャーの更新コールバックによって提供された状態を更新するジェスチャー |
| LongPressGesture(minimumDuration: Double = 0.5, maximumDistance: CGFloat = 10)                                                                                   | ユーザーが長押しをすると成功するジェスチャー                |
| MagnificationGesture(minimumScaleDelta: CGFloat = 0.01)                                                                                                          | 拡大動作を認識し拡大値を追跡するジェスチャー                |
| RotationGesture(minimumAngleDelta: Angle = .degrees(1))                                                                                                          | 回転動作を認識しその回転角度を追跡するジェスチャー             |
| SequenceGesture(First, Second)                                                                                                                                   | 2つのジェスチャーを連続させたジェスチャー                 |
| SimultaneousGesture(First, Second)                                                                                                                               | 同時に起こりうる2つのジェスチャーを含みどちらも先行しないジェスチャー   |
| TapGesture(count: Int = 1)                                                                                                                                       | 1回または複数回のタップを認識するジェスチャー               |

##### GestureMaskの使い方

| 名前                                         | 説明                                    |
| ------------------------------------------ | ------------------------------------- |
| .all                                       | すべてのジェスチャーを有効                         |
| .gesture                                   | 追加されたジェスチャーを有効にしサブビュー階層のすべてのジェスチャーを無効 |
| .subviews                                  | サブビュー階層のすべてのジェスチャーを有効にし追加されたジェスチャーを無効 |
| .none                                      | すべてのジェスチャーを無効                         |
| GestureMask()                              | 空のオプションセットを作成                         |
| GestureMask<Sequence>(Sequence)            | アイテムの有限のシーケンスから新しいセットを作成              |
| GestureMask(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成               |
| GestureMask(rawValue: UInt32)              | 与えられた生の値から新しいオプションセットを作成              |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .simultaneousGesture(DragGesture())

#### transaction

##### 意味

指定されたトランザクション変更関数をビュー内で使用されるすべてのトランザクションに適用

##### 使い方

    .transaction() {
        トランザクションに適用する変換(View)
    }

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .transaction { view in
            view.animation = .interactiveSpring(
                response: 0.60,
                dampingFraction: 0.20,
                blendDuration: 0.25)
        }

#### userActivity

##### 意味

ユーザーのアクティビティタイプを広告

##### 使い方

    .userActivity("宣伝する活動の種類", element: "要素") {
        アクティビティを広告用に修正する機能(View)
    }

    .userActivity("宣伝する活動の種類", isActive: アクティビティの広告を回避するか(Bool)) {
        アクティビティを広告用に修正する機能(View)
    }

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .userActivity("bundleIdentifier.Board", isActive: true) { _ in
            // ビュー
        }

#### onContinueUserActivity

##### 意味

指定されたアクティビティタイプを受信したときに呼び出すハンドラを登録

##### 使い方

    .onContinueUserActivity("処理するアクティビティの種類") {
        NSUserActivityオブジェクトをパラメータとして受け取る呼び出し関数(View)
    }

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onContinueUserActivity("hoge") { _ in
            // ビュー
        }

#### onCopyCommand

##### 意味

システムのコピーコマンドに応じて実行するアクションを追加

##### 使い方

    .onCopyCommand(perform: {
        コピー時に実行されるアクション(View)
    })

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onCopyCommand(perform: {
            let items: [NSItemProvider] = []
            return items
        })

#### onCutCommand

##### 意味

システムのCutコマンドに応答して実行するアクションを追加

##### 使い方

    .onCutCommand(perform: {
        Cut時に実行されるアクション(View)
    })

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onCutCommand(perform: {
            let items: [NSItemProvider] = []
            return items
        })

#### onPasteCommand

##### 意味

システムのPasteコマンドに対応して実行するアクションを追加

##### 使い方

    .onPasteCommand(of: [ユニフォームタイプ識別子(UTType)]) { プロバイダー([NSItemProvider]) in
        pasteコマンドがトリガーされたときに実行するアクション(View)
    }

    .onPasteCommand(of: [ユニフォームタイプ識別子(UTType)], validator: コマンドを検証するハンドラ) { プロバイダー([NSItemProvider]) in
        貼り付けコマンドがトリガーされたときに実行するアクション(View)
    }

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onPasteCommand(of: [String]()) { _ in
            // アクション
        }

#### onDrag

##### 意味

ドラッグアンドドロップ操作のソースとしてアクティブ

##### 使い方

    .onDrag() {
        ドラッグ可能なデータ(NSItemProvider)
    }

    .onDrag(of: ユニフォームタイプ識別子の配列([UTType]), delegate: デリゲート(DropDelegate))

    .onDrop(of: ユニフォームタイプ識別子の配列([UTType]), isTargeted: 更新されるバインディング(Binding<Bool>)?) { プロバイダー[NSItemProvider] in
        アクション
    }

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onDrag() {
            let items: NSItemProvider = NSItemProvider()
            return items
        }

#### itemProvider

##### 意味

特定のデータ要素に使用されるドラッグ表現を提供するクロージャを提供

##### 使い方

    .itemProvider {
        クロージャ(NSItemProvider)
    }

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
         .itemProvider {
            let items: NSItemProvider = NSItemProvider()
            return items
        }

#### onOpenURL

##### 意味

URLを受信したときに起動するハンドラを登録

##### 使い方

    .onOpenURL() { 引数 in
        URLを配信する関数(View)
    }

    .onOpenURL(perform: URLを配信する関数(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onOpenURL() { _ in
            // 処理内容                
        }

#### onMoveCommand

##### 意味

ユーザーがMacキーボードの矢印キーを押したときやApple TVを制御しているときにSiri Remoteの端をタップしたときなど移動コマンドに応じて実行するアクションを追加

##### 使い方

    .onMoveCommand { 引数 in
        移動時に実行されるアクション(View)
    }

    .onMoveCommand(perform: 移動時に実行されるアクション(View))

    .onMoveCommand()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onMoveCommand { direction in
            print(direction)
        }

#### moveDisabled

##### 意味

ビュー階層が移動可能かどうかの条件を追加

##### 使い方

    .moveDisabled(移動可能かどうか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .moveDisabled(true)

#### onDeleteCommand

##### 意味

システムの削除コマンドに応じて実行するアクションを追加

##### 使い方

    .onDeleteCommand {
        削除時に実行されるアクション(View)
    }

    .onDeleteCommand(perform: {
        削除時に実行されるアクション(View)
    })

    .onDeleteCommand()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onDeleteCommand {
            // アクション
        }

#### deleteDisabled

##### 意味

ビュー階層が削除可能かどうかの条件を追加

##### 使い方

    .deleteDisabled(削除可能かどうか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .deleteDisabled(true)

#### pageCommand

##### 意味

ページアップやページダウンのコマンドに応じて値を範囲内でステップ

##### 使い方

    .pageCommand(value: ユーザーがページアップやダウンしたときに変更する値へのバインディング(Binding<V>), in: 値の上限と下限を指定する閉じた範囲(ClosedRange), step: 値を増加または減少させる値を指定(BinaryInteger))

#### onExitCommand

##### 意味

ビューにフォーカスがあるときにexitコマンドの受信に応答してトリガーされるアクションを設定

##### 使い方

    .onExitCommand {
        エスケープキーを押したときに実行されるアクション(View)
    }

    .onExitCommand(perform: エスケープキーを押したときに実行されるアクション(View))

    .onExitCommand()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onExitCommand {
            // アクション
        }

#### onPlayPauseCommand

##### 意味

システムの再生/一時停止コマンドに応答して実行するアクションを追加

##### 使い方

    .onPlayPauseCommand {
        再生/一時停止コマンド時に実行されるアクション(View)
    }

    .onPlayPauseCommand(perform: 再生/一時停止コマンド時に実行されるアクション(View))

    .onPlayPauseCommand()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onPlayPauseCommand {
            // アクション
        }

#### onCommand

##### 意味

指定されたセレクターに応答して実行するアクションを追加

##### 使い方

    .onCommand(登録するセレクタ(Selector))  {
        実行するアクション(View)
    }

    .onCommand(登録するセレクタ(Selector), perform: 実行するアクション(View))

    .onCommand(登録するセレクタ(Selector))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onCommand(#selector(Commands.hoge)) {
            print("Selection: \(self.selection)")
        }

#### onAppear

##### 意味

表示されたときに実行するアクションを追加

##### 使い方

    .onAppear {
        実行するアクション(View)
    }

    .onAppear(perform: 実行するアクション(View))

    .onAppear()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onAppear {
            // アクション
        }

#### onDisappear

##### 意味

非表示になった時に実行するアクションを追加

##### 使い方

    .onDisappear {
        実行するアクション(View)
    }

    .onDisappear(perform: 実行するアクション(View))

    .onDisappear()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onDisappear {
            // アクション
        }

#### onChange

##### 意味

特定の値が変化したときにアクションを発生させるメソッドを追加

##### 使い方

    .onChange(of: クロージャを実行するかどうかを判断する際にチェックする値(Equatable)) { 引数(Equatable) in
        値が変化したときに実行するクロージャー(View)
    }

    .onChange(of: クロージャを実行するかどうかを判断する際にチェックする値(Equatable), perform: 値が変化したときに実行するクロージャー(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onChange(of: "hoge") { _ in
            // アクション
        }

#### onReceive

##### 意味

特定のパブリッシャーによって発行されたデータを検出したときに実行するアクションを追加

##### 使い方

    .onReceive(購読するパブリッシャー(Publisher)) {
        実行するアクション(View)
    }

    .onReceive(購読するパブリッシャー(Publisher), perform: {
        実行するアクション(View)
    })

#### keyboardShortcut

##### 意味

変更したコントロールにキーボードショートカットを割り当て

##### 使い方

    .keyboardShortcut(キーボードショートカット(KeyboardShortcut))

    .keyboardShortcut(キー(KeyEquivalent), イベント(EventModifiers) = .command)

##### KeyboardShortcutの使い方

| 名前                                                                    | 説明                                     |
| --------------------------------------------------------------------- | -------------------------------------- |
| .cancelAction                                                         | Escapeキー                               |
| .defaultAction                                                        | Returnキー                               |
| KeyboardShortcut(KeyEquivalent, modifiers: EventModifiers = .command) | 与えられた同等のキーと修飾キーのセットで新しいキーボードショートカットを作成 |

##### EventModifiersの使い方

| 名前                                            | 説明                       |
| --------------------------------------------- | ------------------------ |
| .all                                          | 全て                       |
| .capsLock                                     | Caps Lock キー             |
| .command                                      | Commandキー                |
| .control                                      | Controlキー                |
| .function                                     | Functionキー               |
| .numericPad                                   | テンキー                     |
| .option                                       | Optionキー                 |
| .shift                                        | Shiftキー                  |
| EventModifiers()                              | 空のオプションセットを作成            |
| EventModifiers<Sequence>(Sequence)            | アイテムの有限のシーケンスから新しいセットを作成 |
| EventModifiers(arrayLiteral: Self.Element...) | 与えられた配列リテラルの要素を含むセットを作成  |
| EventModifiers(rawValue: Int)                 | 生の値から新しいセットを作成           |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .keyboardShortcut("r", modifiers: .command)

#### onHover

##### 意味

ユーザーがポインターをビューのフレームの上または外に移動したときに実行するアクションを追加

##### 使い方

    .onHover { 変数(Bool) in
        実行するアクション(Void)
    }

    .onHover(perform: 実行するアクション(Void))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onHover { _ in
            // アクション
        }

#### hoverEffect

##### 意味

ポインターホバー効果を適用

##### 使い方

    .hoverEffect(ポインターホバー効果(HoverEffect) = .automatic)

##### HoverEffectの使い方

| 名前         | 説明    |
| ---------- | ----- |
| .automatic | 自動    |
| .highlight | ハイライト |
| .lift      | シャドー  |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .hoverEffect(.automatic)

#### focusable

##### 意味

ビューがフォーカス可能かどうかを指定し可能であればビューがフォーカスされたときに実行するアクションを追加

##### 使い方

    .focusable(フォーカス可能かどうか(Bool) = true) {
        フォーカスの変更時に実行されるアクション = { _ in })
    }

    .focusable(フォーカス可能かどうか(Bool) = true, onFocusChange: {
        フォーカスの変更時に実行されるアクション = { _ in }
    })

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .focusable()

#### focusedValue

##### 意味

フォーカスされたビュー階層に状態が依存する他のビューが使用するために提供する値を注入して変更

##### 使い方

    .focusedValue(値を関連付けるキーパス(WritableKeyPath<FocusedValues, Value?>), エクスポートへのフォーカス値(Value))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .focusedValue(\.hoge, .$hogeValue)

#### prefersDefaultFocus

##### 意味

ネームスペースのデフォルトでフォーカスされることを好むかどうかを設定

##### 使い方

    .prefersDefaultFocus(デフォルトでフォーカスされるか(Bool) = true, in: ネームスペース(Namespace.ID))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .prefersDefaultFocus(false, in: menuItems)

#### focusScope

##### 意味

デフォルトのフォーカス設定を制限するために使用できるフォーカススコープを作成

##### 使い方

    .focusScope(ネームスペース(Namespace.ID))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .focusScope(namespace)

#### digitalCrownRotation

##### 意味

指定されたバインディングを更新することによりデジタルクラウンの回転を追跡

##### 使い方

    .digitalCrownRotation($更新される値(Binding<V>))

    .digitalCrownRotation($更新される値(Binding<V>), from: 範囲の下限(BinaryFloatingPoint), through: 範囲の上限(BinaryFloatingPoint), by: 倍数(V.Stride) = nil, sensitivity: 回転量(DigitalCrownRotationalSensitivity) = .high, isContinuous: 連続(Bool) = false, isHapticFeedbackEnabled: フィードバックが有効か(Bool) = ture)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .digitalCrownRotation($crownValue)

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .digitalCrownRotation($crownValue, from: minValue, through: maxValue, by: stepAmount, sensitivity: .low, isContinuous: true)

#### allowsHitTesting

##### 意味

ヒットテスト操作に参加するかどうかを構成

##### 使い方

    .allowsHitTesting(参加するか(Bool))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .allowsHitTesting(true)

#### contentShape

##### 意味

ヒットテストのコンテンツ形状を定義

##### 使い方

    .contentShape(形状(Shape), eoFill: 解釈されるか(Bool) = false)

##### 形状の作成方法(Shape)

| 名前                                                                                      | 説明                             |
| --------------------------------------------------------------------------------------- | ------------------------------ |
| Capsule(style: RoundedCornerStyle = .circular)                                          | カプセル形状はそれを含むビューのフレーム内に整列       |
| Circle()                                                                                | ビューのフレームを中心とした円                |
| ContainerRelativeShape()                                                                | 現在のコンテナ形状のインセットバージョンで置き換えられる形状 |
| Ellipse()                                                                               | 楕円はそれを含むビューのフレーム内に整列           |
| OffsetShape(shape: Content, offset: CGSize)                                             | 並進オフセット変換が適用された形状              |
| Path()                                                                                  | 任意のパスにあわせて描画                   |
| Path((inout Path))                                                                      | 任意のパスにあわせて描画                   |
| Path(CGMutablePath)                                                                     | 任意のパスにあわせて描画                   |
| Path(CGPath)                                                                            | 任意のパスにあわせて描画                   |
| Path(String)                                                                            | 任意のパスにあわせて描画                   |
| Path(CGRect)                                                                            | 任意のパスにあわせて描画                   |
| Path(ellipseIn rect: CGRect)                                                            | 任意のパスにあわせて描画                   |
| Path(roundedRect: CGRect, cornerRadius: CGFloat, style: RoundedCornerStyle = .circular) | 任意のパスにあわせて描画                   |
| Path(roundedRect: CGRect, cornerSize: CGSize, style: RoundedCornerStyle = .circular)    | 任意のパスにあわせて描画                   |
| TransformedShape(shape: Circle(), transform: CGAffineTransform())                       | 矩形の形状はそれを含むビューのフレーム内に配置        |
| RotatedShape(shape: Content, angle: Angle, anchor: UnitPoint = .center)                 | 回転トランスフォームが適用された図形             |
| RoundedRectangle(cornerRadius: CGFloat, style: RoundedCornerStyle = .circular)          | 角の丸い長方形でそれを含むビューのフレーム内に配置      |
| RoundedRectangle(cornerSize: CGSize, style: RoundedCornerStyle = .circular)             | 角の丸い長方形でそれを含むビューのフレーム内に配置      |
| ScaledShape(shape: Content, scale: CGSize, anchor: UnitPoint = .center)                 | スケールトランスフォームが適用された形状           |
| TransformedShape(shape: Content, transform: CGAffineTransform)                          | アフィン変換が適用された形状                 |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .contentShape(TransformedShape(shape: Circle(), transform: CGAffineTransform()))

#### actionSheet

##### 意味

指定したビューをアクションシート表示

##### 使い方

    .actionSheet(isPresented: 表示するか(Binding<Bool>)) {
        クロージャ(ActionSheet)
    }

    .actionSheet(isPresented: 表示するか(Binding<Bool>), content: {
        クロージャ(ActionSheet)
    })

    .actionSheet(item: バインディング(Binding<T?>) {
        クロージャ(ActionSheet)
    }

    .actionSheet(item: バインディング(Binding<T?>), content: {
        クロージャ(ActionSheet)
    })

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .actionSheet(isPresented: $isShowingSheet) {
            ActionSheet(
                title: Text("タイトル"),
                message: Text("メッセージ"),
                buttons:[
                    .cancel()
                ]
            )}

#### sheet

##### 意味

指定したビューをモーダル表示

##### 使い方

    .sheet(isPresented: $シートが表示されるか(Binding<Bool>), onDismiss: モーダルを閉じるときに実行する処理(() -> Void), content: モーダル表示するビュー(Content))

    .sheet(item: バインディング(Binding<Item?>), onDismiss: モーダルを閉じるときに実行する処理(() -> Void), content: モーダル表示するビュー(Content)) 

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .sheet(isPresented: $isShowingSheet, onDismiss: {}) {
            Text("メッセージ")
        }

#### fullScreenCover

##### 意味

指定したブール値へのバインディングがtrueの場合に画面をできるだけ多く覆うモーダルビューを提示

##### 使い方

    .fullScreenCover(isPresented: $シートを表示するかどうかを決定する値(Binding<Bool>), onDismiss: モーダルビューを閉じるときに実行するクロージャー(() -> Void) = nil, content: モーダルビューのモーダル表示するビュー(Content))

    .fullScreenCover(item: バインディング値(Binding<Bool>), onDismiss: モーダルビューを閉じるときに実行するクロージャー(() -> Void) = nil, content: モーダルビューのモーダル表示するビュー(Content))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .fullScreenCover(isPresented: $isPresenting, onDismiss: {}) {
            Text("メッセージ")
        }

#### alert

##### 意味

ユーザーに警告を表示

##### 使い方

    .alert(isPresented: 表示するか(Binding<Bool>)) {
        クロージャー(Alert)
    }

    .alert(isPresented: 表示するか(Binding<Bool>), content: {
        クロージャー(Alert)
    })

    .alert(item: バインディング) {
        クロージャー
    }

    .alert(item: バインディング, content: {
        クロージャー
    })

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .alert(isPresented: $isPresented) {
            Alert(title: Button("Order Complete"),
                  message: Button("Thank you for shopping with us."),
                  dismissButton: .default(Button("OK")))
        }

#### popover

##### 意味

特定の条件がtrueの場合にポップオーバーを表示

##### 使い方

    .popover(isPresented: 表示されるか(Binding<Bool>), attachmentAnchor: 位置決めアンカー(PopoverAttachmentAnchor) = .rect(.bounds), arrowEdge: 辺(Edge) = .top) {
        クロージャー(Content)
    }

    .popover(isPresented: 表示されるか(Binding<Bool>), attachmentAnchor: 位置決めアンカー(PopoverAttachmentAnchor) = .rect(.bounds), arrowEdge: 辺(Edge) = .top, content: クロージャー(Content))

    .popover(item: バインディング(Binding<Item?>), attachmentAnchor: 位置決めアンカー(PopoverAttachmentAnchor) = .rect(.bounds), arrowEdge: 辺(Edge) = .top) {
        クロージャー(Content)
    }

    .popover(item: バインディング(Binding<Item?>), attachmentAnchor: 位置決めアンカー(PopoverAttachmentAnchor) = .rect(.bounds), arrowEdge: 辺(Edge) = .top, content: クロージャー(Content))

##### PopoverAttachmentAnchorの使い方

| 名前     | 説明                                |
| ------ | --------------------------------- |
| .point | SwiftUIのビューに対する可能な位置関係を示す単位点として表現 |
| .rect  | ソースのフレームを基準                       |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .popover(isPresented: $isShowingPopover) {
            PopoverView()
        }

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .popover(item: $popover) { detail in
            Button("\(detail.body)")
        }

#### fileExporter

##### 意味

メモリ内の文書をディスク上のファイルに書き出すためのシステムインターフェースを提供

##### 使い方

    .fileExporter(isPresented: インターフェイスを表示するかどうかのバインディング(Binding<Bool>), document: エクスポートするインメモリーのドキュメント(FileDocument), contentType: 書き出したファイルに使用するコンテンツタイプ, defaultFilename: "エクスポートされるファイルに使用されるデフォルトの名前") {
        成功または失敗したときに呼び出されるコールバック
    }

    .fileExporter(isPresented: インターフェイスを表示するかどうかのバインディング(Binding<Bool>), document: エクスポートするインメモリーのドキュメント(FileDocument), contentType: 書き出したファイルに使用するコンテンツタイプ, defaultFilename: "エクスポートされるファイルに使用されるデフォルトの名前", onCompletion: 成功または失敗したときに呼び出されるコールバック)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .fileExporter(isPresented: $isShowingExportDialog, document: store, contentType: Store.readableContentTypes.first!) { result in }

#### fileImporter

##### 意味

ユーザーが複数のファイルを取り込むためのシステムインターフェースを提供

##### 使い方

    .fileImporter(isPresented: $インターフェイスを表示するかどうかのバインディング(Binding<Bool>), allowedContentTypes: インポート可能なサポートされているコンテンツタイプのリスト([UTType]), allowsMultipleSelection: ユーザーが複数のファイルを選択してインポートできるかどうか(Bool)) {
        成功または失敗したときに呼び出されるコールバック
    }

    .fileImporter(isPresented: $インターフェイスを表示するかどうかのバインディング(Binding<Bool>), allowedContentTypes: インポート可能なサポートされているコンテンツタイプのリスト([UTType]), allowsMultipleSelection: ユーザーが複数のファイルを選択してインポートできるかどうか(Bool), onCompletion: 成功または失敗したときに呼び出されるコールバック)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .fileImporter(isPresented: $shareDirectoryFileImportPresented, allowedContentTypes: [.folder], onCompletion: selectShareDirectory)

#### fileMover

##### 意味

ユーザーが既存のファイルを新しい場所に移動させるためのシステムインターフェースを提供

##### 使い方

    .fileMover(isPresented: インターフェイスを表示するかどうかのバインディング(Binding<Bool>), file: 移動するファイルのURL(URL)?) {
        成功または失敗したときに呼び出されるコールバック(Result<URL, Error>) -> Void)
    }

    .fileMover(isPresented: インターフェイスを表示するかどうかのバインディング(Binding<Bool>), file: 移動するファイルのURL(URL)?, onCompletion: 成功または失敗したときに呼び出されるコールバック(Result<URL, Error>) -> Void)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .fileMover(isPresented: $displayAlert, file: URL(fileURLWithPath: "/")) {_ in 
            print("completing move")
        }

#### tag

##### 意味

一意のタグ値を設定

##### 使い方

    .tag(タグ名(Hashable))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .tag($0)

#### id

##### 意味

IDを指定されたプロキシ値にバインド

##### 使い方

    .id(プロキシ値(Hashable))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .id($0)

#### equatable

##### 意味

新しい値が古い値と同じ場合にビューが子ビューを更新しないようにする

##### 使い方

    .equatable()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .equatable()

#### defaultAppStorage

##### 意味

ビューに含まれるAppStorageが使用するデフォルトのストア

##### 使い方

    .defaultAppStorage(AppStorageのデフォルトのストアとして使用するユーザー(UserDefaults))

##### UserDefaultsの使い方

| 名前                                          | 説明                                               |
| ------------------------------------------- | ------------------------------------------------ |
| UserDefaults()                              | アプリと現在のユーザーのデフォルト値で初期化されたuser defaultsオブジェクトを作成  |
| UserDefaults?(suiteName suitename: String?) | 指定されたデータベース名のデフォルト値で初期化されたuser defaultsオブジェクトを作成 |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .defaultAppStorage(UserDefaults(suiteName: "user")!)

#### preference

##### 意味

指定された設定の値を設定

##### 使い方

    .preference(key: キー名(PreferenceKey.Type) = PreferenceKey.self, value: 値(PreferenceKey.Value))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .preference(key: MyPreferenceKey.self, value: MyPreferenceData(size: proxy.size))

#### transformPreference

##### 意味

設定値に変換を適用

##### 使い方

    .transformPreference(キー名(PreferenceKey.Type) = PreferenceKey.self) {
        設定値の処理
    }

    .transformPreference(キー名(PreferenceKey.Type) = K.self, 設定値の処理((inout PreferenceKey.Value) -> Void))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .transformPreference(hoge.self, {$0.left = hoge.size})

#### anchorPreference

##### 意味

##### 使い方

    .anchorPreference(key: キー名(PreferenceKey.Type) = PreferenceKey.self, value: 値(Anchor<A>.Source) {
        アンカー処理
    }

    .anchorPreference(key: キー名(PreferenceKey.Type) = PreferenceKey.self, value: 値(Anchor<A>.Source), transform: アンカー処理)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .anchorPreference(key: hoge.self, value: .bounds) { anchor in
            // 処理
        }

#### transformAnchorPreference

##### 意味

##### 使い方

    .transformAnchorPreference(key: キー名(PreferenceKey.Type) = PreferenceKey.self, value: 値(Anchor<A>.Source)) {
        アンカー処理
    }

    .transformAnchorPreference(key: キー名(PreferenceKey.Type) = PreferenceKey.self, value: 値(Anchor<A>.Source), transform: アンカー処理)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .transformAnchorPreference(key: ItemPreferenceKey.self, value: .bottomTrailing) {
            // 処理
        }

#### onPreferenceChange

##### 意味

指定された設定キーの値が変更されたときに実行するアクションを追加

##### 使い方

    .onPreferenceChange(キー名(PreferenceKey.Type) = PreferenceKey.self) {
        実行するアクション
    }

    .onPreferenceChange(キー名(PreferenceKey.Type) = PreferenceKey.self, perform: 実行するアクション)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .onPreferenceChange(hoge.self) { prefs in
           // アクション
        }

#### backgroundPreferenceValue

##### 意味

ビューから指定された設定値を使用して別のビューを最初のビューの背景として作成

##### 使い方

    .backgroundPreferenceValue(キー名(PreferenceKey.Type) = PreferenceKey.self) {
        設定値
    }

    .backgroundPreferenceValue(キー名(PreferenceKey.Type) = PreferenceKey.self, 設定値(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .backgroundPreferenceValue(hoge.self) { preference -> hoge<AnyView> in
            // ビュー
        }

#### overlayPreferenceValue

##### 意味

ビューから指定された設定値を使用して別のビューを最初のビューの上にオーバーレイとして作成

##### 使い方

    .overlayPreferenceValue(キー名(PreferenceKey.Type) = PreferenceKey.self) {
        設定値
    }

    .overlayPreferenceValue(キー名(PreferenceKey.Type) = PreferenceKey.self, 設定値(View))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .overlayPreferenceValue(AnchorKey.self, { anchor in
            // ビュー
        }

#### environment

##### 意味

指定されたキーパスの環境値を指定された値に設定

##### 使い方

    .environment(キーパスの環境値(WritableKeyPath<EnvironmentValues, V>), 値)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .environment(\.truncationMode, .head)

#### environmentObject

##### 意味

用品ビューsubhierachyにObservableObject

##### 使い方

    .environmentObject(下位階層で使用できるようにするオブジェクト(ObservableObject))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .environmentObject(appSettings)

#### transformEnvironment

##### 意味

指定された関数を使用して指定されたキーパスの環境値を変換

##### 使い方

    .transformEnvironment(キーパスの環境値(WritableKeyPath<EnvironmentValues, V>)) {
        変更値
    }

    .transformEnvironment(キーパスの環境値(WritableKeyPath<EnvironmentValues, V>), transform: 変更値)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .transformEnvironment(\.hoge) {r in
            r = hoge
        }

#### previewDevice

##### 意味

プレビューに使用するデバイスを設定

##### 使い方

    .previewDevice(デバイス名(PreviewDevice))

    .previewDevice()

##### PreviewDeviceの使い方

| 名前                                                                                 | 説明                     |
| ---------------------------------------------------------------------------------- | ---------------------- |
| PreviewDevice(extendedGraphemeClusterLiteral value: Self.StringLiteralType)        | 与えられた値で初期化されたインスタンスを作成 |
| PreviewDevice(unicodeScalarLiteral value: Self.ExtendedGraphemeClusterLiteralType) | 与えられた値で初期化されたインスタンスを作成 |
| PreviewDevice(stringLiteral: String)                                               | 与えられた値で初期化されたインスタンスを作成 |
| PreviewDevice(rawValue: String)                                                    | 与えられた値で初期化されたインスタンスを作成 |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .previewDevice(PreviewDevice(rawValue: "iPhone 12 Pro"))

#### previewDisplayName

##### 意味

エディターに表示されるユーザーに表示される名前を提供

##### 使い方

    .previewDisplayName("表示名")

    .previewDisplayName()

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .previewDisplayName("iPhone 13")

#### previewLayout

##### 意味

プレビューレイアウトのサイズを設定

##### 使い方

    .previewLayout(プレビューレイアウトのサイズ(PreviewLayout))

##### PreviewLayoutの使い方

| 名前                                      | 説明                     |
| --------------------------------------- | ---------------------- |
| .device                                 | プレビューを中央に表示            |
| .fixed(width: CGFloat, height: CGFloat) | 固定サイズのコンテナでプレビューを中央に表示 |
| .sizeThatFits                           | コンテナをプレビューのサイズに合わせる    |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .previewLayout(.fixed(width: 10, height: 20))

#### previewContext

##### 意味

プレビュー用のコンテキストを宣言

##### 使い方

    .previewContext(プレビュー用のコンテキスト(PreviewContext) = nil)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .previewContext(hogePreviewContext(family: .systemSmall))

#### modifier

##### 意味

修飾子をビューに適用

##### 使い方

    .modifier(修飾子)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .modifier(BorderedCaption())

#### path

##### 意味

パスを描画

##### 使い方

    .path(in: 基準となるフレーム(CGRect))

##### CGRectの使い方

| 名前                                                              | 説明                        |
| --------------------------------------------------------------- | ------------------------- |
| .infinite                                                       | 無限の広がりを持つ四角形              |
| .null                                                           | 無効な値を表すNULLの長方形           |
| .zero                                                           | 原点とサイズがともに0である長方形         |
| CGRect(origin: CGPoint, size: CGSize)                           | 指定された原点とサイズの矩形を作成         |
| CGRect(x: Double, y: Double, width: Double, height: Double)     | 座標と寸法を浮動小数点値で指定した矩形を作成    |
| CGRect(x: Int, y: Int, width: Int, height: Int)                 | 座標と寸法を整数値で指定した矩形を作成       |
| CGRect(x: CGFloat, y: CGFloat, width: CGFloat, height: CGFloat) | 座標と寸法をCGFloatの値で指定した矩形を作成 |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .path(in: .zero)

#### trim

##### 意味

パスとしての表現に基づいた小数の量でトリミング

##### 使い方

    .trim(from: 開始位置(CGFloat) = 0, to: 終了位置(CGFloat) = 1)

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .trim()

#### transform

##### 意味

アフィン変換を適用

##### 使い方

    .transform(アフィン変換行列(CGAffineTransform))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .transform(CGAffineTransform())

#### size

##### 意味

サイズのある長方形からパスを作成

##### 使い方

    .size(サイズ(CGSize))

    .size(width: 幅(CGFloat), height: 高さ(CGFloat))

##### CGSizeの使い方

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .size(CGSize())

#### scale

##### 意味

バウンディングフレームを変更することなくこの図形をスケーリング

##### 使い方

    .scale(サイズ変更に使用される乗算係数(CGFloat), anchor: 開始位置(UnitPoint) = .center)

    .scale(x: X軸(CGFloat) = 1, y: Y軸(CGFloat) = 1, anchor: 開始位置(UnitPoint) = .center)

##### UnitPointの使い方

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

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())

#### rotation

##### 意味

アンカーポイントを中心に指定した角度で図形を回転

##### 使い方

    .rotation(角度(Angle), anchor: 開始位置(UnitPoint) = .center)

##### Angleの使い方

| 名前               | 説明      |
| ---------------- | ------- |
| .degrees(Double) | 度を指定    |
| .radians(Double) | ラジアンを指定 |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())

#### offset

##### 意味

指定されたサイズでこの図形の相対的な位置を変更

##### 使い方

    .offset(オフセット値(CGSize))

    .offset(オフセット値(CGPoint))

    .offset(x: X軸(CGFloat) = 0, y: Y軸(CGFloat) = 0)

##### CGSizeの使い方

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .offset()

#### stroke

##### 意味

輪郭を色やグラデーションで描画

##### 使い方

    .stroke(描画方法を指定(ShapeStyle), lineWidth: 幅(CGFloat) = 1)

    .stroke(描画方法を指定(ShapeStyle), style: スタイル(StrokeStyle))

    .stroke(lineWidth: 幅(CGFloat) = 1)

    .stroke(style: スタイル(StrokeStyle))

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .stroke(Color.purple, lineWidth: 5)

#### fill

##### 意味

色やグラデーションで塗りつぶす

##### 使い方

    .fill(描画方法を指定(ShapeStyle), style: スタイル(FillStyle) = FillStyle())

    .fill(style: スタイル(FillStyle) = FillStyle())

##### 例

    TransformedShape(shape: Circle(), transform: CGAffineTransform())
        .fill()

### 参考サイト

<https://developer.apple.com/documentation/swiftui/transformedshape>

---
layout: page
---

### 説明

ビュー階層を介して伝達される環境値のコレクション

### 使い方

    EnvironmentValues()

### 例

#### 基本的な使い方

    private struct MyEnvironmentKey: EnvironmentKey {
        static let defaultValue: String = "Default value"
    }
    extension EnvironmentValues {
        var myCustomValue: String {
            get { self[MyEnvironmentKey.self] }
            set { self[MyEnvironmentKey.self] = newValue }
        }
    }
    extension View {
        func myCustomValue(_ myCustomValue: String) -> some View {
            environment(\.myCustomValue, myCustomValue)
        }
    }

### 宣言

    struct EnvironmentValues

### プロパティ

| 名前                                     | 型                         | 説明                                 |
| -------------------------------------- | ------------------------- | ---------------------------------- |
| accessibilityDifferentiateWithoutColor | Bool                      | アクセシビリティカラーが有効か                    |
| accessibilityEnabled                   | Bool                      | アクセシビリティが有効か                       |
| accessibilityInvertColors              | Bool                      | アクセシビリティ(色の反転)が有効か                 |
| accessibilityReduceMotion              | Bool                      | アクセシビリティ(視差効果)が有効か                 |
| accessibilityReduceTransparency        | Bool                      | アクセシビリティ(透明度を減らす)が有効か              |
| accessibilityShowButtonShapes          | Bool                      | アクセシビリティ(ボタンシェイプ)が有効か              |
| legibilityWeight                       | LegibilityWeight?         | テキストに適用するフォントの太さ                   |
| colorScheme                            | ColorScheme               | 配色                                 |
| colorSchemeContrast                    | ColorSchemeContrast       | 配色に伴うコントラスト                        |
| controlSize                            | ControlSize               | コントロールに適用するサイズ                     |
| controlActiveState                     | ControlActiveState        | コントロールのアクティブな状態                    |
| managedObjectContext                   | NSManagedObjectContext    | 管理対象オブジェクト                         |
| defaultMinListHeaderHeight             | CGFloat?                  | ヘッダーのデフォルトの最小高さ                    |
| defaultMinListRowHeight                | CGFloat                   | 行のデフォルトの最小高さ                       |
| allowsTightening                       | Bool                      | 文字間の間隔を狭めるかどうか                     |
| layoutDirection                        | LayoutDirection           | レイアウトの方向                           |
| lineLimit                              | Int?                      | 最大行数                               |
| lineSpacing                            | CGFloat                   | テキストの行間隔                           |
| minimumScaleFactor                     | CGFloat                   | 最小許容比率                             |
| multilineTextAlignment                 | TextAlignment             | 複数行のテキスト配置                         |
| sizeCategory                           | ContentSizeCategory       | コンテンツの好ましいサイズ                      |
| truncationMode                         | Text.TruncationMode       | レイアウトがテキストの最終行をどのように切り詰めるかを示す値     |
| disableAutocorrection                  | Bool?                     | 自動補正が有効か                           |
| textCase                               | Text.Case?                | 表示時にTextのケースを変換するスタイルのオーバーライド      |
| font                                   | Font?                     | デフォルトフォント                          |
| defaultWheelPickerItemHeight           | CGFloat                   | 日付ピッカーなどのホイールスタイルのピッカーの項目のデフォルトの高さ |
| calendar                               | Calendar                  | ビューが日付を扱う際に使用する現在のカレンダー            |
| editMode                               | Binding&lt;EditMode&gt;?        | 編集モード                              |
| isEnabled                              | Bool                      | この環境に関連付けられているビューが操作可能か            |
| locale                                 | Locale                    | ビューが使用する現在のロケール                    |
| presentationMode                       | Binding&lt;PresentationMode&gt; | プレゼンテーションモードで表示されているか              |
| timeZone                               | TimeZone                  | ビューが日付を扱う際に使用する現在のタイムゾーンを指定        |
| redactionReasons                       | RedactionReasons          | ビュー階層に適用されているリダクションの理由             |
| horizontalSizeClass                    | UserInterfaceSizeClass?   | この環境の水平方向のサイズクラス                   |
| verticalSizeClass                      | UserInterfaceSizeClass?   | この環境の垂直方向のサイズクラス                   |
| undoManager                            | UndoManager?              | ビューのアンドゥ操作を登録するためのアンドゥマネージャー       |
| scenePhase                             | ScenePhase                | シーンの現在のフェーズ                        |
| openURL                                | OpenURLAction             | 適切なシステムサービスを使用してURLを開く             |
| isFocused                              | Bool                      | フォーカス可能な最も近い祖先がフォーカスを持っているかどうか     |
| resetFocus                             | ResetFocusAction          | フォーカスシステムにデフォルトフォーカスの再評価を要求するアクション |
| widgetFamily                           | WidgetFamily              | ウィジェットのテンプレート（小、中、大）               |
| displayScale                           | CGFloat                   | ディスプレイの種類                          |
| imageScale                             | Image.Scale               | この環境の画像スケール                        |
| pixelLength                            | CGFloat                   | 画面上の1ピクセルの大きさ                      |
| description                            | String                    | 環境値インスタンスの内容を表す文字列                 |

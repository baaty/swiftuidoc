---
layout: page
---

### 説明

ビュー階層を介して伝達される環境値のコレクション

### 使い方

    EnvironmentValues()
        .メソッド

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

| 名前                                     | 型                         | 説明                                          |
| -------------------------------------- | ------------------------- | ------------------------------------------- |
| accessibilityDifferentiateWithoutColor | Bool                      | システム環境設定の「Differentiate without Color」が有効か  |
| accessibilityEnabled                   | Bool                      | ユーザーが支援技術を有効にしているかどうかを示すブール値                |
| accessibilityInvertColors              | Bool                      | システム環境設定の「色の反転」を有効にするか                      |
| accessibilityReduceMotion              | Bool                      | Reduce Motionのシステム環境設定が有効か                  |
| accessibilityReduceTransparency        | Bool                      | 透過性を減らすというシステム環境設定が有効か                      |
| accessibilityShowButtonShapes          | Bool                      | システム環境設定「Show Button Shapes」が有効であるか         |
| legibilityWeight                       | LegibilityWeight?         | テキストに適用するフォントの太さを指定                         |
| colorScheme                            | ColorScheme               | 配色                                          |
| colorSchemeContrast                    | ColorSchemeContrast       | 配色に伴うコントラスト                                 |
| controlSize                            | ControlSize               | コントロールに適用するサイズ                              |
| controlActiveState                     | ControlActiveState        | コントロールのアクティブな状態                             |
| managedObjectContext                   | NSManagedObjectContext    | managedObject                               |
| defaultMinListHeaderHeight             | CGFloat?                  | ヘッダーのデフォルトの最小高さ                             |
| defaultMinListRowHeight                | CGFloat                   | 行のデフォルトの最小高さ                                |
| allowsTightening                       | Bool                      | 文字間の間隔を狭めるかどうか                              |
| layoutDirection                        | LayoutDirection           | レイアウトの方向性                                   |
| lineLimit                              | Int?                      | 最大行数                                        |
| lineSpacing                            | CGFloat                   | ある線分の下端から次の線分の上端までの距離をポイント                  |
| minimumScaleFactor                     | CGFloat                   | 最小許容比率                                      |
| multilineTextAlignment                 | TextAlignment             | テキストインスタンスがどのように行を揃えるかを示す値                  |
| sizeCategory                           | ContentSizeCategory       | コンテンツの好ましいサイズ                               |
| truncationMode                         | Text.TruncationMode       | レイアウトがテキストの最終行をどのように切り詰めるかを示す値              |
| disableAutocorrection                  | Bool?                     | 自動補正が有効になっているか                              |
| textCase                               | Text.Case?                | 表示時にTextのケースを変換するスタイルのオーバーライド               |
| font                                   | Font?                     | デフォルトフォント                                   |
| defaultWheelPickerItemHeight           | CGFloat                   | 日付ピッカーなどのホイールスタイルのピッカーの項目のデフォルトの高さ          |
| calendar                               | Calendar                  | ビューが日付を扱う際に使用する現在のカレンダー                     |
| editMode                               | Binding<EditMode>?        | この環境に関連付けられているビューの内容をユーザーが編集できるかどうかを示すモード   |
| isEnabled                              | Bool                      | この環境に関連付けられているビューがユーザーとの対話を可能にするかどうかを示すブール値 |
| locale                                 | Locale                    | ビューが使用すべき現在のロケール                            |
| presentationMode                       | Binding<PresentationMode> | この環境に関連付けられたビューの現在のプレゼンテーションモードへのバインディング    |
| timeZone                               | TimeZone                  | ビューが日付を扱う際に使用する現在のタイムゾーンを指定                 |
| redactionReasons                       | RedactionReasons          | ビュー階層に適用されているリダクションの理由                      |
| horizontalSizeClass                    | UserInterfaceSizeClass?   | この環境の水平方向のサイズクラス                            |
| verticalSizeClass                      | UserInterfaceSizeClass?   | この環境の垂直方向のサイズクラス                            |
| undoManager                            | UndoManager?              | ビューのアンドゥ操作を登録するためのアンドゥマネージャー                |
| scenePhase                             | ScenePhase                | シーンの現在のフェーズ                                 |
| openURL                                | OpenURLAction             | 適切なシステムサービスを使用してURLを開く                      |
| isFocused                              | Bool                      | フォーカス可能な最も近い祖先がフォーカスを持っているかどうか              |
| resetFocus                             | ResetFocusAction          | フォーカスシステムにデフォルトフォーカスの再評価を要求するアクション          |
| widgetFamily                           | WidgetFamily              | ウィジェットのテンプレート（小、中、大）                        |
| displayScale                           | CGFloat                   | この環境の表示規模                                   |
| imageScale                             | Image.Scale               | この環境のイメージスケール                               |
| pixelLength                            | CGFloat                   | 画面上の1ピクセルの大きさ                               |
| description                            | String                    | 環境値インスタンスの内容を表す文字列                          |

### 参考サイト

<https://developer.apple.com/documentation/swiftui/environmentvalues>

---
layout: page
---

### 説明

日付ピッカーを表示して日時を選択

### 使い方

#### 境界のない範囲で日付を選択するインスタンスを作成

    DatePicker(ローカライズされた文字列キー(LocalizedStringKey), selection: $表示されている日付の値を選択(Binding<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date])

    DatePicker(selection: $表示されている日付の値を選択(Binding<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date]) {
        日付の使用方法を説明するビュー(Label)
    }

    DatePicker(selection: $表示されている日付の値を選択(Binding<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date], label: 日付の使用方法を説明するビュー)

#### 指定された範囲のDateを選択するインスタンスを作成

    DatePicker(タイトル(StringProtocol), selection: $表示されている日付の値を選択(Binding<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date])    

#### 閉じた範囲の日付を選択するインスタンスを作成

    DatePicker(タイトル(StringProtocol), selection: $表示されている日付の値を選択(Binding<Date>), in: 選択可能な日付に含まれる範囲(ClosedRange<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date])

    DatePicker(ローカライズされた文字列キー(LocalizedStringKey), selection: $表示されている日付の値を選択(Binding<Date>), in: 選択可能な日付に含まれる範囲(ClosedRange<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date])

    DatePicker(selection: $表示されている日付の値を選択(Binding<Date>), in: 選択可能な日付に含まれる範囲(ClosedRange<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date]) {
        日付の使用方法を説明するビュー(Label)
    }

#### 終了日以前の日付を選択するインスタンスを作成

    DatePicker(selection: $表示されている日付の値を選択(Binding<Date>), in: 選択可能な日付に含まれる範囲(ClosedRange<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date], label: 日付の使用方法を説明するビュー)

    DatePicker(ローカライズされた文字列キー(LocalizedStringKey), selection: $表示されている日付の値を選択(Binding<Date>), in: 選択可能な終了日の前のオープン範囲(PartialRangeThrough<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date])

#### 開始日以降の日付を選択するインスタンスを作成

    DatePicker(タイトル(StringProtocol), selection: $表示されている日付の値を選択(Binding<Date>), in: 選択可能な終了日の前のオープン範囲(PartialRangeThrough<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date])

    DatePicker(selection: $表示されている日付の値を選択(Binding<Date>), in: 開始日を選択(PartialRangeFrom<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date]) {
        日付の使用方法を説明するビュー(Label)
    }

    DatePicker(selection: $表示されている日付の値を選択(Binding<Date>), in: 開始日を選択(PartialRangeFrom<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date], label: 日付の使用方法を説明するビュー)

#### 終了日以前の日付を選択するインスタンスを作成

    DatePicker(selection: $表示されている日付の値を選択(Binding<Date>), in: 選択可能な終了日の前のオープン範囲(PartialRangeThrough<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date]) {
        日付の使用方法を説明するビュー(Label)
    }

    DatePicker(selection: $表示されている日付の値を選択(Binding<Date>), in: 選択可能な終了日の前のオープン範囲(PartialRangeThrough<Date>), displayedComponents: 表示および編集できる日付コンポーネント(DatePicker<Label>.Components) = [.hourAndMinute, .date], label: 日付の使用方法を説明するビュー)

### 引数の使い方

#### Date

| 名前                                                    | 説明                                             |
| ----------------------------------------------------- | ---------------------------------------------- |
| .date                                                 | 年、月、日の表示                                       |
| .hourAndMinute                                        | 分、時間の表示                                        |
| Date()                                                | 現在の日付と時刻で初期化された日付の値を作成                         |
| Date(timeIntervalSinceNow: TimeInterval)              | 現在の日付と時刻から指定された秒数だけ相対的に初期化された日付値を作成            |
| Date(timeInterval: TimeInterval, since date: Date)    | 指定された別の日付から指定された秒数だけ相対的に初期化された日付値を作成           |
| Date(timeIntervalSinceReferenceDate ti: TimeInterval) | 2001年1月1日のUTC 00:00:00を基準に指定された秒数で初期化された日付値を作成 |
| Date(timeIntervalSince1970: TimeInterval)             | 1970年1月1日のUTC 00:00:00を基準に指定された秒数で初期化された日付値を作成 |

### 例

#### 基本的な使い方

    @State private var date = Date()
    var body: some View {
        DatePicker(
            "日付を選択",
            selection: $date
        )
    }

#### スタイルの変更

    @State private var date = Date()
    var body: some View {
        DatePicker(
            "日付を選択",
            selection: $date
        )
            .datePickerStyle(.stepperField)
    }

#### 日付のみ変更

    @State private var date = Date()
    var body: some View {
        DatePicker(
            "日付を選択",
            selection: $date,
            displayedComponents: [.date]
        )
            .datePickerStyle(.stepperField)
    }

### 宣言

    struct DatePicker<Label> where Label : View

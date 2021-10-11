---
layout: page
---

### 説明

ビューコンテンツをグループ化

### 使い方

    Group {
        コンテンツ(Content)
    }

    Group(content: コンテンツ)

### 例

#### 基本的な使い方

    Group {
        // コンテンツ
    }

### 宣言

    @frozen struct Group&lt;Content&gt;

### メソッド

| 名前                    | 説明                       |
| --------------------- | ------------------------ |
| commands              | シーンにコマンドを追加              |
| defaultAppStorage     | AppStorageが使用するデフォルトのストア |
| handlesExternalEvents | 使用できるかどうかを示すModifier     |
| onChange              | 変化したときに実行するアクション         |
| windowStyle           | ウィンドウのスタイルを設定            |
| windowToolbarStyle    | ツールバーのスタイルを設定            |

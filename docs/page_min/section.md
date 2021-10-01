---
layout: page
---

### 説明

リストに階層を追加するために使用できるコンテナビュー

### 使い方

#### 指定されたセクションの内容でセクションを作成

    Section {
        コンテンツ
    }

    Section(content: コンテンツ)

#### フッターと指定されたセクション・コンテンツを持つセクションを作成

    Section(footer: フッター(Footer)) {
        コンテンツ
    }

    Section(footer: フッター(Footer), content: コンテンツ)

#### ヘッダーと指定されたセクション・コンテンツを持つセクションを作成

    Section(header: ヘッダー(Parent)) {
        コンテンツ
    }

    Section(header: ヘッダー(Parent), content: コンテンツ)

#### ヘッダーやフッターおよび指定されたセクション・コンテンツを持つセクションを作成

    Section(header: ヘッダー(Parent), footer: フッター(Footer)) {
        コンテンツ
    }

    Section(header: ヘッダー(Parent), footer: フッター(Footer), content: コンテンツ)

### 例

#### 基本的な使い方

    Section {}

### 宣言

    struct Section<Parent, Content, Footer>

### プロパティ

| 名前           | 型         | 説明    |
| ------------ | --------- | ----- |
| internalBody | some View | 内部ボディ |

### メソッド

| 名前          | 説明                            |
| ----------- | ----------------------------- |
| collapsible | ユーザーがセクションを折りたたむことができるかどうかを設定 |

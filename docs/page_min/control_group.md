---
layout: page
---

### 説明

視覚的に似ているビューをまとめるコンテナビュー

### 使い方

#### 子ビューを持つ新しいコントロールグループを作成

    ControlGroup {
        子ビュー(Content)
    }

    ControlGroup(content: 子ビュー(() -> Content))

#### スタイル設定に基づいてコントロールグループを作成

    ControlGroup {
        スタイル設定(ControlGroupStyleConfiguration)
    }

    ControlGroup(スタイル設定(ControlGroupStyleConfiguration))

### 例

#### 基本的な使い方

    ControlGroup {
        Button("Hello")
        Button("World")
    }

### 宣言

    struct ActionSheet

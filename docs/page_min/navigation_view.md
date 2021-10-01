---
layout: page
---

### 説明

ナビゲーションの画面遷移を管理するためのコンテナビュー

### 使い方

    NavigationView {
        コンテンツ
    }

    NavigationView(content: コンテンツ)

### 例

#### 基本的な使い方

    NavigationView {            
        Text("Hello World")
    }

#### ナビゲーションタイトル

    NavigationView {
        VStack {
            Text("Hello World")
        }
            .navigationTitle("ナビゲーションタイトル")
    }

#### ナビゲーションバーを非表示

    NavigationView {
        VStack {
            Text("Hello World")
        }
            .navigationBarHidden(isHidden)
    }

#### ナビゲーションバーにアイテムを追加

    NavigationView {
        VStack {
            Text("Hello World")
        }
            .toolbar {
                ToolbarItem {
                    Text("アイテム")
                }
            }
    }

### 宣言

    struct NavigationView<Content> where Content : View

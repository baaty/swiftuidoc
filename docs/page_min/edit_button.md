---
layout: page
---
### 説明

編集モードを切り替えるボタン

### 使い方

    EditButton()

### 例

#### 基本的な使い方

    @State private var fruits = [
        "Apple",
        "Banana",
        "Papaya",
        "Mango"
    ]
    var body: some View {
        NavigationView{
            List {
                ForEach(
                    fruits,
                    id: \.self
                ) { fruit in
                    Text(fruit)
                }
                .onDelete { self.deleteFruit(at :$0) }
                .onMove { self.moveFruit(from: $0, to: $1) }
            }
            .navigationTitle("Fruits")
            .toolbar { EditButton() }
        }
    }

### 宣言

    struct EditButton

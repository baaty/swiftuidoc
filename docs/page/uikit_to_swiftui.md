---
layout: page
---

### 説明

UIKitからSwiftUIへの置き換え

### Controller

| UIKit                      | SwiftUI             |
| -------------------------- | ------------------- |
| UIViewController           | View                |
| UITableViewController      | List                |
| UICollectionViewController | LazyVGridとLazyHGrid |
| UISplitViewController      | NavigationView      |
| UINavigationController     | NavigationView      |
| UIPageViewController       | TabView             |
| UITabBarController         | TabView             |
| UISearchController         | なし                  |
| UIImagePickerController    | なし                  |
| UIVideoEditorController    | なし                  |
| UIActivityViewController   | なし                  |
| UIAlertController          | Alert               |

### view

| UIKit                   | SwiftUI                                     |
| ----------------------- | ------------------------------------------- |
| UILabel                 | Text, Label                                 |
| UITabBar                | TabView                                     |
| UITabBarItem            | TabView                                     |
| UITextField             | TextField                                   |
| UITextView              | TextEditor                                  |
| UITableView             | List                                        |
| UINavigationBar         | NavigationView                              |
| UINavigationItem        | ToolbarItem                                 |
| UIBarButtonItem         | NavigationView                              |
| UICollectionView        | LazyVGridとLazyHGrid                         |
| UIStackView             | HStack, LazyHStack                          |
| UIStackView             | VStack, LazyVStack                          |
| UIScrollView            | ScrollView                                  |
| UIActivityIndicatorView | ProgressView with CircularProgressViewStyle |
| UIImageView             | Image                                       |
| UIPickerView            | Picker                                      |
| UIButton                | Button, Link                                |
| UIDatePicker            | DatePicker                                  |
| UIPageControl           | なし                                          |
| UIProgressView          | ProgressView                                |
| UISegmentedControl      | Picker                                      |
| UISlider                | Slider                                      |
| UIStepper               | Stepper                                     |
| UISwitch                | Toggle                                      |
| UIToolBar               | NavigationView with .toolbar                |
| MKMapView               | Map                                         |

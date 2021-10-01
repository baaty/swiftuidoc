---
layout: page
---

### 説明

再利用可能なアクションを作成

### 宣言

    @frozen struct Animation

### プロパティ

| 名前                  | 型         | 説明                  |
| ------------------- | --------- | ------------------- |
| Animation.default   | Animation | デフォルト               |
| Animation.easeIn    | Animation | 徐々に加速               |
| Animation.easeInOut | Animation | 加速してから減速            |
| Animation.easeOut   | Animation | 徐々に減速               |
| Animation.linear    | Animation | 等速で変化               |
| customMirror        | Mirror    | インスタンスのカスタムミラー      |
| debugDescription    | String    | デバック用のインスタンスのテキスト表現 |
| description         | String    | インスタンスのテキスト表現       |

### メソッド

| 名前                            | 説明                    |
| ----------------------------- | --------------------- |
| Animation.easeIn              | 徐々に加速                 |
| Animation.easeInOut           | 加速してから減速              |
| Animation.easeOut             | 徐々に減速                 |
| Animation.interactiveSpring   | インタラクティブなスプリングアニメーション |
| Animation.interpolatingSpring | 補間スプリングアニメーション        |
| Animation.linear              | 等速で変化                 |
| Animation.spring              | スプリングアニメーション          |
| Animation.timingCurve         | タイミング曲線               |

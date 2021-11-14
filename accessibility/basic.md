# アクセシビリティとは

[アクセシビリティとは？](https://developer.mozilla.org/ja/docs/Learn/Accessibility/What_is_accessibility)から学ぶ

たとえば、以下のような人々のように能力や環境にかかわらず、同じ機会を与えること。

- ハンディキャップを持つ人のため
- モバイルデバイスや遅いネットワークを利用してる人のため

## メリット

- セマンティクスを守ることでSEOにも効果がある
- 公的イメージが良くなる
  - 倫理、モラルに遵守することになるため

### 法律的な側面

法律では努力目標とされている
- [(総務省)みんなの公共サイト 運用ガイドライン 2016年度版](https://www.soumu.go.jp/main_content/000439213.pdf#page=32)

### どんな配慮がある

- スクリーンリーダー
  - MacだとVoice Overというアプリがある(Command + F5で起動する。と思う)
- 拡大鏡(ズーム機能)
- タブキーによるアクセスコントロール
  - tabindex属性というやつ
- 一貫性のあるレイアウト
  - 一貫性がないことがストレスになる人もいる

このあたりは色々ガイドラインや参考がある。MDNだといかにまとまっている

[アクセシビリティのガイドラインと法律](https://developer.mozilla.org/ja/docs/Learn/Accessibility/What_is_accessibility#accessibility_guidelines_and_the_law)

例) 
- [Cognitive accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Cognitive_accessibility)
- [Web Content Accessibility Guidelines (WCAG) Overview](https://www.w3.org/WAI/standards-guidelines/wcag/)
- [Cognitive and Learning Disabilities Accessibility Task Force (Coga TF) of the AG WG and APA WG](https://www.w3.org/WAI/GL/task-forces/coga/)

### アクセシビリティを実装する

100%対応することは難しいが、早期から対応しておくことを検討した方が良い。

- プロジェクト早期から対応することで、手元を減らす
  - あとから対応する方が大変になる
- アクセシビリティは障害向けの対応ではなく、全てのユーザーを想定していることを留意する
  - ネットワークが遅かったり、モバイルデバイスに対応することはアクセシビリティの対応として適している

### API

アクセシビリティAPIが各OS毎で用意されている。これらは、JSやCSSの情報は含まず、HTMLとしてのセマンティクスの情報を利用する傾向にある

- Windows: Microsoft Active Accessibility（MSAA） / IAccessible、UIAExpress、IAccessible2
- Mac OS X: NSAccessibility
- Linux: AT-SPI
- Android: Accessibility framework
- iOS: UIAccessibility

詳細は[Accessible Rich Internet Applications (WAI-ARIA) 1.1](https://www.w3.org/TR/wai-aria/)にまとまっている。

# WAI-ARIAの基本

[WAI-ARIAの基本](https://developer.mozilla.org/ja/docs/Learn/Accessibility/WAI-ARIA_basics)から学ぶ

## 基本

ブラウザーや支援技術が認識出来るように新しいセマンティクスを追加する仕組み

- ロール(Role)
  - HTML5構造要素を追加する(以下、例)
  - `role="navigation"`, `role="banner"`, `role="tab"`
  - ロールの一覧は[こちら](https://www.w3.org/TR/wai-aria-1.1/#role_definitions)で確認出来る
- プロパティ(Property)
  - 要素の性質を定義する
  - `area-required="true"`, `area-labelledby="hoge"`
- ステート(State)
  - 要素の現在の状態を定義する
  - `area-disabled="true"`

### WAI-ARIAのサポート状況

WAI-ARIAがサポートされているかどうかを確認するのは以下の理由でとても大変

- WAI-ARIAそのものの機能が大量にある
- OS、ブラウザー、スクリーンリーダーの組み合わせが大量にあり、対応しているかの確認が大変

### いつ使うべきか

基本的には必要な時だけ使いのが良い。必要な時の判断は以下例がある

- role属性を使用してHTMLとしてのセマンティクスを追加する場合
- 動的なコンテンツを更新する場合
  - aria-liveを使うとコンテンツに更新があった場合にスクリーンリーダーにそれを伝えることが出来る
- セマンティクスがない要素に対して意味論を追加する場合
  - 例えばdivにaria-requiredを追加する

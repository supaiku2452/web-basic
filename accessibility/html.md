# アクセシビリティの基礎

[HTML: アクセシビリティの基礎](https://developer.mozilla.org/ja/docs/Learn/Accessibility/HTML)から学ぶ

アクセシビリティにおいてセマンティクスを意識してHTMLを利用することが大事。

JSやCSSで見た目や処理がとても素晴らしいものが出来るかもしれないが、デフォルトで用意されている機能はそもそもアクセシビリティがよく無駄なマークアップをする必要がない状態になっている。

例えば、`<button>`はEnterキーで押下出来たり、button同士をタブキーで移動出来る。これ以外にも以下の利点がある

- 開発しやすい
  - デフォルトで十分な機能が用意されている
- モバイル対応
  - デフォルトでもある程度対応されているため、ファイルサイズを小さく保てる
- SEOにも良い
  - セマンティクスを遵守したページはキーワードの重みが適切につけられるためページが目につきやすくなる(上位にいきやすくなる)

## テキストコンテンツ

a11y-good-semantics-example.htmlをVoiceOverで読んでもらうと分かるが、Webページの内容が結構すんなり入ってくる。

a11y-bad-semantics-example.htmlをVoiceOverで読んでもらうとページをだらだらと読み上げるだけど、文章の区切り(見出しやリストといった意味のあるもの)が分からない

また、CSSやJSを使う時もセレクターによる区別がつけられないため開発効率も良くない。

### 明確な言葉

俗語や不必要な専門用語は聞き手を惑わしてしまうため、一般的な言葉を使うのが良い。他にも以下注意点がある

- 範囲を示すときには、**5から7**と記載する。**5 - 7**と書かない
- 略語は展開する
  - **Jan**ではなく、**January**と書く
- 頭文字を取るような省略は、最初にフルで書いた後に後から略語を適用する
  - **Hypertext Markup LanguageすなわちHTML**と書く

### もう少し長いサンプル
- [良いサンプル: good-semantics](https://mdn.github.io/learning-area/accessibility/html/good-semantics.html)はこちら
- [悪いサンプル: bad-semantics](https://mdn.github.io/learning-area/accessibility/html/bad-semantics.html)はこちら

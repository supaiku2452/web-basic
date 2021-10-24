# HTML基礎

[HTML の基本](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/HTML_basics)から学ぶ

## 基本
- opening tag
  - `<p>`
- closing tag
  - `</p>`
- content
  - 要素の内容
- element
  - 上記3つのまとまりを指す

![構成説明図](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-small.png)
_参照元: [MDN Web Docs - HTML要素の中身](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/HTML_basics#anatomy_of_an_html_element)_

## 空要素
`<img>`のようなやつは空要素と呼ぶ。タグ内に要素がないため

```html
<img src="images/firefox-icon.png" alt="My test image">
```

## 画像

`alt`属性には画像の説明を入れる。目の不自由な人は画面リーダーを使っておりそれがaltを読むため。

## 見出し

`h1` ~ `h6`まで見出しがある。見出しには暗黙のスタイルがあるが、テキストを大きくする、太くすると言った装飾の用途では使わない。

見出しは、アクセシビリティとSEOなどで利用されているため、正しいレベルで使用すること

- 参考
  - [Chromeのデフォルトスタイル](https://chromium.googlesource.com/chromium/blink/+/refs/heads/main/Source/core/css/html.css)
  - [その他ブラウザ](https://coliss.com/articles/build-websites/operation/css/user-agent-stylesheets.html)

## リスト
- ul
  - Unordered lists
- ol
  - ordered lists
- li
  - list items

- 参考
  - [w3.org - 10 Lists](https://www.w3.org/TR/html4/struct/lists.html#h-10.2)

## リンク

- `href`
  - hypertext reference

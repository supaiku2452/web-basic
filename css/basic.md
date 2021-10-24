# CSS基礎

[CSS の基本](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/CSS_basics)から学ぶ

CSSはスタイルシート言語であり、マークアップ言語ではない。

## 基本構造

- selector
  - HTMLの要素名
- declaration
  - `color:red;`のような単一宣言
- property
  - `color`といった装飾したいもの
- property value
  - `red`といった装飾内容

![CSSの基本構造](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics/css-declaration-small.png)
_参照元: [MDN Web Docs CSS - 規則セットの構造](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/CSS_basics)_

セレクターは複数指定可能

```css
p, li, h1, .special {
  color: red;
}
```

## セレクター

- 要素セレクター
  - `p {...}`
- IDセレクター
  - `#id {...}`
- クラスセレクター
  - `.class-name {...}`
- 属性セレクター
  - `img[src] {...}`
  - 指定された属性を持つものが対象
  - 属性の値まで指定することが可能
    - `img[src="xxxx"] {...}`
- 疑似クラスセレクター
  - `a:hover {...}`
  - 指定された要素が指定された状態にあるものが対象
- 疑似要素セレクター
  - `p::first-line {...}`
  - 要素の特定部分が対象
  - p要素で最初に現れた最初の行が対象
- 子結合子
  - `article > p {...}`
  - 要素に対する子コンビネーター`>`によって指定されたものが対象
- 子孫結合子
  - `article  p {...}`
  - 指定された子要素が指定された孫要素を含むものが対象
- 隣接兄弟結合子
  - `h1 + p {...}`
  - 同じ親要素を持ち、1つ目の要素の直後に2つ目の要素があるものが対象
- 一般兄弟結合子
  - `h1 ~ p {...}`
  - 同じ親要素を持ち、1つ目の要素の後に2つ目の要素があるものが対象

- 参考
  - [CSS セレクター](https://developer.mozilla.org/ja/docs/Learn/CSS/Building_blocks/Selectors)


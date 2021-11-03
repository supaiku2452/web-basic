# 画像

[HTML の画像](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)から学ぶ

## 基礎

imageの置き場所は、SEO的に `<img src="images/<image-file>" >` がいいらしい。また、ファイル名も意味が分かるものが良い。

### 代替テキスト

`alt`属性は画像が見えない・表示されない状況で使用するためにある。内容は、画像に対する説明が適切。

代替テキストが必要な理由

- スクリーンリーダーで読まれる
- パスが間違っている場合に、何が表示使用しているか分かる

altに何を書くべきか

- 基本は画像に対する説明
- CSSによる装飾(背景など)に使う場合は、`alt=""`とする
  - この場合はaltは余計な情報となる(背景の情報が欲しい人はいない)
- 画像がコンテンツに取って重要な要素を持つときは、altに説明を書くのではなく、要素として説明を入れるのが良い
  - もしaltに説明を入れると２重になってしまう

### 幅と高さ

`width`と`height`を使って指定する。画像が読み込まれない場合は、表示されるスペースが残るが問題ない。レイアウトも崩れないし、CLS的にもいい？

画像サイズを変更する必要がある場合はCSSを使う。width/height変える前提だと、画像が適切な状態でダウンロードされない可能性がある

### 画像タイトル

`title`属性だが、アクセシビリティ上問題があるので使わない方が良い。

### キャプション

画像に対するキャプションがある場合は、`<figure>`と`<figcaption>`を使うと良い

before

```html

<div class="figure">
    <img src="image-path"
         alt="description"
         width="100"
         height="100">
    <p>ここにキャプションを表示する</p>
</div>
```

after

```html

<figure>
    <img src="image-path"
         alt="description"
         width="100"
         height="100">
    <figcaption>ここにキャプションを表示する</figcaption>
</figure>
```

アクセシビリティの観点として、キャプションは画像が見える人に向けたメッセージであるが、代替テキストは画像が欠けた場合を対象にしている。なので、altとfigcaptionで同じことは言わない方が良い。

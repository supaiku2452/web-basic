# meta

[head には何が入る? HTML のメタデータ](https://developer.mozilla.org/ja/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)から学ぶ

## 基本

### 文字コード

基本は`utf-8`を指定する

```html

<meta charset="utf-8">
```

### metaとSEO

`author`と`description`属性は指定した方が良い

- author
  - Webページの作成者を指す
- description
  - Webページの説明を指す
  - Googleで検索したときのページタイトル以下に説明は表示される。SEO的にはあった方がいいので基本的には指定した方が良い

![Web アクティブラーニング:検索エンジンにおける description の扱い](https://mdn.mozillademos.org/files/16074/mdn-search-result.png)
_参照元: MDN Web Docs [Web アクティブラーニング:検索エンジンにおける description の扱い](https://developer.mozilla.org/ja/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#active_learning_the_descriptions_use_in_search_engines)_

なお、`keyword`はSEOに関係しないので必要なものだけ定義しておくとよい

### Open Graph Data

Facebookが開発したメタデータプロトコル([OGP](https://ogp.me/))。グラフという表現はよく分からない

FacebookやTwitterなどでページをリンクしたときに、指定した画像やタイトル、説明が良い感じで表示される

以下、OGP関連の属性を設定した時のイメージ

```html

<meta property="og:image" content="https://developer.mozilla.org/static/img/opengraph-logo.png">
<meta property="og:description" content="The Mozilla Developer Network (MDN) provides
information about Open Web technologies including HTML, CSS, and APIs for both Web sites
and HTML5 Apps. It also documents Mozilla products, like Firefox OS.">
<meta property="og:title" content="Mozilla Developer Network">
```

_引用元: MDN Web Docs [メタデータの他の種類](https://developer.mozilla.org/ja/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#other_types_of_metadata )_

![Facebookリンク共有イメージ](https://mdn.mozillademos.org/files/12349/facebook-output.png)
_参照元: MDN Web Docs [メタデータの他の種類](https://developer.mozilla.org/ja/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#other_types_of_metadata )_

- データタイプ
  - Basic Metadata
    - og:title - The title of your object as it should appear within the graph, e.g., "The Rock".
    - og:type - The type of your object, e.g., "video.movie". Depending on the type you specify, other properties may
      also be required.
    - og:image - An image URL which should represent your object within the graph.
    - og:url - The canonical URL of your object that will be used as its permanent ID in the graph,
      e.g., "https://www.imdb.com/title/tt0117500/".
  - Optional Metadata
    - og:audio - A URL to an audio file to accompany this object.
    - og:description - A one to two sentence description of your object.
    - og:determiner - The word that appears before this object's title in a sentence. An enum of (a, an, the, "", auto).
      If auto is chosen, the consumer of your data should chose between "a" or "an". Default is "" (blank).
    - og:locale - The locale these tags are marked up in. Of the format language_TERRITORY. Default is en_US.
    - og:locale:alternate - An array of other locales this page is available in.
    - og:site_name - If your object is part of a larger web site, the name which should be displayed for the overall
      site. e.g., "IMDb".
    - og:video - A URL to a video file that complements this object.
  
 _引用元: The Open Graph protocol [Basic Metadata, Optional Metadata](https://ogp.me/#metadata)_

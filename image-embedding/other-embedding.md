# その他埋め込み

[object から iframe へ — その他の埋め込み技術](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies)から学ぶ

## 基礎

iframeを利用するときは、`src`属性の設定をJavaScriptでやるのが良いらしい。本体のページコンテンツの描画をブロックすることがないので、SEO的にもよい(多分、First Contentful Paintのこと)

### セキュリティ上の懸念

iframeはクリックジャギングによく使われる。

X-Frame-Options

常に`sandbox`属性を使用する。用途に合った制限をかけるべき。


# hyperlink

[ハイパーリンクの作成](https://developer.mozilla.org/ja/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)から学ぶ

## 基礎

`<a>`の`title`属性は、リンクにホバーした時にツールチップが表示される。titleに重要な情報を表示する場合は、キーボードベースでアクセスする人はこの情報に到達できないため、コンテンツとして表した方が良い。

### ドキュメントフラグ

HTML文書の特定部分にリンクすることも可能。これを実現したい場合は、対象要素に`id`属性を付与する必要がある。

-　ページ内リンクの場合は、`<a href="#example">link<a/>`
-　ページ外リンクの場合は、`<a href="hoge.html#example">link<a/>`

### ベストプラクティス

- サーチエンジンはリンクテキストを使用してターゲットファイルにインデックスをつけるので、リンクにはキーワードを含めた方が良い(説明的が良い)。
  - 例えば、 `click here` のリンクだと訳がわからん
- リンク名に、`~~リンク`のようにリンクを含めるのは冗長。スクリーンリーダーはリンクであれば、リンクと読んでくれる。
- リンクラベルは端的である方が良い

### 相対リンク

できるだけ相対リンクを使う。絶対リンクの場合は、ブラウザがドメインを解釈するところから始めるので効率が悪い

### HTML以外のリンク

リンクによりさまざまなアクションを起こすことができるが、ユーザーはそれをリンクを見ただけで判断することはできない。そのため、リンクを押したら何が起こるか、わかりやすくしておくのが良い。

```html
<p><a href="http://www.example.com/large-report.pdf">
  Download the sales report (PDF, 10MB)
</a></p>

<p><a href="http://www.example.com/video-stream/" target="_blank">
  Watch the video (stream opens in separate tab, HD quality)
</a></p>

<p><a href="http://www.example.com/car-game">
  Play the car game (requires Flash)
</a></p>
```

_参照元: [MDN Web Docs - ハイパーリンクの作成](https://developer.mozilla.org/ja/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#linking_to_non-html_resources_%E2%80%94_leave_clear_signposts)_

### downloadリンク

download属性をダウンロード時のデフォルトダウンロード名にすることができる

### メールリンク

クリックした際にメールの新規メッセージを開きたい場合は、`mailto:`スキーマを利用する

```html
<a href="mailto:nowhere@mozilla.org">メールをどこにも送信しません</a>
```
_参照元: [MDN Web Docs - ハイパーリンクの作成](https://developer.mozilla.org/ja/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#e-mail_links)_



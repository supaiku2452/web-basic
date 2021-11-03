# 動画と音声

[動画と音声のコンテンツ](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)から学ぶ

## video要素

`<video>`は、`src`と`controls`の属性がある

- src
  - 動画のパス
- controls
  - 動画や音声の再生を制御する
  - てんかんを患っている人にとって重要らしい

videoタグ内の段落は、代替コンテンツと呼ばれる。ページにアクセスしているブラウザが古い時に表示される

### 複数フォーマット

複数のフォーマットをサポートする場合は、`source`要素を複数定義する

```html
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>お使いのブラウザは HTML5 動画をサポートしていません。その代わりに<a href="rabbit320.mp4">動画へのリンク</a>があります。</p>
</video>
```

_引用元: MDN Web Docs [複数のフォーマットをサポートする](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content#supporting_multiple_formats)_

### その他機能

使いそうなものだけ

- poster
  - 動画が再生される前に表示される画像のURLを指定する
- preload
  - 大きなファイルをバッファリングする要素
    - none: バッファリングしない
    - auto: メディアファイルをバッファリングする
    - metadata: メタデータだけバッファリングする

## audio要素

基本はvideo同じだが、ビデオプレイヤーよりも使用する領域が小さい

### テキストトラック

以下理由によりテキストトラックが好まれる

- 聴覚障害が動画を理解するため
  - 音声が聞こえないので
- 騒がしい場所でも動画を理解出来る
- 動画のネイティブでない人も理解出来る

`WebTT`フォーマットと`<track>`がそれに対応している

動画に対してテキストファイルを書くための形式。いつテキストデータを表示するかといった情報はメタデータに含まれる

- 字幕(subtitles): 音声を理解出来ない人向け(母国語ではない)
- キャプション: 音声を聞くことが出来ない人に何が起こっているか伝える

vttを置く場合はこんなイメージ。

```html
<video controls>
    <source src="example.mp4" type="video/mp4">
    <source src="example.webm" type="video/webm">
    <track kind="subtitles" src="subtitles_en.vtt" srclang="en">
</video>
```

_引用元: MDN Web Docs [動画のテキストトラックを表示する](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content#displaying_video_text_tracks)_

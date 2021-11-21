# アクセシブルマルチメディア

[アクセシブルマルチメディア](https://developer.mozilla.org/ja/docs/Learn/Accessibility/Multimedia)から学ぶ

## 基本

audio/videoにcontrolsを設定すると、コントロールパネルが出てくるが何個か問題がある

```html
<audio controls>
  <source src="viper.mp3" type="audio/mp3">
  <source src="viper.ogg" type="audio/ogg">
  <p>Your browser doesn't support HTML5 audio. Here is a <a href="viper.mp3">link to the audio</a> instead.</p>
</audio>

<br>

<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```

- キーボードアクセスが出来ない
  - コントロール間のタブ移動が出来ない
- ブラウザー間でスタイルと機能が異なる

これらはJSを使ってコントロールを自作する必要がある。参考は[こちら](https://github.com/mdn/learning-area/tree/master/accessibility/multimedia/custom-controls-OOJS)

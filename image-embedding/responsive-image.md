# レスポンシブ画像

[レスポンシブ画像](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)から学ぶ

## 基本

コンテンツのサイズに合わせた画像が欲しい時に、一つの画像だけだとそれに対応出来ない。また、モバイル対応となると一つの画像で対応しようとすると、どうしてもモバイルに適した画像かPCに適した画像かのどちらかを取らなくてはならない。

レスポンシブ画像に対応する場合は、以下のようになる

```html
<img srcset="elva-fairy-320w.jpg 320w,
             elva-fairy-480w.jpg 480w,
             elva-fairy-800w.jpg 800w"
     sizes="(max-width: 320px) 280px,
            (max-width: 480px) 440px,
            800px"
     src="elva-fairy-800w.jpg" alt="妖精の衣装を着たエルバ">
```

_引用元: [レスポンシブ画像の作り方](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images#how_do_you_create_responsive_images)_

上記のように定義すると、メディア条件に該当した時に指定の画像を取得しにいく。これであれば、viewportに合わせた画像を取りに行くので無駄にダウンロードすることもない。

```html
<img srcset="elva-fairy-320w.jpg,
             elva-fairy-480w.jpg 1.5x,
             elva-fairy-640w.jpg 2x"
     src="elva-fairy-640w.jpg" alt="妖精の衣装を着たエルバ">
```

上記のように、解像度を変えることも出来る

また、pictureを使って複数のresourceを宣言することも出来る

```html
<picture>
  <source media="(max-width: 799px)" srcset="elva-480w-close-portrait.jpg">
  <source media="(min-width: 800px)" srcset="elva-800w.jpg">
  <img src="elva-800w.jpg" alt="クリスは立って彼の娘エルバを保持します">
</picture>
```

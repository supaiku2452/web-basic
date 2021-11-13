# 基礎

[HTML の表の基本](https://developer.mozilla.org/ja/docs/Learn/HTML/Tables/Basics)から学ぶ

## 基本

テーブル(表)を表現するものであり、テーブルレイアウトを表現するものではない。

- アクセシビリティを低下させる
- レスポンスな対応が難しくなる
  - レイアウトはコンテンツによって決まるが、本来のセマンティクスのある要素(header/sectionなど)とは異なる

### `<th>` テーブルヘッダー

表の見出しとして利用する。デフォルトCSSとしてスタイルがあたるので、tdを使うより良い。`scope`属性を使うとより便利らしい

### 列への共通のスタイル付け

列全体へのスタイル設定は、`<col>`要素と`<colgroup>`要素で実現出来る。

```html
<table>
    <colgroup>
        <col style="background-color: red; font-weight: bold">
        <col style="background-color: yellow">
    </colgroup>
    <tr>
        <th>Data 1</th>
        <th>Data 2</th>
    </tr>
</table>
```






---
title: テンプレート
---

# テンプレート

Middleman は HTML の開発を簡単にするためにたくさんのテンプレート言語への
アクセスを提供します。テンプレート言語はページ内で変数やループを使えるように
するシンプルなものから, ページを HTML に変換するまったく異なったフォーマットを
提供するものにまで及びます。 Middleman は ERB, Haml, Sass, SCSS や CoffeeScript
のサポートを搭載しています。Tilt が有効な gem であればその他にも多くのエンジンが
有効化できます ([リスト参照][see the list])。

## テンプレートの基礎

デフォルトのテンプレート言語は ERB です。ERB は変数の追加,
メソッド呼び出し, ループの使用や if 文を除き, そのままの HTML です。
このガイドの次のセクションでは使用例として ERB を使います。

Middleman で使うテンプレートはそのファイル名にテンプレート言語の拡張子を
含みます。ERB で書かれたシンプルな index ページはファイル名の
`index.html` と ERB の拡張子を含む `index.html.erb` という名前に
なります。

まず, このファイルには単純な HTML が書かれています:

```html
<h1>ようこそ</h1>
```

思いつきでループを追加することができます:

```erb
<h1>ようこそ</h1>
<ul>
  <% 5.times do |num| %>
    <li>カウント <%= num %></li>
  <% end %>
</ul>
```

  [see the list]: /jp/advanced/template-engine-options/

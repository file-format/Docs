{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","rhtml ファイル", "rhtml ファイル形式", "rhtml ファイルの種類", "ファイル", "種類", "rhtml ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML ページ",
  "description":"RHTML ファイル形式と,RHTML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## .RHTML オプション番号

拡張子が .rhtml のファイルは、Ruby コードまたはスクリプトを含むサーバー側の [HTML](/web/html/) ファイルです。コードは、バックエンドで実行されている Ruby on Rails を使用してサーバー上で実行されます。 Ruby on Rails を知らない人のために説明すると、これは Model-View-Control パターンに基づくバックエンド データベースを備えた Web アプリケーションを開発するためのフルスタック フレームワークです。簡単に言うと、RHTML は HTML と Ruby を組み合わせたものであり、HTML タグを使用する Web 開発者が Ruby スクリプト/プログラミングの機能を利用できるようになっています。

## RHTML ファイル形式

RHTML ファイルは、他のテキストベースの Web ファイルと同様に、プレーン テキスト形式で記述されます。実行するコードは `<% %>` で囲み、出力の場合は `<%= %>` ステートメントでコードを記述します。

## RHTML の例

次の例では、HTML と Ruby on Rails の最も単純な組み合わせを使用して、製品リストから各製品の名前を出力します。
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## 参考文献

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


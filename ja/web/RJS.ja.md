{
  "date" : "2021-05-24",
  "keywords" :["rjs", "ファイル", "拡張子", "ファイル形式", "ファイル拡張子", "RJS", "Ruby Javascriptファイル"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript ファイル",
  "description":"RJS ファイル形式とは何か,および RJS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## .RJS オプション番号

拡張子が .rjs のファイルは、Rails 開発者が Ruby を使用して動的な JavaScript コードを作成できるようにする Ruby コードと JavasScript の組み合わせです。 Ruby コードは Java 関数に埋め込まれ、Ruby エンジンがサーバー上で実行されている必要がある Web サーバー上でコンパイルされます。 RJS は [RHTML](/web/rhtml/) に似ています。唯一の違いは、ラテラルには [HTML](/web/html/) に Ruby コードが含まれているのに対し、Javascript 関数に Ruby コードが含まれていることです。

## RJS ファイル形式

RJS ファイルは、他のスクリプト言語やプログラミング言語と同様にプレーン テキストでコーディングされます。このようなページがクライアントから要求されると、Ruby コードがサーバーで実行され、HTML と Javascript コードのみがクライアントのブラウザーに返されます。 RJS ファイルの構文は、Ruby と JavaScript の構文を組み合わせた構文に似ており、Ruby コードのみが JavaScript 関数に埋め込まれています。

### RJS の例

次の例は、単純な Ruby コードを個別に示してから、JavaScript 関数に埋め込みます。

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
以下はRubyJSです：
```Ruby
# here you go!

foo = -> { "bar" }
```
## 参考文献

* [RJS](https://github.com/makevoid/rjs)


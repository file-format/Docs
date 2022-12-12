{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml", "rhtml fájl", "rhtml fájlformátum", "rhtml fájltípus", "fájl", "típus", "mi az rhtml fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML oldal",
  "description":"További információ az RHTML fájlformátumról és az RHTML-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Mi az RHTML fájl?

Az .rhtml kiterjesztésű fájl egy szerveroldali [HTML](/hu/web/html/) fájl, amely Ruby-kódot vagy szkripteket tartalmaz. A kód végrehajtása a szerveren a háttérben futó Ruby on Rails segítségével történik. Azok számára, akik nem ismerik a Ruby on Rails-t, ez egy full-stack keretrendszer a Model-View-Control mintán alapuló háttéradatbázisokkal rendelkező webalkalmazások fejlesztéséhez. Egyszerűen fogalmazva, az RHTML a HTML és a Ruby kombinációja, ahol a Ruby szkriptelés/programozás ereje elérhető a webfejlesztők számára HTML-címkéket használva.

## RHTML fájlformátum

Az RHTML fájlok egyszerű szöveges formátumban vannak írva, mint bármely más szövegalapú webfájl. A végrehajtandó kód a `<% %>` közé van zárva, míg a kimenetnél a kód a `<%= %>` utasítások közé kerül.

## RHTML példa

A következő példa a HTML és a Ruby on Rails legegyszerűbb kombinációját használja az egyes termékek nevének a terméklistából történő kimenetére.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Hivatkozások

* [TutorialsPoint – Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


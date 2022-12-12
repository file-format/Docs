{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml", "soubor rhtml", "formát souboru rhtml", "typ souboru rhtml", "soubor", "typ", "co je soubor rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML Page",
  "description":"Další informace o formátu souborů RHTML a rozhraních API, která mohou vytvářet a otevírat soubory RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Co je soubor RHTML?

Soubor s příponou .rhtml je soubor [HTML](/cs/web/html/) na straně serveru, který obsahuje kód nebo skripty Ruby. Kód je spuštěn na serveru pomocí Ruby on Rails běžícího na backendu. Pro ty, kteří o Ruby on Rails nevědí, je to full-stack framework pro vývoj webových aplikací s backendovými databázemi založenými na vzoru Model-View-Control. Jednoduše řečeno, RHTML je kombinací HTML a Ruby, kde je síla skriptování/programování Ruby dostupná webovým vývojářům pomocí HTML tagů.

## Formát souboru RHTML

Soubory RHTML jsou psány ve formátu prostého textu jako jakékoli jiné textové webové soubory. Kód, který se má provést, je uzavřen v `<% %>`, zatímco pro výstup je kód zapsán uvnitř příkazů `<%= %>`.

## Příklad RHTML

Následující příklad používá nejjednodušší kombinaci HTML a Ruby on Rails k výstupu názvu každého produktu ze seznamu produktů.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Reference

* [TutorialsPoint – Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


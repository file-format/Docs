{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","rhtml-fil", "rhtml-filformat", "rhtml-filtyp", "fil", "typ", "vad är en rhtml-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML-sida",
  "description":"Läs mer om RHTML-filformat och API:er som kan skapa och öppna RHTML-filer.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Vad är en RHTML-fil?

En fil med tillägget .rhtml är en [HTML](/sv/web/html/)-fil på serversidan som innehåller Ruby-kod eller skript. Koden exekveras på servern med hjälp av Ruby on Rails som körs i backend. För de som inte känner till Ruby on Rails är det ett ramverk i full stack för att utveckla webbapplikationer med backend-databaser baserade på Model-View-Control-mönstret. Enkelt sagt är RHTML en kombination av HTML och Ruby där kraften i Ruby-skript/programmering är tillgänglig för webbutvecklare som använder HTML-taggar.

## RHTML filformat

RHTML-filer skrivs i vanligt textformat som alla andra textbaserade webbfiler. Koden som ska köras är innesluten i `<% %>` medan för utdata skrivs koden inuti `<%= %>`-satser.

## Exempel på RHTML

Följande exempel använder den enklaste kombinationen av HTML och Ruby on Rails för att mata ut namnet på varje produkt från en produktlista.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Referenser

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


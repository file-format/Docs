{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","rhtml-Datei", "rhtml-Dateiformat", "rhtml-Dateityp", "Datei", "Typ", "was ist eine rhtml-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby-HTML-Seite",
  "description":"Erfahren Sie mehr über das RHTML-Dateiformat und APIs, die RHTML-Dateien erstellen und öffnen können.",
  "linktitle" :"RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Was ist eine RHTML-Datei?

Eine Datei mit der Erweiterung .rhtml ist eine serverseitige [HTML](/de/web/html/)-Datei, die Ruby-Code oder Skripte enthält. Der Code wird auf dem Server ausgeführt, indem Ruby on Rails im Backend ausgeführt wird. Für diejenigen, die Ruby on Rails nicht kennen, es ist ein Full-Stack-Framework für die Entwicklung von Webanwendungen mit Backend-Datenbanken, die auf dem Model-View-Control-Muster basieren. Einfach gesagt, RHTML ist eine Kombination aus HTML und Ruby, bei der Webentwickler mithilfe von HTML-Tags die Leistungsfähigkeit von Ruby-Skripting/-Programmierung nutzen können.

## RHTML-Dateiformat

RHTML-Dateien werden wie alle anderen textbasierten Webdateien im Nur-Text-Format geschrieben. Der auszuführende Code ist in `<% %>` eingeschlossen, während der Code für die Ausgabe in `<%= %>`-Anweisungen geschrieben wird.

## RHTML-Beispiel

Das folgende Beispiel verwendet die einfachste Kombination aus HTML und Ruby on Rails, um den Namen jedes Produkts aus einer Produktliste auszugeben.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Verweise

* [TutorialsPoint – Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","rhtml file", "rhtml file format", "rhtml file type", "file", "type", "che cos'è un file rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Pagina HTML Ruby",
  "description":"Scopri il formato di file RHTML e le API che possono creare e aprire file RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Che cos'è un file RHTML?

Un file con estensione .rhtml è un file [HTML](/it/web/html/) lato server che contiene codice o script Ruby. Il codice viene eseguito sul server utilizzando Ruby on Rails in esecuzione sul backend. Per coloro che non conoscono Ruby on Rails, è un framework full-stack per lo sviluppo di applicazioni Web con database back-end basati sul modello Model-View-Control. Detto semplicemente, RHTML è una combinazione di HTML e Ruby in cui la potenza dello scripting/programmazione di Ruby è disponibile per gli sviluppatori Web che utilizzano tag HTML.

## Formato file RHTML

I file RHTML sono scritti in formato di testo normale come qualsiasi altro file Web basato su testo. Il codice da eseguire è racchiuso tra `<% %>` mentre per l'output, il codice è scritto all'interno di istruzioni `<%= %>`.

## Esempio RHTML

L'esempio seguente utilizza la combinazione più semplice di HTML e Ruby on Rails per generare il nome di ogni prodotto da un elenco di prodotti.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Riferimenti

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


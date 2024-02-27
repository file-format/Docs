{
  "date": "2021-05-24",
  "keywords": [
"rhtml",
"rhtml fil",
"rhtml filformat",
"rhtml filtype",
"fil",
"type",
"hvad er en rhtml-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RHTML - Ruby HTML-side",
  "description": "Lær om RHTML-filformat og API'er, der kan oprette og åbne RHTML-filer.",
  "linktitle": "RHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rhtm-dal"
}
},
  "lastmod": "2021-05-24"
}

## Hvad er en RHTML-fil?

En fil med filtypen .rhtml er en [HTML](/web/html/)-fil på serversiden, der indeholder Ruby-kode eller scripts. Koden udføres på serveren ved hjælp af Ruby on Rails, der kører i backend. For dem, der ikke kender til Ruby on Rails, er det en fuldstackramme til udvikling af webapplikationer med backend-databaser baseret på Model-View-Control-mønsteret. Simpelthen sagt, RHTML er en kombination af HTML og Ruby, hvor kraften i Ruby scripting/programmering er tilgængelig for webudviklere, der bruger HTML-tags.

## RHTML filformat

RHTML-filer er skrevet i almindeligt tekstformat som alle andre tekstbaserede webfiler. Koden, der skal udføres, er indesluttet i `<% %>`, mens koden for output er skrevet inde i `<%= %>`-sætninger.

## RHTML eksempel

Følgende eksempel bruger den enkleste kombination af HTML og Ruby on Rails til at udlæse navnet på hvert produkt fra en produktliste.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Referencer

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)



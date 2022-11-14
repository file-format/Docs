{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","rhtml-bestand", "rhtml-bestandsformaat", "rhtml-bestandstype", "bestand", "type", "wat is een rhtml-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML-pagina",
  "description":"Meer informatie over de RHTML-bestandsindeling en API's die RHTML-bestanden kunnen maken en openen.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Wat is een RHTML-bestand?

Een bestand met de extensie .rhtml is een server-side [HTML](/nl/web/html/)-bestand dat Ruby-code of scripts bevat. De code wordt uitgevoerd op de server met behulp van de Ruby on Rails die op de backend draait. Voor degenen die Ruby on Rails niet kennen, het is een full-stack framework voor het ontwikkelen van webapplicaties met backend-databases op basis van het Model-View-Control-patroon. Simpel gezegd, RHTML is een combinatie van HTML en Ruby waarbij de kracht van Ruby scripting/programmering beschikbaar is voor webontwikkelaars die HTML-tags gebruiken.

## RHTML-bestandsindeling

RHTML-bestanden zijn geschreven in platte tekst, net als alle andere op tekst gebaseerde webbestanden. De uit te voeren code is tussen `<% %>` ingesloten, terwijl voor uitvoer de code tussen `<%= %>`-statements wordt geschreven.

## RHTML-voorbeeld

In het volgende voorbeeld wordt de eenvoudigste combinatie van HTML en Ruby on Rails gebruikt om de naam van elk product uit een productenlijst uit te voeren.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Referenties

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


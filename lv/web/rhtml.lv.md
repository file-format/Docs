{
  "date": "2021-05-24",
  "keywords": [
"rhtml",
"rhtml fails",
"rhtml faila formātā",
"rhtml faila tips",
"failu",
"veids",
"kas ir rhtml fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RHTML — rubīna HTML lapa",
  "description": "Uzziniet par RHTML faila formātu un API, kas var izveidot un atvērt RHTML failus.",
  "linktitle": "RHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rhtm-lvl"
}
},
  "lastmod": "2021-05-24"
}

## Kas ir RHTML fails?

Fails ar paplašinājumu .rhtml ir servera puses [HTML](/web/html/) fails, kas satur Ruby kodu vai skriptus. Kods tiek izpildīts serverī, izmantojot Ruby on Rails, kas darbojas aizmugurē. Tiem, kas nezina par Ruby on Rails, tas ir pilnas kaudzes ietvars tīmekļa lietojumprogrammu izstrādei ar aizmugures datu bāzēm, kuru pamatā ir Model-View-Control modelis. Vienkārši sakot, RHTML ir HTML un Ruby kombinācija, kur tīmekļa izstrādātājiem, izmantojot HTML tagus, ir pieejamas Ruby skriptu/programmēšanas iespējas.

## RHTML faila formāts

RHTML faili ir rakstīti vienkārša teksta formātā, tāpat kā citi teksta tīmekļa faili. Izpildāmais kods ir ietverts `<% %>`, savukārt izvadei kods tiek ierakstīts priekšrakstos `<%= %>`.

## RHTML piemērs

Nākamajā piemērā tiek izmantota vienkāršākā HTML un Ruby on Rails kombinācija, lai izvadītu katra produkta nosaukumu no produktu saraksta.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Atsauces
* [TutorialsPoint — Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

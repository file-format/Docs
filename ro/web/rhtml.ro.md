{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","fișier rhtml", "format fișier rhtml", "tip fișier rhtml", "fișier", "tip", "ce este un fișier rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML – Ruby HTML Page",
  "description":"Aflați despre formatul de fișier RHTML și despre API-urile care pot crea și deschide fișiere RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Ce este un fișier RHTML?

Un fișier cu extensia .rhtml este un fișier [HTML](/ro/web/html/) de partea serverului care conține cod sau scripturi Ruby. Codul este executat pe server folosind Ruby on Rails care rulează la backend. Pentru cei care nu știu despre Ruby on Rails, este un cadru complet pentru dezvoltarea de aplicații web cu baze de date backend bazate pe modelul Model-View-Control. Pur și simplu spus, RHTML este o combinație de HTML și Ruby în care puterea de scriptare/programare Ruby este disponibilă dezvoltatorilor web care folosesc etichete HTML.

## Format de fișier RHTML

Fișierele RHTML sunt scrise în format text simplu, ca orice alte fișiere web bazate pe text. Codul de executat este inclus în `<% %>`, în timp ce pentru ieșire, codul este scris în instrucțiunile `<%= %>`.

## Exemplu RHTML

Următorul exemplu folosește cea mai simplă combinație de HTML și Ruby on Rails pentru a scoate numele fiecărui produs dintr-o listă de produse.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Referințe

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


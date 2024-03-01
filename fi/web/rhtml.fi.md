{
  "date": "2021-05-24",
  "keywords": [
"rhtml",
"rhtml-tiedosto",
"rhtml-tiedostomuoto",
"rhtml-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on rhtml-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RHTML - Ruby HTML -sivu",
  "description": "Opi RHTML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RHTML-tiedostoja.",
  "linktitle": "RHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rhtm-fil"
}
},
  "lastmod": "2021-05-24"
}

## Mikä on RHTML-tiedosto?

Tiedosto, jonka pääte on .rhtml, on palvelinpuolen [HTML](/web/html/)-tiedosto, joka sisältää Ruby-koodia tai komentosarjoja. Koodi suoritetaan palvelimella käyttämällä Ruby on Rails -ohjelmaa, joka on käynnissä taustajärjestelmässä. Niille, jotka eivät tiedä Ruby on Railsista, se on täyden pinon kehys web-sovellusten kehittämiseen taustatietokannoista, jotka perustuvat Model-View-Control -malliin. Yksinkertaisesti sanottuna RHTML on HTML:n ja Rubyn yhdistelmä, jossa Rubyn komentosarjan/ohjelmoinnin teho on HTML-tageja käyttävien web-kehittäjien käytettävissä.

## RHTML-tiedostomuoto

RHTML-tiedostot kirjoitetaan vain tekstimuodossa, kuten muutkin tekstipohjaiset verkkotiedostot. Suoritettava koodi on `<% %>` sisällä, kun taas tulostettaessa koodi kirjoitetaan `<%= %>` -käskyjen sisään.

## RHTML esimerkki

Seuraava esimerkki käyttää yksinkertaisinta HTML- ja Ruby on Rails -yhdistelmää kunkin tuotteen nimen tulostamiseen tuoteluettelosta.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Viitteet

* [TutorialsPoint – Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)



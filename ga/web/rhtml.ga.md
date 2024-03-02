{
  "date": "2021-05-24",
  "keywords": [
"rhtml",
"Comhad rhtml",
"Formáid comhaid rhtml",
"Cineál comhaid rhtml",
"comhad",
"cineál",
"Cad is comhad rhtml ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RHTML - Leathanach HTML Ruby",
  "description": "Foghlaim faoi fhormáid comhaid RHTML agus APIs ar féidir leo comhaid RHTML a chruthú agus a oscailt.",
  "linktitle": "RHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rhtm-gal"
}
},
  "lastmod": "2021-05-24"
}

## Cad is comhad RHTML ann?

Is comhad é comhad a bhfuil iarmhír .rhtml air ná comhad ar thaobh an fhreastalaí {{ HYPERLINK1}} ina bhfuil cód Ruby nó scripteanna. Déantar an cód a fhorghníomhú ar an bhfreastalaí ag baint úsáide as an Ruby on Rails a ritheann ag an inneall. Dóibh siúd nach bhfuil cur amach acu ar Ruby on Rails, is creat lánchruach é chun feidhmchláir ghréasáin a fhorbairt le bunachair shonraí inneall atá bunaithe ar an bpatrún Model-View-Control. Go simplí ráite, is meascán de HTML agus Ruby é RHTML ina bhfuil cumhacht scriptithe/ríomhchláraithe Ruby ar fáil d’fhorbróirí gréasáin ag baint úsáide as clibeanna HTML.

## Formáid Chomhaid RHTML

Scríobhtar comhaid RHTML i bhformáid gnáth-théacs cosúil le haon chomhaid ghréasáin téacs-bhunaithe eile. Tá an cód atá le feidhmiú faoi iamh laistigh de `<% %>` agus le haghaidh aschur, tá an cód scríofa laistigh de ráitis `<%= %>`.

## Sampla RHTML

Úsáideann an sampla seo a leanas an meascán is simplí de HTML agus Ruby on Rails chun ainm gach táirge a aschur ó liosta táirgí.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Tagairtí

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)



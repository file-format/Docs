{
  "date": "2021-05-24",
  "keywords": [
"rhtml",
"rhtml failą",
"rhtml failo formatas",
"rhtml failo tipas",
"failą",
"tipo",
"kas yra rhtml failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RHTML – rubino HTML puslapis",
  "description": "Sužinokite apie RHTML failo formatą ir API, kurios gali kurti ir atidaryti RHTML failus.",
  "linktitle": "RHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rhtm-ltl"
}
},
  "lastmod": "2021-05-24"
}

## Kas yra RHTML failas?

Failas su plėtiniu .rhtml yra serverio pusės [HTML](/web/html/) failas, kuriame yra Ruby kodas arba scenarijai. Kodas vykdomas serveryje naudojant Ruby on Rails, veikiantį užpakalinėje programoje. Tiems, kurie nežino apie Ruby on Rails, tai yra visa sistema, skirta kurti žiniatinklio programas su užpakalinėmis duomenų bazėmis, pagrįstomis modelio peržiūros ir valdymo modeliu. Paprasčiau tariant, RHTML yra HTML ir Ruby derinys, kuriame Ruby scenarijų / programavimo galia yra prieinama žiniatinklio kūrėjams, naudojantiems HTML žymas.

## RHTML failo formatas

RHTML failai rašomi paprasto teksto formatu, kaip ir bet kurie kiti tekstiniai žiniatinklio failai. Kodas, kurį reikia vykdyti, yra įtrauktas į `<% %>`, o išvesties kodas rašomas `<%= %>` sakiniuose.

## RHTML pavyzdys

Šiame pavyzdyje naudojamas paprasčiausias HTML ir Ruby on Rails derinys, kad išvestų kiekvieno produkto pavadinimą iš produktų sąrašo.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Nuorodos

* [TutorialsPoint – Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)



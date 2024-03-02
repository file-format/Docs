{
  "date": "2020-11-11",
  "keywords": [
"DDL",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Comhaid Bunachar Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid DDL agus APIanna ar féidir comhaid DDL a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid DDL - Comhad Teanga um Shainmhíniú Sonraí",
  "linktitle": "DDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dd-gal"
}
},
  "lastmod": "2020-11-11"
}

## Cad is comhad DDL ann?

Comhad le síneadh .ddl is ea comhad Teanga Sainmhíniú Sonraí a úsáidtear chun scéimre an bhunachair shonraí a shainiú. Tá ráitis/orduithe ann chun oibriú le struchtúir bhunachar sonraí mar táblaí, colúin, taifid agus réimsí eile. Scríobhtar orduithe i gcomhad DDL in [SQL](/database/sql/) agus is féidir leo oibríochtaí a dhéanamh ar nós tábla a chruthú sa bhunachar sonraí, scaoil agus nuashonrú. Tá scéimre bunachar sonraí faoi úinéireacht a chruthaithe agus is féidir na hoibríochtaí CRUD ar fad a dhéanamh air. Is iad na feidhmchláir mhóréilimh ar féidir leo comhaid DDL a chruthú agus a oscailt ná Eagarthóir Téacs Windows, Jetbrains Intellij Idea, agus EclipseLink.

## Orduithe DDL

Is féidir roinnt orduithe a bheith i gcomhad DDL amháin a dhéanfaidh, de bharr comhréire a cheartú, a fhorghníomhú in ord agus a dhéanfaidh athruithe ar an scéimre, mar shampla tacair agus táblaí carachtair a chruthú, táblaí a ligean, táblaí a athainmniú agus a athrú. Úsáidtear orduithe DDL a leanúint go coitianta agus iad ag obair le scéimre bunachar sonraí.

`CREATE` - Úsáidtear é chun an bunachar sonraí nó a chuid cuspóirí a chruthú (cosúil le tábla, innéacs, feidhm, radharcanna, nós imeachta stórais agus truicear).

`DROP` - Úsáidtear é chun rudaí a scriosadh ón mbunachar sonraí.

`ALTER` - Úsáidtear é chun struchtúr an bhunachair shonraí a athrú.

`TRUNCATE` - Úsáidtear é chun gach taifead a bhaint de thábla, lena n-áirítear gach spás a leithdháileadh do na taifid a bhaint.

`COMMENT` – Cuireann sé tuairimí leis an bhfoclóir sonraí.

`RENAME` - Athainmnítear réad atá sa bhunachar sonraí cheana féin.

## Sampla DDL

Taispeánann an sampla seo a leanas ráiteas DDL le haghaidh ordú CREATE a chruthaíonn tábla agus a shainíonn a réimsí.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Tagairtí ##

* [DDL le Vicipéid]( https://ga.wikipedia.org/wiki/Data_definition_language)



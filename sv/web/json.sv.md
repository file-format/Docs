---
date: 2019-10-11
keywords: json, .json, json-filformat, hur man öppnar json-filer, javascript-objektnotation, json-dataformat, .json-filformat
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON-filformat - Vad är en JSON-fil?
linktitle: JSON
description: "Lär dig mer om JSON-filformat och API:er som kan skapa och öppna JSON-filer." 
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Vad är en JSON-fil?

JSON (JavaScript Object Notation) är ett öppet standardfilformat för att dela data som använder läsbar text för att lagra och överföra data. JSON-filer lagras med tillägget .json. JSON kräver mindre formatering och är ett bra alternativ för [XML](/sv/web/xml/). JSON härrör från JavaScript men är ett språkoberoende dataformat. Generering och analys av JSON stöds av många moderna programmeringsspråk. *application/json* är mediatypen som används för JSON.

## JSON-filformat - kort historik

Det fanns ett behov av realtidsserver till klientkommunikation som ledde till skapandet av JSON. JSON-formatet specificerades först av Douglas Crockford i mars 2001. JSON baserades på Standard ECMA-262 3rd Edition—december 1999 som är en delmängd av JavaScript.

Den första upplagan av JSON-standarden ECMA-404 publicerades i oktober 2013 av Ecma International. RFC 7159 blev huvudreferensen för JSONs internetanvändningar 2014. I november 2017 publicerades ISO/IEC 21778:2017 som en internationell standard. RFC 8259 publicerades den 13 december 2017 av The Internet Engineering Task Force som är den aktuella versionen av Internet Standard STD 90.

## JSON-filstruktur

JSON-data skrivs i **nyckel/värde**-par. Nyckeln och värdet separeras av ett kolon(:) i mitten med nyckeln till vänster och värdet till höger. Olika nyckel/värdepar separeras med ett kommatecken(,). Nyckeln är en sträng omgiven av dubbla citattecken, till exempel "namn". Värdena kan vara av följande typer.

- `Nummer`
- `String`: Sekvens av Unicode-tecken omgiven av dubbla citattecken.
- 'Boolesk': Sant eller falskt.
- `Array`: En lista med värden omgiven av hakparenteser, till exempel

``` json
[ "Äpple", "Banan", "Apelsin" ]
```

- `Objekt`: En samling nyckel-/värdepar omgivna av t.ex. hängslen

``` json
{"name": "Jack", "age": 30, "favoriteSport" : "Fotboll"}
```

JSON-objekt kan också kapslas för att representera strukturen för data. Nedan ges ett exempel på ett JSON-objekt.

### JSON-formatexempel

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Vad är den maximala storleken på JSON-filen?

Det finns praktiskt taget ingen gräns för den maximala storleken på en JSON-fil. Det kan vara lika långt som det utrymme som innehållet kräver för att lagras.

När det gäller att använda JSON-filformat för att överföra data över internet, måste man vara försiktig med de tillgängliga resurserna på datorn. Om stora JSON-data överförs kommer överföringen att påverkas om klientwebbläsaren har begränsat minne.


Det finns ingen hård gräns definierad av specifikationen, men du måste vara försiktig så att du inte tar ut resurser på dina användares datorer, eftersom det snabbt kommer att försämra deras användarupplevelse och de kommer sannolikt att överge din app.

## JSON vs XML

**XML** är ett annat vanligt och allmänt använt filformat för utbyte av data över internet. När det gäller utbyte av data mellan applikationer har utvecklare möjlighet att använda både XML- och JSON-filformat. JSON antas dock som det bekvämaste sättet för datautbyte mellan applikationer över internet på grund av följande skäl.

1. JSON ger en tydlig och mer lättläst bild av data jämfört med XML-filformat
1. JSON minskar kostnaden för dataöverföring över internet eftersom den har mindre antal tecken för att definiera samma datauppsättning jämfört med XML
1. Moderna programmeringsspråk tillhandahåller inbyggda parsers för att analysera JSON-svaret över webben.

## Visste du?

Du kan bli en bidragsgivare på FileFormat.com för att hålla filformatgemenskapen uppdaterad med dina resultat. Om du måste dela något om JSON- eller webbfilformat kan du lägga upp dina resultat i avsnittet [Web File Format News](https://news.fileformat.com/t/Web) så att folk kan lära sig mer från dessa.

## Referenser

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [En introduktion till JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)


---
date: 2019-10-11
keywords: json, .json, json-bestandsindeling, hoe json-bestanden te openen, javascript-objectnotatie, json-gegevensindeling, .json-bestandsindeling
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON-bestandsindeling - Wat is een JSON-bestand?
linktitle: JSON
description: "Meer informatie over de JSON-bestandsindeling en API's die JSON-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Wat is een JSON-bestand?

JSON (JavaScript Object Notation) is een open standaardbestandsindeling voor het delen van gegevens die door mensen leesbare tekst gebruikt om gegevens op te slaan en te verzenden. JSON-bestanden worden opgeslagen met de .json-extensie. JSON vereist minder opmaak en is een goed alternatief voor [XML](/nl/web/xml/). JSON is afgeleid van JavaScript, maar is een taalonafhankelijk gegevensformaat. Het genereren en parseren van JSON wordt ondersteund door veel moderne programmeertalen. *application/json* is het mediatype dat voor JSON wordt gebruikt.

## JSON-bestandsindeling - korte geschiedenis

Er was behoefte aan realtime server-naar-clientcommunicatie die leidde tot het maken van JSON. Het JSON-formaat werd voor het eerst gespecificeerd door Douglas Crockford in maart 2001. JSON was gebaseerd op Standard ECMA-262 3rd Edition-december 1999, een subset van JavaScript.

De eerste editie van JSON-standaard ECMA-404 werd in oktober 2013 gepubliceerd door Ecma International. RFC 7159 werd de belangrijkste referentie voor JSON's internetgebruik in 2014. In november 2017 werd ISO/IEC 21778:2017 gepubliceerd als een internationale standaard. RFC 8259 werd op 13 december 2017 gepubliceerd door The Internet Engineering Task Force, de huidige versie van de internetstandaard STD 90.

## JSON-bestandsstructuur

JSON-gegevens worden geschreven in **sleutel/waarde**-paren. De sleutel en waarde worden gescheiden door een dubbele punt (:) in het midden met de sleutel aan de linkerkant en de waarde aan de rechterkant. Verschillende sleutel/waarde-paren worden gescheiden door een komma(,). De sleutel is een string omringd door dubbele aanhalingstekens, bijvoorbeeld "naam". De waarden kunnen van de volgende typen zijn.

- 'Nummer'
- `String`: reeks Unicode-tekens tussen dubbele aanhalingstekens.
- `Boolean`: waar of niet waar.
- `Array`: een lijst met waarden tussen vierkante haken, bijvoorbeeld

```json
[ "Appel", "Banaan", "Oranje" ]
```

- `Object`: een verzameling sleutel/waarde-paren omgeven door bijvoorbeeld accolades

```json
{"name": "Jack", "leeftijd": 30, "favorieteSport": "Voetbal"}
```

JSON-objecten kunnen ook worden genest om de structuur van de gegevens weer te geven. Hieronder ziet u een voorbeeld van een JSON-object.

### JSON-formaat voorbeeld

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

## Wat is de maximale grootte van een JSON-bestand?

Er is praktisch geen limiet op de maximale grootte van een JSON-bestand. Het kan zo lang zijn als de ruimte die nodig is om de inhoud op te slaan.

Als het gaat om het gebruik van het JSON-bestandsformaat voor het overbrengen van gegevens via internet, moet men voorzichtig zijn met de beschikbare bronnen van de computer. Als grote JSON-gegevens worden overgedragen, wordt de overdracht beïnvloed als de clientbrowser een beperkt geheugen heeft.


Er is geen harde limiet gedefinieerd door specificatie, maar u moet oppassen dat u de bronnen op de computers van uw gebruikers niet uitput, omdat dit hun gebruikerservaring snel zal verslechteren en ze uw app waarschijnlijk zullen verlaten.

## JSON versus XML

**XML** is een ander veelgebruikt en veelgebruikt bestandsformaat voor de uitwisseling van gegevens via internet. Als het gaat om de uitwisseling van gegevens tussen applicaties, hebben ontwikkelaars de mogelijkheid om zowel XML- als JSON-bestandsindelingen te gebruiken. JSON wordt echter om de volgende redenen gebruikt als de handigste manier voor gegevensuitwisseling tussen applicaties via internet.

1. JSON geeft een duidelijke en gemakkelijker leesbare weergave van gegevens in vergelijking met XML-bestandsindelingen
1. JSON vermindert de overhead van gegevensoverdracht via internet omdat het minder tekens heeft om dezelfde gegevensset te definiëren in vergelijking met XML
1. Moderne programmeertalen bieden ingebouwde parsers om het JSON-antwoord via internet te ontleden.

## Wist je dat?

U kunt een bijdrager worden op FileFormat.com om de gemeenschap voor bestandsindelingen op de hoogte te houden van uw bevindingen. Als u iets wilt delen over JSON- of webbestandsindelingen, kunt u uw bevindingen posten in de sectie [Nieuws over webbestandsindelingen](https://news.fileformat.com/t/Web), zodat mensen hier meer over kunnen leren.

## Referenties

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [Een inleiding tot JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)


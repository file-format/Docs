{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Bestand", "Extensie", "Bestandsindeling", "Bestandsextensie", "RJS", "Ruby Javascript-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript-bestand",
  "description":"Meer informatie over de RJS-bestandsindeling en API's die RJS-bestanden kunnen maken en openen.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Wat is een RJS-bestand?

Een bestand met de extensie .rjs is een combinatie van Ruby-code en JavsScript waarmee Rails-ontwikkelaars Ruby kunnen gebruiken om dynamische JavaScript-code te produceren. Ruby-code is ingebed in Java-functies en wordt gecompileerd op de webserver waarvoor de Ruby-engine op de server moet draaien. RJS lijkt op [RHTML](/nl/web/rhtml/); het enige verschil is dat de lateral Ruby-code bevat in [HTML](/nl/web/html/) terwijl het Ruby-code bevat in Javascript-functies.

## RJS-bestandsindeling

RJS-bestanden zijn gecodeerd in platte tekst zoals elke andere script- of programmeertaal. Wanneer een dergelijke pagina door de klant wordt opgevraagd, wordt de Ruby-code op de server uitgevoerd en worden alleen HTML- en Javascript-code teruggestuurd naar de browser van de klant. De syntaxis van het RJS-bestand is vergelijkbaar met die van een combinatie van Ruby- en JavaScript-syntaxis, zodat alleen de Ruby-code is ingebed in JavaScript-functies.

### RJS Voorbeeld

Het volgende voorbeeld toont een eenvoudige Ruby-code onafhankelijk en vervolgens ingesloten in een JavaScript-functie.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
en het volgende is de RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Referenties

* [RJS](https://github.com/makevoid/rjs)


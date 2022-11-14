{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Bestand maken - Xcode Makefile-scriptbestand",
  "description":"Meer informatie over XCode MakeFile Format en API's die MakeFile-bestanden kunnen maken en openen.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Wat is een MAKE-bestand?

Een MAKE-bestand is een XCode-scriptbestand dat de compilatie van code organiseert. Het wordt gebruikt om programma's uit meerdere broncodebestanden te compileren en te koppelen. Dit helpt bij het bepalen welke delen van een grote applicatie opnieuw moeten worden gecompileerd wanneer de applicatie moet worden bijgewerkt. Laat bestanden een reeks instructies gebruiken om uit te voeren, afhankelijk van welke bestanden zijn gewijzigd.

## Voorbeeld van MAKE-bestandsindeling

De volgende inhoud wordt uitgevoerd met behulp van het hulpprogramma Make en de uitvoer is als volgt.

```
hello:
	echo "hello world"
```
**Uitvoer maken**

```
$ make
echo "hello world"
hello world
```

## Referenties
* [XCode en merk - Apple-forums](https://developer.apple.com/forums/thread/657458)
* [Gids voor Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)


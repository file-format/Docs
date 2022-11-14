{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INC-bestandsextensie - Wat is een INC-bestand?",
  "description":"Meer informatie over INC Inclusief bestandsindeling en API's die INC-bestanden kunnen maken en openen.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Wat is een INC-bestand?

Een INC-bestand is een include-bestand dat door de broncode van het softwareprogramma wordt gebruikt om naar headerinformatie te verwijzen. Het is vergelijkbaar met het [.h-bestandsformaat](/nl/programming/h/) en bevat declaraties, functies, headers of macro's die kunnen worden hergebruikt door broncodebestanden zoals C++. INC-bestanden worden gebruikt door verschillende programmeertalen zoals C, [C++](/nl/programming/cpp/), Pascal, [PHP](/nl/programming/php/) en [Java](/nl/programming/java/). Teksteditors zoals Microsoft Notepad, Notepad++ en TextEdit kunnen worden gebruikt om INC-bestanden te openen.

## INC-bestandsindeling - Meer informatie

Een INC-bestand wordt opgeslagen als platte tekstbestand met alle declaraties opgenomen volgens de declaratiesyntaxis. Eén INC-bestand kan ook verwijzen naar andere INC-bestanden. Eenmaal gemaakt, wordt het INC-bestand onderdeel van het project en kan er vanuit bronbestanden zoals C++ naar worden verwezen. Er kan naar worden verwezen door meerdere bronbestanden om duplicatie te voorkomen.

## INC-bestandsinhoud

INC-bestanden kunnen de volgende informatie bevatten.

**'Variabelen'** - In het geval van Object Oriented Programming (OOP), bevat een klasse-headerbestand definities van alle variabelen op klasseniveau die toegankelijk zijn via de broncodebestanden van de implementatie

**'Methods Declaration'** - Alle methodedeclaraties zijn opgenomen in de .h-headerbestanden om toegankelijk te zijn voor meerdere implementatiebestanden.

**'Niet-inline functiedefinities'** - Headerbestanden kunnen ook definities van niet-inline-methoden bevatten.

## Nadeel van het gebruik van INC-bestanden in PHP

PHP zijn server-side scripts die op de server draaien en de resultaten terugsturen naar de aanroepende webpagina's. Als een PHP-bestand verwijst naar een INC-bestand en de server is niet geconfigureerd om .inc-bestanden te ontleden (wat heel gebruikelijk is), kan een gebruiker de php-broncode in het .inc-bestand bekijken door naar de URL-directory te gaan. Je moet dus voorzichtig zijn bij het gebruik van INC-bestanden als include-bestanden in PHP.

## Referenties

* [INC gebruiken in PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)


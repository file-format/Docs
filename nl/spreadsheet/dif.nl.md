{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "bestand", "extensie", "bestandsformaat", "Data Interchange File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een DIF-bestandsextensie is en API's die DIF-bestanden kunnen maken en openen.",
  "title" :"DIF - Bestandsindeling voor gegevensuitwisseling",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Wat is een DIF-bestand?

DIF staat voor Data Interchange Format dat wordt gebruikt om spreadsheetgegevens tussen verschillende applicaties te importeren/exporteren. Deze omvatten Microsoft Excel, OpenOffice Calc, StarCalc en vele anderen. Het slaat gegevens op in een enkele spreadsheet, wat de enige beperking is van dit bestandsformaat.

## Korte geschiedenis van DIF-bestandsindeling ##

Het DIF-bestandsformaat is begin jaren tachtig ontwikkeld door Software Arts, Inc. De specificaties van het bestandsformaat voor DIF waren opgenomen in VisiCalc, het eerste spreadsheetprogramma voor personal computers. Deze specificaties waren auteursrechtelijk beschermd in 1981 en waren een geregistreerd handelsmerk van Software Arts Products Corp.

## DIF-bestandsindeling ##

DIF slaat spreadsheetinhoud op in ASCII-tekstbestand waarmee het kan worden bekeken en bewerkt met een teksteditor. Het formaat bezit zijn plaats in de lijst met gegevensserialisatieformaten vanwege de kenmerken van gegevensuitwisseling. Een DIF-bestand bestaat uit 2 secties; een koptekst en gegevens.

Alles in DIF wordt vertegenwoordigd door een 2- of 3-regelige chunk. Headers krijgen een brok van 3 regels; gegevens, 2.

* Header-chunks beginnen met een tekstidentificatie die alleen in hoofdletters, alleen alfabetische tekens en minder dan 32 letters bestaat. De volgende regel moet een getallenpaar zijn en de derde regel moet een tekenreeks tussen aanhalingstekens zijn.
* Gegevensbrokken beginnen met een cijferpaar en de volgende regel is een tekenreeks tussen aanhalingstekens of een trefwoord.

### Waarden ###

Een waarde beslaat twee regels, de eerste een paar getallen en de tweede een tekenreeks of een trefwoord. Het eerste cijfer van het paar geeft het type aan:

* −1 – type richtlijn, het tweede getal wordt genegeerd, de volgende regel is een van deze trefwoorden:
** BOT – begin van tuple (begin van rij)
** EOD – einde van gegevens
* 0 – numeriek type, waarde is het tweede getal, de volgende regel is een van deze trefwoorden:
** V – geldig
** N.v.t. – niet beschikbaar
** FOUT – fout
** TRUE – echte booleaanse waarde
** FALSE – valse booleaanse waarde
* 1 – stringtype, het tweede getal wordt genegeerd, de volgende regel is de string tussen dubbele aanhalingstekens

### DIF Header-chunk ###

Het kopgedeelte van een DIF-bestand bestaat uit een id-regel gevolgd door de twee regels van een waarde. De numerieke waarden in header-chunks gebruiken alleen een lege tekenreeks in plaats van de geldigheidssleutelwoorden. De details van deze header-chunks zijn als volgt.

* TABEL - er volgt een numerieke waarde van de versie, de niet meer gebruikte tweede regel van de waarde bevat een generatorcommentaar
* VECTOREN - het aantal kolommen volgt als een numerieke waarde
* TUPLES - het aantal rijen volgt als een numerieke waarde
* DATA - na een dummy 0 numerieke waarde volgen de gegevens voor de tabel, elke rij voorafgegaan door een BOT-waarde, de hele tabel wordt afgesloten met een EOD-waarde

### DIF Voorbeeld ###

Het volgende voorbeeld toont de inhoud van een eenvoudig werkblad en de equivalente DIF-representatie.


|Naam|Leeftijd
---|---|
|Bob|34
|Blad|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Referenties ##

* [ DIF - Door Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)


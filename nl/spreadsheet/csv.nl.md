{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "bestand", "extensie", "bestandsindeling", "Door komma's gescheiden waarden", "Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over CSV-bestandsindelingen en API's die CSV-bestanden kunnen maken en openen.",
  "title" :"CSV-bestandsindeling",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Wat is een CSV-bestand?

Bestanden met de extensie .csv (door komma's gescheiden waarden) vertegenwoordigen platte tekstbestanden die gegevensrecords bevatten met door komma's gescheiden waarden. Elke regel in een CSV-bestand is een nieuw record uit de reeks records in het bestand. Dergelijke bestanden worden gegenereerd wanneer gegevensoverdracht is bedoeld van het ene opslagsysteem naar het andere. Aangezien alle toepassingen records kunnen herkennen, gescheiden door komma's, is het zeer gemakkelijk om dergelijke gegevensbestanden in de database te importeren. Bijna alle spreadsheetprogramma's zoals Microsoft Excel of OpenOffice Calc kunnen CSV zonder veel moeite importeren. Gegevens die uit dergelijke bestanden worden geïmporteerd, worden gerangschikt in cellen van een spreadsheet voor weergave aan de gebruiker.

## Korte geschiedenis ##

Hieronder volgen enkele snelle feiten over de oorsprong en geschiedenis van het CSV-bestandsformaat.

* 1972 - IBM Fortran (level H extended) compiler ondersteunde ze onder OS/360

* 1978 - Lijstgerichte invoer/uitvoer werd ondersteund door FORTRAN 77 dat komma's en spaties gebruikte voor scheidingstekens

* 2005 - CSV is gestandaardiseerd met [RFC4180](https://tools.ietf.org/html/rfc4180) als MIME-inhoudstype.

* 2013 - De tekortkomingen van RFC4180 werden verholpen door een W3C-aanbeveling

* 2015 - W3C maakte de eerste concepten van aanbevelingen voor CSV-metadatastandaarden, die in december 2015 als aanbeveling begonnen

## Converteer CSV-bestanden ##

CSV-bestanden kunnen worden geconverteerd naar verschillende bestandsindelingen met behulp van de toepassingen die deze bestanden kunnen openen. Microsoft Excel kan bijvoorbeeld gegevens importeren uit een CSV-bestandsindeling en deze opslaan in XLS, [XLSX](/nl/spreadsheet/xlsx/), [PDF](/nl/pdf/), [TXT](/nl/tekstverwerking/txt/) , XML en [HTML](/nl/web/html/) bestandsformaten. Evenzo bieden andere desktop- en onlineservices de mogelijkheid om CSV-bestanden te exporteren naar HTML, ODS en [RTF](/nl/word-processing/rtf/).

## CSV-bestandsindeling ##

Het is bekend dat het CSV-bestandsformaat wordt gespecificeerd onder [RFC4180](https://tools.ietf.org/html/rfc4180). Het definieert elk bestand als CSV-compatibel als:

* Elk record bevindt zich op een aparte regel, begrensd door een regeleinde (CRLF). Bijvoorbeeld:
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx CRLF
* Het laatste record in het bestand kan al dan niet een eindregeleinde hebben. Bijvoorbeeld:
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx
* Er kan een optionele kopregel verschijnen als de eerste regel van het bestand met hetzelfde formaat als normale recordregels. Deze header bevat namen die overeenkomen met de velden in het bestand en moet hetzelfde aantal velden bevatten als de records in de rest van het bestand (de aan- of afwezigheid van de headerregel moet worden aangegeven via de optionele "header"-parameter van dit Mime type). Bijvoorbeeld:
* veldnaam,veldnaam,veldnaam CRLF
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿Binnen de kop en elk record kunnen er een of meer velden zijn, gescheiden door komma's. Elke regel moet hetzelfde aantal velden in het hele bestand bevatten. Spaties worden beschouwd als onderdeel van een veld en mogen niet worden genegeerd. Het laatste veld in het record mag niet worden gevolgd door een komma. Bijvoorbeeld:
* aaa, bbb, ccc
* Elk veld kan al dan niet tussen dubbele aanhalingstekens staan (sommige programma's, zoals Microsoft Excel, gebruiken echter helemaal geen dubbele aanhalingstekens). Als velden niet tussen dubbele aanhalingstekens staan, mogen er geen dubbele aanhalingstekens in de velden verschijnen. Bijvoorbeeld:\
* "aaa", "bbb", "ccc" CRLF
* zzz,yyy,xxx
* Velden met regeleinden (CRLF), dubbele aanhalingstekens en komma's moeten tussen dubbele aanhalingstekens worden geplaatst. Bijvoorbeeld:
* "aaa", "b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* Als dubbele aanhalingstekens worden gebruikt om velden te omsluiten, dan moet een dubbel aanhalingsteken dat in een veld verschijnt, worden ontsnapt door er een ander dubbel aanhalingsteken voor te plaatsen. Bijvoorbeeld:
* "aaa", "b""bb", "ccc"

In het licht van modern gebruik is het scheidingsteken echter niet beperkt tot alleen komma's en kan het ook puntkomma's, tabs of spaties zijn. Toepassingen zoals Microsoft Excel bieden de mogelijkheid om het scheidingsteken op te geven voor het importeren van records uit een CSV-bestand.

## Referenties

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)


{
  "date": "2019-12-10",
  "keywords": [
"CSV",
"fil",
"udvidelse",
"filformat",
"Kommaseparerede værdier",
"Regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om CSV-filformat og API'er, der kan oprette og åbne CSV-filer.",
  "title": "CSV filformat",
  "linktitle": "CSV",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-cs-dav"
}
},
  "lastmod": "2019-12-10"
}

## Hvad er en CSV-fil?

Filer med filtypenavnet .csv (Comma Separated Values) repræsenterer almindelige tekstfiler, der indeholder registreringer af data med kommaseparerede værdier. Hver linje i en CSV-fil er en ny post fra det sæt af poster, der er indeholdt i filen. Sådanne filer genereres, når dataoverførsel er tilsigtet fra et lagersystem til et andet. Da alle applikationer kan genkende poster adskilt med komma, er import af sådanne datafiler til databasen gjort meget bekvemt. Næsten alle regnearksapplikationer som Microsoft Excel eller OpenOffice Calc kan importere CSV uden stor indsats. Data importeret fra sådanne filer er arrangeret i celler i et regneark til repræsentation for brugeren.

## Kort historie ##

Følgende er nogle hurtige fakta om oprindelsen og historien for CSV-filformat.

* 1972 - IBM Fortran (niveau H udvidet) compiler understøttede dem under OS/360


* 1978 - Listestyret input/output blev understøttet af FORTRAN 77, der brugte kommaer og mellemrum til afgrænsere


* 2005 - CSV blev standardiseret med [RFC4180](https://tools.ietf.org/html/rfc4180) som en MIME-indholdstype.


* 2013 - RFC4180's mangler blev håndteret af en W3C-anbefaling


* 2015 - W3C lavede de første udkast til anbefalinger til CSV-metadatastandarder, der begyndte som anbefaling i december 2015


## Konverter CSV-filer ##

CSV-filer kan konverteres til flere forskellige filformater ved hjælp af de programmer, der kan åbne disse filer. For eksempel kan Microsoft Excel importere data fra CSV-filformat og gemme dem i filformaterne XLS, [XLSX](/spreadsheet/xlsx/), [PDF](/pdf/), [TXT](/word-processing/txt/), XML og [HTML](/web/html/). På samme måde giver andre desktop- og onlinetjenester mulighed for at eksportere CSV-filer til HTML, ODS og [RTF](/word-processing/rtf/).

## CSV-filformat ##

CSV-filformatet er kendt for at være angivet under [RFC4180](https://tools.ietf.org/html/rfc4180). Det definerer enhver fil til at være CSV-kompatibel, hvis:

* Hver post er placeret på en separat linje, afgrænset af et linjeskift (CRLF). For eksempel:

  * aaa,bbb,ccc CRLF
  * zzz,ååå,xxx CRLF
* Den sidste post i filen kan have et afsluttende linjeskift. For eksempel:

  * aaa,bbb,ccc CRLF
  * zzz,ååå,xxx
* Der kan være en valgfri overskriftslinje, der vises som den første linje i filen med samme format som normale optagelseslinjer. Denne overskrift vil indeholde navne svarende til felterne i filen og bør indeholde det samme antal felter som posterne i resten af filen (tilstedeværelsen eller fraværet af overskriftslinjen skal angives via den valgfrie "header" parameter i denne MIME-type). For eksempel:

  * feltnavn, feltnavn, feltnavn CRLF
  * aaa,bbb,ccc CRLF
  * zzz,ååå,xxx CRLF
* Inde i overskriften og hver post kan der være et eller flere felter, adskilt af kommaer. Hver linje skal indeholde det samme antal felter i hele filen. Mellemrum betragtes som en del af et felt og bør ikke ignoreres. Det sidste felt i posten må ikke efterfølges af et komma. For eksempel:

  * aaa,bbb,ccc
* Hvert felt kan eller må ikke være omgivet af dobbelte anførselstegn (dog bruger nogle programmer, såsom Microsoft Excel, slet ikke dobbelte anførselstegn). Hvis felter ikke er omgivet af dobbelte anførselstegn, vises der muligvis ikke dobbelte anførselstegn inde i felterne. For eksempel:\

  * aaa,bbb,ccc CRLF
  * zzz,ååå,xxx
* Felter, der indeholder linjeskift (CRLF), dobbelte anførselstegn og kommaer skal være omgivet af dobbelte anførselstegn. For eksempel:

  * aaa,b CRLF
  * bb,ccc CRLF
  * zzz,ååå,xxx
* Hvis der bruges dobbelte anførselstegn til at omslutte felter, skal et dobbelt anførselstegn, der optræder i et felt, escapes ved at indlede det med endnu et dobbelt anførselstegn. For eksempel:

  * aaa,bbb,ccc

Men i lyset af moderne brug er afgrænsningen ikke begrænset til kun komma og kan også være semikolon, tabulator eller mellemrum. Programmer såsom Microsoft Excel giver mulighed for at angive afgrænsningstegnet for import af poster fra en CSV-fil.

## Referencer

* [RFC 4180](https://tools.ietf.org/html/rfc4180)

* [RFC 2048](https://tools.ietf.org/html/rfc2048)

* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)



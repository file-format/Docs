{
  "date": "2021-04-10",
  "keywords": [
"TR3",
"Fil",
"Udvidelse",
"Filformat",
"e-bog",
"TomeRaider",
"Yadabyte"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om TR3 filformat og API'er, der kan oprette og åbne TR3 filer.",
  "title": "TR3 - TomeRaider 3 e-bogsfil",
  "linktitle": "TR3",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-tr-da3"
}
},
  "lastmod": "2021-04-10"
}

## Hvad er TR3 fil? ##

TR3-filen er en TomeRaider 3 e-bog, der understøtter hurtig søgning og komprimering. Det kan fungere korrekt gennem TomeRaider-relateret program. Yadabyte er udvikleren af denne software, et britisk software- og webudviklingsfirma baseret i Storbritannien. TomeRaider eBook-læserapplikationen kan bruges til at fungere korrekt og administrere indholdet af disse TR3-filer. Denne relaterede e-bogslæser kan installeres på computere, der kører på Microsoft Windows-baserede systemer og mange overførbare gadgets. TR3-filen tilhører gruppen af e-bogsfiler, der bruges i operativsystemer som Windows 10, Windows 7, Windows 8/8.1, Windows Vista, Windows XP.

TR3-specifikke **HTML-tags** er som følger:

|Tag|Beskrivelse|
---|---|
|\<new> |For at oprette TomeRaider-filer ud fra tekstfiler er den nye tag alt, der skal til.<new> tag definerer starten af siderne.|
|\<CATDEF> ... \</CATDEF> |definerer kategorinavnet|
|\<META> ... \</META> |er et tag, der bruges til at definere alle de metadata, der bruges i filformatet. Dette tag indeholder en række parametre.|
|\<EXPMSG> |Dette tag styrer den meddelelse, der vises, når en fil er udløbet. Når en bruger forsøger at se en side efter filen er udløbet, vises udløbsmeddelelsen i stedet for den faktiske sidetekst.|
|\<DIEMSG> |Dette tag ligner EXPMSG. Det bruges til at vise en meddelelse, når filen dør.|
|\<ENGMSG> |Dette tag bruges til at oprette den besked, der vises for krypterede sider. Meddelelsen vises i stedet for sideteksten, hvis brugeren forsøger at åbne en krypteret side, før den låses op.|
|\<expmsg> ,\<diemsg> og \<encmsg> |Ignoreret i sideteksten. De skal placeres i filoverskriften før den første<new> tag.|
|\<SELECTION> . \</ SELECTION> |Bruges til at understøtte forespørgsler. Dette tag skal være før det første<new> tag. Den kompilerer udvælgelsesdata for brugerens forespørgsel.|
|\<catset> . \</catset> | Bruges til at tildele kategorinavne til hvert emne.|


## Problemer med at åbne en TR3 fil ##

Her er listen over nogle almindelige problemer, der kan opstå og forårsage fejlfunktion af filformatet:

* Korrupt fil
* Inficeret fil på grund af virus
* Ukorrekte links til TR3-filen i arkivadgang
* Ingen adgangsret i systemet til at åbne filerne
* Forældet drev i dit system
* Fjernelse af rapporten fra TR3 fra Windows-arkivet
* Kontakt udvikleren kan være en bedre mulighed for bedre output


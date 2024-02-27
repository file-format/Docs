{
  "date": "2019-10-11",
  "keywords": [
"chm",
"chm filen",
"chm filformat",
"chm filtype",
"fil",
"type",
"hvad er en chm-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CHM - Kompileret HTML-hjælpefilformat",
  "description": "Lær om, hvad en CHM-fil og API'er er, der kan oprette og åbne dem.",
  "linktitle": "CHM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ch-dam"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er CHM fil?

CHM-filformatet repræsenterer Microsoft **[HTML](/web/html/)** hjælpefil, der består af en samling HTML-sider. Det giver et indeks til hurtig adgang til emnerne og navigation til forskellige dele af hjælpedokumentet. CHM-filen kan søges efter indhold via den medfølgende søgemulighed. CHM er Microsofts proprietære online hjælpefilformat, der ofte bruges til softwaredokumentation. Derudover bruges det i flere andre applikationer som træningsvejledninger, interaktive bøger og elektroniske nyhedsbreve. De fleste af de moderne Microsoft-udviklingsmiljøer understøtter generering af CHM-dokumentation fra information, der er tilgængelig i applikationen.

CHM-filformatets unikke evne til at implementere en kombineret indholdsfortegnelse og indeks gør det forskelligt fra andre standard HTML-sider. Den genererede CHM-fil er relativt lille i størrelse og kan derfor nemt distribueres med softwarepakker. Hjælpeværktøjet HTML Help Workshop giver et brugervenligt system til at oprette og administrere hjælpeprojekter og deres relaterede filer. CHM-filer kan indeholde tekst, billeder og hyperlinks; kan ses i en webbrowser; bruges af Windows og andre programmer som en onlinehjælpeløsning.

## CHM filformat

Den endelige form for genereret CHM-fil afhænger af, hvordan hjælpesystemet er designet, og om det er beregnet til et program eller et websted. En CHM-fil understøtter datakomprimering med LZX-komprimering for at generere de komprimerede HTML-filer. Den har den indbyggede søgemaskine til hurtig søgning af indhold sammen med evnen til at flette flere .CHM-filer. En CHM-fil består af et sæt HTML-filer, en sammenkædet indholdsfortegnelse og en indeksfil.

### HTML-filer

Uanset om du opretter hjælpeemner til distribution med et program eller på nettet, er de dokumenter, du forfatter, oprettet ved hjælp af et særligt formateringssprog kendt som Hypertext Markup Language (HTML). HTML-emnefiler har filtypenavnet .htm eller .html.

Selvom hvert hjælpeemne eller hver webside, du forfatter, ser ud til at være et dokument med tekst, grafik eller animerede billeder, er .htm-filer faktisk tekstdokumenter, der har specielle HTML-formateringskoder. Disse koder, kaldet tags, fortæller en browser, hvordan hver side skal vises. Kun den tekst, der vises i et emne eller en webside, er faktisk i .htm-filen. Enhver grafik, lyd, animerede billeder eller andre elementer, der vises, er separate filer, som din HTML-fil peger på. Browseren kopierer eller downloader grafikken, lydene eller andre elementer, når den ser tags, der fortæller den at gøre det.

### Indholdsfortegnelse (TOC)
Hjælpeindholdsfortegnelsen (.hhc)-filen er en HTML-fil, der indeholder emnetitlerne til din indholdsfortegnelse. Når en bruger åbner indholdsfortegnelsen i en kompileret hjælpefil (eller på en webside) og klikker på en emnetitel, åbnes HTML-filen, der er knyttet til den pågældende titel.

### Indeksfil
Indeksfilen (.hhk) er en HTML-fil, der indeholder indeksindgange (søgeord) til dit indeks. Når en bruger åbner indekset i en kompileret hjælpefil eller på en webside og klikker på et nøgleord, åbnes HTML-filen, der er knyttet til nøgleordet.

## HTML-hjælpekomponenter

HTML-hjælp består af flere komponenter. Disse omfatter følgende:

* `HTML Help Workshop`: a help authoring tool with an easy-to-use graphical interface for creating project files, HTML topic files, contents files, index files, and everything else you need to put together an online help system or Web site.
* `HTML Help ActiveX-kontrol`: et lille, modulært program, der bruges til at indsætte hjælpenavigation og sekundær vinduesfunktionalitet i en HTML-fil.

* `The HTML Help Viewer`: et fuldt funktionelt og tilpasseligt vindue med tre ruder, hvor online hjælpeemner kan vises.

* `Microsoft HTML Help Image Editor`: et online grafikværktøj til at lave skærmbilleder; og til konvertering, redigering og visning af billedfiler.

* `The HTML Help Java Applet`: et lille, Java-baseret program, der kan bruges i stedet for et ActiveX-objekt til at indsætte hjælpenavigation i en HTML-fil.

* `Det eksekverbare program til HTML-hjælp`: programmet, der viser og kører hjælp, når du klikker på en kompileret hjælpefil.

* `HTML Help compiler`: programmet, der kompilerer projekt, indhold, indeks, emne og andre filer til en kompileret hjælpefil.

* `The HTML Help Authoring Guide`: an online guide designed to assist help authors in using HTML Help to design a help system. The guide also contains a complete HTML Help reference for developers and an HTML tag reference for authors.

## Referencer

* [Microsoft HTML-hjælp](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)

* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)



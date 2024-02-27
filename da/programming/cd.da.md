{
  "date": "2020-01-10",
  "keywords": [
"cd",
".cd",
"hvad er en cd-fil",
"hvordan man åbner en cd-fil",
"udvidelse",
"fil",
"cd fil",
"cd filformat",
"cd filtypenavn"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CD - Visual Studio Class Diagram File",
  "description": "Lær om cd-filformater og API'er, der kan oprette og åbne cd-filer.",
  "linktitle": "CD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c-dad"
}
},
  "lastmod": "2021-06-24"
}

## Hvad er en CD-fil?

En fil med filtypen .cd er en Visual Studio-klassediagramfil, der giver information om strukturen og forholdet mellem alle klasserne i den aktuelle løsning. En Visual Studio-løsning (repræsenteret af [.sln](/programming/sln/)) kan indeholde et eller flere projekter, der hver har flere forskellige klasser. Klassediagramfilen kan genereres ved at højreklikke på projektet og vælge indstillingen klassediagram.

## Klassediagram (.cd) filformat - flere oplysninger

En klassediagramfil gemmes i standard XML-filformat, der repræsenterer klasser i et projekt som XML-noder. Hvis Visual Studio ikke er tilgængelig, kan disse klassediagramfiler åbnes i ethvert program, der understøtter åbning af XML-filer.

### Sådan tilføjes klassediagrammer til Visual Studio Project

I Visual Studio skal du åbne den løsning/projekt, som du vil tilføje klassediagrammet til. Højreklik derefter på projektnoden, og vælg derefter Tilføj > Nyt element. Eller tryk på Ctrl+Shift+A.

 * Dialogboksen Tilføj nyt element åbnes.

 * Udvid Fælles elementer > Generelt, og vælg derefter Klassediagram fra skabelonlisten. For Visual C++-projekter, se i kategorien Utility for at finde klassediagramskabelonen.

### Eksporter klassediagrammer (CD) til billeder

Visual Studio gør det muligt at konvertere/eksportere klassediagrammer til billeder såsom [PNG](/image/png/), [JPEG](/image/jpeg/) og [BMP](/image/bmp/). Disse eksporterede klassediagramfiler kan bruges til dokumentation og teknisk datapakke (TDP) registreringsformål. For at konvertere et klassediagram til billede kan følgende trin bruges fra Microsoft Visual Studio.

1. Åbn din klassediagram (.cd) fil.
1. Fra menuen Klassediagram eller genvejsmenuen for diagramoverfladen skal du vælge Eksporter diagram som billede.
1. Vælg et diagram.
1. Vælg det format, du ønsker.
1. Vælg Eksporter for at afslutte eksporten.

## Referencer

* [Designkurser i Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)



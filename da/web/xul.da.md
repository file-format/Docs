{
  "date": "2021-05-24",
  "keywords": [
"xul",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"XML-brugergrænsefladesprog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XUL - XML User Interface Language File",
  "description": "Lær om XUL filformat og API'er, der kan oprette og åbne XUL filer.",
  "linktitle": "XUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xu-dal"
}
},
  "lastmod": "2021-05-24"
}

## Hvad er en XUL fil?

En fil med filtypen .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) står for XML User Interface Language) er en [XML](/web/xml/)-baseret markup-sprogfil til oprettelse af brugergrænseflader. Det blev udviklet af Mozilla for udviklere til at skabe grafiske brugergrænsefladeelementer, der ligner andre markup-sprog, der bruges til at oprette websider. XUL har været meget i brug af Mozilla i sin Firefox-browser, hvor den brugte Mozilla-kodebasen. XUL-gengivelse udføres ved hjælp af
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software)). Firefox-gafler som Pale Moon, Basilisk og Waterfox bevarer understøttelse af XUL-tilføjelser. XUL-filer er identificeret med MIME-type: application/vnd.mozilla.xul+xml.

## XUL filformat

XUL-filer er skrevet i almindelig tekst baseret på XML-filformat og gengives ved hjælp af Gecko-motoren. De tre hoveddele af en XUL-struktur er:

 * `Indhold` - Dette inkluderer vinduets erklæringer og brugergrænsefladeelementerne indeholdt i dem.
 * `Skin` - Det inkluderer alle typografiark, billeder og andre temarelaterede filer. Udseendet af et vindue er beskrevet i typografiarkene.
 * `Locale` - Tekst, der vises i et vindue, gemmes separat, og flere sæt sprogfiler kan bruges af brugere.

### XUL-eksempel

Følgende eksempel skaber tre knapper, der er stablet oven på hinanden i lodret retning.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Referencer

* [XUL - af Wikipedia](https://en.wikipedia.org/wiki/XUL)

* [XUL Arkiveret dokumentation - Af Mozilla](https://wiki.mozilla.org/XUL:Home_Page)



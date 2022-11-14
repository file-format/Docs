{
  "date" : "2021-05-24",
  "keywords" :["xul", "File", "Extension", "File Format", "File Extension", "XML User Interface Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML-taalbestand voor gebruikersinterface",
  "description":"Meer informatie over XUL-bestandsindelingen en API's die XUL-bestanden kunnen maken en openen.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Wat is een XUL-bestand?

Een bestand met de extensie .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) staat voor XML User Interface Language) is een op [XML](/nl/web/xml/) gebaseerd opmaaktaalbestand voor gebruikersinterfaces maken. Het is ontwikkeld door Mozilla voor ontwikkelaars om grafische gebruikersinterface-elementen te maken die vergelijkbaar zijn met andere opmaaktalen die worden gebruikt voor het maken van webpagina's. XUL is op grote schaal in gebruik door Mozilla in zijn Firefox-browser, waar het de Mozilla-codebase gebruikte. XUL-rendering wordt uitgevoerd met behulp van de
[Gecko-engine](https://en.wikipedia.org/wiki/Gecko_(software)). Firefox-vorken zoals Pale Moon, Basilisk en Waterfox behouden ondersteuning voor XUL-add-ons. XUL-bestanden worden geïdentificeerd met MIME-type: application/vnd.mozilla.xul+xml.

## XUL-bestandsindeling

XUL-bestanden zijn geschreven in platte tekst op basis van XML-bestandsindeling en worden weergegeven met behulp van de Gecko-engine. De drie belangrijkste onderdelen van een XUL-structuur zijn:

* `Inhoud` - Dit omvat de verklaringen van het venster en de elementen van de gebruikersinterface die daarin zijn opgenomen.
* `Skin` - Het bevat alle stylesheets, afbeeldingen en andere themagerelateerde bestanden. Het uiterlijk van een venster wordt beschreven in de stylesheets.
* `Locale` - Tekst die in een venster wordt weergegeven, wordt afzonderlijk opgeslagen en gebruikers kunnen meerdere sets taalbestanden gebruiken.

### XUL Voorbeeld

In het volgende voorbeeld worden drie knoppen gemaakt die in verticale richting op elkaar zijn gestapeld.

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

## Referenties

* [XUL - Door Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [XUL gearchiveerde documentatie - door Mozilla](https://wiki.mozilla.org/XUL:Home_Page)


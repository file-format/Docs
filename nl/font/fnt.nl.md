{
  "date" : "2020-08-20",
  "keywords" :[ "fnt-bestand", "fnt-bestandsindeling", "wat is een fnt-bestand", "bestand", "fnt-voorbeeld", "fnt-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows-lettertypebestand",
  "description":"Meer informatie over de FNT-bestandsindeling en API's die FNT-bestanden kunnen maken en openen.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Wat is een FNT-bestand?

Een bestand met de extensie .fnt is een lettertypebestand dat algemene lettertype-informatie op Windows-besturingssystemen opslaat. FNT-bestanden zijn grotendeels vervangen door TrueType (.TTF) en OpenType (.OTF) bestandsindelingen en zijn vanaf nu een verouderde bestandsindeling voor lettertypen. Deze bestanden kunnen een enkele beoordelaar of vectorlettertype opslaan. Alle apparaatstuurprogramma's ondersteunen de Windows 2.x-lettertypen. Niet alle apparaatstuurprogramma's
ondersteuning van de Windows 3.0-versie.

## FNT-bestandsindeling

FNT-bestanden kunnen een enkel raster- of vectorlettertype opslaan. De vectorformaten worden vaker gebruikt door GDI in vergelijking met het raster waar de glyph van elk charter wordt gedefinieerd met behulp van een kleine bitmap. De voor de hand liggende reden voor de vervanging van .fnt door .ttf en .otf is het rasterformaat.

### Koptekst van lettertypebestand
Het begin van zowel raster- als vectorlettertypebestanden is gebruikelijk, gevolgd door verschillende informatie voor elk type bestand. De header van het lettertypebestand bevat voor Windows 3.0 zes nieuwe velden die als volgt zijn ingesteld op nul om compatibiliteit met toekomstige versies van Windows te garanderen.

* dvlaggen
* dfAspace
* dfBspatie
* dfCspace
* dfColorPointer
* dfGereserveerd1

Ga voor gedetailleerde informatie over de headers voor Windows 3.0 en 2.0 naar het [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Referenties
* [Lettertype Bestandsformaat](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Een lettertype installeren of verwijderen in Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)


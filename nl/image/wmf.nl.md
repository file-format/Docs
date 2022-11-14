{
  "date" : "2019-10-11",
  "keywords" :[ "wmf-bestand", "wmf-bestandsformaat", "wat is een wmf-bestand", "bestand", "wmf-voorbeeld", "wmf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows Metafile Format",
  "description":"Meer informatie over WMF-bestandsindelingen en API's die WMF-bestanden kunnen maken en openen.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een WMF-bestand?

Bestanden met de WMF-extensie vertegenwoordigen Microsoft Windows Metafile (WMF) voor het opslaan van zowel vector- als bitmap-afbeeldingsgegevens. Om nauwkeuriger te zijn, WMF behoort tot de vectorbestandsindelingscategorie van Grafische bestandsindelingen die apparaatonafhankelijk is. Windows Graphical Device Interface (GDI) gebruikt de functies die zijn opgeslagen in een WMF-bestand om een afbeelding op het scherm weer te geven. Een meer verbeterde versie van WMF, bekend als Enhanced Meta Files (EMF), werd later gepubliceerd, waardoor het formaat rijker is aan functies. In de praktijk is WMF vergelijkbaar met SVG.

## Specificaties WMF-bestandsindeling ##

Een WMF-bestand verwees naar de 16-bits bestandsindeling op het moment van lancering met Windows 3.0. Het bestandsformaat bestaat uit een reeks records met variabele lengte die grafische tekenopdrachten, objectdefinities en eigenschappen bevatten. Omdat WMF-bestanden zijn gebaseerd op opdrachten die aan de GDI worden weergegeven om de afbeelding te tekenen, staat het ook bekend als een digitale opname van de afbeelding die kan worden afgespeeld om die afbeelding te reproduceren. De volledige specificaties van het bestandsformaat van WMF zijn online beschikbaar en moeten worden geraadpleegd voor de ontwikkeling van toepassingen om met WMF-bestanden te werken. Een WMF-bestand is georganiseerd in een:

* WMF-koptekstrecord
* WMF-record(s)
* WMF End-of-File Record

### WMF-koprecord ###

Het **META_HEADER Record** bevat informatie die de kenmerken van het metabestand definieert, waaronder:

* Het type van het metabestand
* De versie van het metabestand
* De grootte van het metabestand
* Het aantal objecten gedefinieerd in het metabestand
* De grootte van de grootste afzonderlijke record in het metabestand

### WMF Plaatsbare Header Record ###

Het **META_PLACEABLE Record** bevat uitgebreide informatie over de afbeelding, waaronder:

* Een begrenzende rechthoek
* Logische eenheidsgrootte, voor schaling
* Een controlesom, ter validatie

### WMF-record ###

WMF-records hebben een generiek formaat, dat is gespecificeerd in het specificatiedocument. Elk WMF-record bevat de volgende informatie:

* De recordgrootte:
* De opnamefunctie
* Parameters, indien aanwezig, voor de opnamefunctie

## Referenties ##

* [[MS-WMF]: Windows-metabestandsindeling](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)


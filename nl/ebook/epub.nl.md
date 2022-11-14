{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "bestand", "extensie", "formaat", "E-Book", "Digitaal boek"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over EPUB-bestandsindelingen en API's die EPUB-bestanden kunnen maken en openen.",
  "title" :"Wat is een EPUB-bestand?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Wat is een EPUB-bestand?

Bestanden met de extensie .epub zijn een bestandsindeling voor e-books die uitgevers en consumenten een standaard digitale publicatie-indeling bieden. Het formaat is inmiddels zo gangbaar dat het door veel e-readers en softwareapplicaties wordt ondersteund. Op Mac OS biedt de vooraf geïnstalleerde **Books**-software bijvoorbeeld ondersteuning voor het openen van dergelijke bestanden. Daarnaast is er veel compatibele software beschikbaar voor smartphones, tablets en computers. EPUB-bestandsstandaarden worden onderhouden door het [International Digital Publishing Forum ](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). De versie EPUB 3 wordt ook onderschreven door de Book Industry Study Group (BISG), een toonaangevende boekhandelsvereniging voor gestandaardiseerde best practices, onderzoek, informatie en evenementen, voor het verpakken van inhoud.

## Korte geschiedenis van het EPUB-bestandsformaat

* **Oktober 2007** - EPUB 2.0 is goedgekeurd
* **September 2010** - Onderhoudsupdate uitgebracht
* **Oktober 2011** - EPUB 3.0-specificaties zijn van kracht geworden
* **Juni 2014** - Er is een kleine onderhoudsupdate uitgebracht om de 3.0-versie te vervangen
* **Januari 2017** - EPUB 3.1 is van kracht geworden

## EPUB-bestandsindeling

EPUB-bestandsindeling is een archief waarvan de naam kan worden gewijzigd in de extensie [ZIP](/nl/compression/zip/) en de inhoud ervan kan worden bekeken door het archief uit te pakken met een willekeurige archiefextractor. Het is een open XML-gebaseerd formaat en bestaat uit HTML-bestanden, afbeeldingen, CSS-stijlbladen en andere elementen. Het kan ook worden geconverteerd naar PDF, Mobi en verschillende andere bestandsindelingen via een aantal softwaretoepassingen en API's.

{{< figure src="../epub.png" alt="EPUB-bestandsindeling" >}}

**EPUB E-Book geopend met Mac OS Books Application**

Het EPUB-bestandsformaat is gebaseerd op de volgende drie open standaarden.

### Open Publieke Structuur (OPS) ###

Een EPUB 2.0-bestand gebruikt XHTML 1.1 om de inhoud van een publicatie te construeren. In essentie betekent dit dat een EPUB-bestand uit een of meer webpagina's bestaat. Ook al zou je de volledige inhoud van een boek of krant op één pagina kunnen opnemen, het is beter dat zo'n bestand niet groter is dan 300K, zowel om prestatie- als compatibiliteitsredenen. Net als bij gewone webpagina's wordt de styling en lay-out bepaald met behulp van cascading style sheets (CSS). In EPUB-bestanden moet een subset (beperkte reeks opdrachten) van CSS2 worden gebruikt. Veel van de nieuwe functies van CSS3, zoals afgeronde vakken of slagschaduwen, zijn nog niet beschikbaar. Voor achterwaartse compatibiliteit kan een maker ook DTBook gebruiken in plaats van XHTML om de inhoud te coderen.

### Open verpakkingsformaat (OPF) ###

Dit deel van de specificaties behandelt structurele informatie zoals metadata (wie is de auteur en de uitgever, wat is de titel,..), het manifest (een lijst van alle bestanden in een epub-bestand) en de inhoudsopgave. Deze gegevens zijn allemaal ingesloten met behulp van XML.

### Open Container Format (OCF) ###

Zoals de bovenstaande beschrijvingen duidelijk hadden moeten maken, bestaat een EPUB-document uit een reeks bestanden. De OCF-specificaties bepalen hoe al die bestanden uiteindelijk worden verpakt in één enkel containerbestand. Hiervoor wordt ZIP-compressie gebruikt.

## Ondersteunde bestandsindelingen voor afbeeldingen ##

De EPUB-bestandsindeling ondersteunt de volgende afbeeldingsbestandsindelingen.

* [GIF](/nl/image/gif/)
* [JPG](/nl/image/jpeg/)
* [PNG](/nl/image/png/)
* [SVG](/nl/page-description-language/svg/)

## Referenties ##

* [EPUB - Door Wikipedia](https://en.wikipedia.org/wiki/EPUB)


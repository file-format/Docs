{
  "date" : "2020-08-20",
  "keywords" :[ "ttf-bestand", "ttf-bestandsformaat", "wat is een ttf-bestand", "bestand", "ttf-voorbeeld", "ttf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - TrueType-lettertypebestandsindeling",
  "description":"TrueType-lettertypen (TTF) zijn gebaseerd op specificaties voor digitale lettertypetechnologie die oorspronkelijk zijn ontworpen door Apple, Inc. Zowel Apple als Microsoft gebruikten TTF op Mac- en Windows-besturingssystemen.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Wat is een TTF-bestand?

Een bestand met de extensie .ttf vertegenwoordigt lettertypebestanden op basis van de TrueType-lettertypetechnologie. Het werd oorspronkelijk ontworpen en gelanceerd door Apple Computer, Inc voor Mac OS en werd later overgenomen door Microsoft voor Windows OS. TrueType-lettertypen bieden weergave van de hoogste kwaliteit op computerschermen en printers zonder enige afhankelijkheid van resolutie. Alle moderne applicaties die lettertypen gebruiken, kunnen met TTF-bestanden werken. TTF-lettertypebestanden zijn vrij beschikbaar via internet en kunnen ook worden geconverteerd naar andere lettertypebestandsindelingen zoals OTF en WOFF.

## Korte geschiedenis

Ontworpen door Apply Computer, Inc in de jaren 80 voor MacOS, was het TTF-lettertypeformaat bedoeld om enkele technische beperkingen van Adobe's Type 1-formaat op te lossen. Apple voegde in 1991 ondersteuning toe voor TrueType-lettertypen in Mac. Het ontwerpdoel achter TTF-lettertypen was efficiëntie in opslag en verwerking, en uitbreidbaarheid. Op basis van deze uitbreidbaarheid kunnen bestaande lettertypen worden geconverteerd naar TrueType-indeling.

Microsoft gebruikte de TrueType-lettertypen voor het eerst in Windows 3.1 in april 1992 nadat Apple ermee instemde TrueType in licentie te geven aan Microsoft. Het verbeterde het rastermechanisme en verbeterde de efficiëntie en prestaties.

## Specificaties True Type-bestandsindeling

Een TrueType-lettertypebestand is een binair bestand dat bestaat uit een reeks aaneengeschakelde tabellen. Elke tabel is een reeks woorden en heeft een naam die bekend staat als 'Tag'. Elke tag is van het gegevenstype uint32 en bestaat uit vier tekens. De eerste tabel in het bestand is de lettertypemap die toegang geeft tot andere tabellen in het lettertypebestand. Lettertypegegevens zijn opgenomen in andere tabellen die worden gevolgd na de tabel met lettertypedirectory's. Aangezien elke tabel toegankelijk is via zijn tag, kunnen de tabellen in elke volgorde in het bestand worden weergegeven.

De vereiste tabellen en hun tagnamen worden weergegeven in de volgende tabel.

|**Tag**|**Tabel**|
---|---|
|'cmap'| karakter naar glyph mapping|
|'glyf'| glyph-gegevens|
|'hoofd'| lettertype header|
|'hea'| horizontale kop|
|'hmtx'| horizontale statistieken|
|'plaats'| index naar locatie|
|'maxp'| maximaal profiel|
|'naam'| naamgeving|
|'post'| PostScript|

### Gegevenstypen
TrueType-lettertypen gebruiken de standaard integer en aanvullende gegevenstypen zoals vermeld in de volgende tabel.

|**Gegevenstype** | **Beschrijving** |
---|---|
|shortFrac| 16-bits ondertekende breuk|
|Vast| 16,16-bits getekende vaste-kommagetal|
|FWoord| 16-bits geheel getal met teken dat een hoeveelheid beschrijft in FUnits, de kleinste meetbare afstand in em-ruimte.|
|uFWoord| 16-bits geheel getal zonder teken dat een hoeveelheid beschrijft in FUnits, de kleinste meetbare afstand in em-ruimte.|
|F2Dot14| 16-bits vast getal met teken, waarbij de lage 14 bits een breuk vertegenwoordigen.|
|longDateTime| Het lange interne formaat van een datum in seconden sinds 12.00 uur middernacht, 1 januari 1904. Het wordt weergegeven als een 64-bits geheel getal met teken.|

### Lettertypemap

De eerste tabel in het TrueType-lettertype is de lettertypemap die toegang geeft tot de informatie die nodig is voor toegang tot gegevens in andere tabellen. Het bestaat verder uit:

* `Offset subtabel` - houdt de tabellen in het lettertype bij en biedt offset-informatie om toegang te krijgen tot elke tabel in de directory
* `Tabelmap` - Bevat vermeldingen voor elke tabel in het lettertype

#### Offset subtabel
De offset-subtabel wordt hieronder weergegeven.

|**Type**|**Naam**|**Beschrijving**|
---|---|---|
|uint32| scaler-type| Een tag om de OFA-scaler aan te geven die moet worden gebruikt om dit lettertype te rasteren; zie de opmerking over het type scaler hieronder voor meer informatie.|
|uint16| aantalTabellen| aantal tafels|
|uint16| zoekbereik| (maximaal vermogen van 2 <= numTables)*16|
|uint16| entrySelector| log2(maximaal vermogen van 2 <= numTables)|
|uint16| bereikShift| aantalTables*16-zoekbereik|

#### Tabeldirectory
De tabeldirectory komt direct na de offset-subtabel. De structuur is zoals weergegeven in de volgende tabel.

|**Type**|**Naam**|**Beschrijving**|
---|---|---|
|uint32| tag| 4-byte-ID|
|uint32| checkSom| controlesom voor deze tabel|
|uint32| compenseren| offset vanaf het begin van sfnt|
|uint32| lengte| lengte van deze tabel in byte (werkelijke lengte niet opgevulde lengte)|

Elke tabel in een lettertypebestand moet zijn eigen tabeldirectory-item hebben. Items in een tabel moeten in oplopende volgorde op tag worden gesorteerd.


## Referenties
* [TrueType-lettertypereferentiehandleiding](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [TrueType-overzicht](https://learn.microsoft.com/en-us/typography/truetype/)


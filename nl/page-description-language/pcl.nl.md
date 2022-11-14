{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Meer informatie over PCL-bestandsindelingen en API's die PCL-bestanden kunnen maken en openen.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PCL-bestand? ##

PCL staat voor Printer Command Language, een Page Description Language die is geïntroduceerd door Hewlett Packard (HP). HP heeft PCL gecreëerd om een efficiënte manier te bieden voor het beheren van printerfuncties op veel verschillende afdrukapparaten. Het formaat is oorspronkelijk ontwikkeld voor HP's dot-matrix- en inkjetprinters, maar is in de loop van de tijd onderdeel geworden van verschillende thermische, matrix- en paginaprinters. Het formaat onderging verschillende revisies, wat resulteerde in verschillende versies waarbij elke versie werd verbeterd om te voldoen aan de eisen van de tijd met betrekking tot de printerbesturingsfuncties. Vandaag de dag is PCL de meest verspreide printertaal in de laatste printermarkt.

## PCL-versies ##

PCL-versies verschillen in functionaliteit (bijv. ondersteuning van lettertypen: bitmaplettertypen, schaalbare lettertypen (Intellifonts, TrueType-lettertypen), rastergrafische compressiemethoden, HP-GL/2 grafische ondersteuning).

**PCL 1:** rond 1980 - Print- en Space-functionaliteit is de basisset van functies voor eenvoudige, handige werkstationuitvoer voor één gebruiker.

**PCL 2:** rond 1980 - EDP (Electronic Data Processing)/Transaction-functionaliteit is een superset van PCL 1. Er zijn functies toegevoegd voor algemene doeleinden, systeemprinten voor meerdere gebruikers.

**PCL 3**: 1984 - Office-tekstverwerkingsfunctionaliteit is een superset van PCL 2. Er zijn functies toegevoegd voor de productie van hoogwaardige kantoordocumenten en verhoogde dpi tot 300 dpi. Het stond het gebruik van een beperkt aantal bitmap-lettertypen en afbeeldingen toe en ondersteunde HP-GL. PCL 3 werd op grote schaal geïmiteerd door andere printerfabrikanten en werd door deze bedrijven aangeduid als "LaserJet Plus-emulatie".
(Printers: HP DeskJet familie, HP LaserJet serie printer, HP LaserJet Plus serie printer)

**PCL3+:** Gebruikt door DeskJet en DesignJet printerfamilies.

**PCL3c:** Gebruikt door DeskJet en DesignJet printerfamilies.

**PCL3e**: Gebruikt door DeskJet en DesignJet printerfamilies. Nu ook gebruikt in PhotoSmart.

**PCL3GUI**: gebruikt RTL en wordt gebruikt door de DeskJet- en DesignJet-printerfamilies.

**PCLSLEEK**: gebruikt RTL en wordt gebruikt door de DeskJet- en DesignJet-printerfamilies.

**PCL 4**: 1985 - De functie voor pagina-opmaak is een superset van PCL 3. Ondersteunde macro's, grotere bitmaplettertypen en afbeeldingen. (Printers: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing-functionaliteit is een superset van PCL 4. Nieuwe publicatiemogelijkheden zijn onder meer het schalen van lettertypen en HP-GL/2 (vector) graphics. (Printers: HP LaserJet III)

**PCL 5e:** 1994 - Dit is een ingrijpende herziening, met nieuwe functies zoals Adaptive Compression System, 2-byte tekencodering, ondersteuning voor vectorlettertypen en bidirectionele configuratieopdrachten. Bevat logische bewerkingen (komt overeen met GDI ROP's) om Windows-ondersteuning te verbeteren voordat paden worden geknipt. (Printers: HP LaserJet 4)

**PCL 5j:** Nieuwe functies zoals 2-byte tekenondersteuning voor Japanse residente schaalbare lettertypen, verticaal schrijven, Japanse papierformaten en lettertekenreeksen. (Printers: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Kleurondersteuning en logische bewerkingen zijn toegevoegd aan PCL5. PCL5c is ouder dan PCL5e. Sommige modellen ondersteunen ook uitknippaden. (Printers: HP Color LaserJet, HP PaintJet 300 XL (eerste printer met PCL5c), HP DeskJet 1200C/1600C (deze modelnummers zijn hergebruikt en de nieuwere modellen zijn niet PCL 5c)

**PCL 5ce:** Ondersteunt schaalbare lettertypen van Agfa Microtype. (Printers: HP 2500c Pro-printer)

**PCL 6 / XL:** 1996 - PCL 6 of PCL XL is een nieuw formaat dat in 1995 werd geïntroduceerd en dat niet compatibel is met eerdere versies van PCL. (Printers: HP LaserJet 5, 5M en 5N)

## PCL 6 Overzicht ##

HP introduceerde PCL 6 in 1996, de volgende evolutie van de PCL-taal en aanverwante technologieën. Het heeft de volgende componenten:

**PCL 6 Enhanced:** biedt een geoptimaliseerde versie voor afdrukken vanuit grafische gebruikersinterfaces (GUI's) zoals MS Windows en OS/2

**PCL 6 Standard:** biedt volledige achterwaartse compatibiliteit met eerdere HP LaserJet-printers

**PCL Font Synthesis:** biedt schaalbare lettertypen, lettertypebeheer en opslag van formulieren en lettertypen.

De uitgebreide versie PCL XL ligt dichter bij GDI die veel toepassingen gebruiken. Het zorgt ervoor dat er minder vertalingen plaatsvinden, wat resulteert in verhoogde WYSIWYG-mogelijkheden en betere prestaties met applicaties die escapes ondersteunen die zijn geïmplementeerd door de Enhanced driver. De uitvoer van de Enhanced (PCL XL) driver is mogelijk niet hetzelfde als de uitvoer van de Standard driver. Als de uitvoer niet is zoals verwacht, kiest u in plaats daarvan de standaarddriver (PCL5e).

PCL 6 Enhanced-opdrachten zijn ontworpen om optimaal te voldoen aan de grafische afdrukvereisten voor op GUI gebaseerde toepassingen. In de meeste gevallen is er voor elke grafische afdrukopdracht die een GUI wil uitvoeren, een bijpassende PCL 6 Enhanced-opdracht. Dit vermindert het aantal commando's dat nodig is om een grafische pagina te beschrijven. Elke opdracht in PCL 6 Enhanced is ontworpen om minimale gegevensoverdracht van de host-pc naar de printer te vereisen. Dit vermindert de hoeveelheid gegevens die nodig is om een pagina te beschrijven.

Het Windows-afdruksysteem voor de meeste HP LaserJet-printers biedt twee afzonderlijke stuurprogramma's: Standaard en Verbeterd. Het Standard-stuurprogramma biedt achterwaartse compatibiliteit door gebruik te maken van PCL 6 Standard (PCL5e)-opdrachten voor het afdrukken van eenvoudige tekst of pagina's met gemengde tekst en afbeeldingen. Het Enhanced-stuurprogramma maakt gebruik van de PCL 6 Enhanced-opdrachten die zijn geoptimaliseerd voor het afdrukken van complexe grafische pagina's.

## PCL 6 klasse herzieningen ##

#### Klasse 1.1 ####

**Tekentools:** Ondersteuning voor tekenlijnen, bogen/ellipsen/akkoorden, (afgeronde) rechthoeken, polygonen, Bezier-paden, uitgeknipte paden, rasterafbeeldingen, scanlijnen, rasterbewerkingen.
**Kleurverwerking:** Ondersteuning voor 1/4/8-bits paletten, RGB/grijze kleurruimte. Ondersteuning van aangepaste halftoonpatronen (max. 256 patronen).
**Compressie:** Ondersteunt RLE.
**Maateenheden:** Inch, millimeter, tiende millimeter.
**Papierverwerking:** Ondersteunt aangepaste of vooraf gedefinieerde sets papiersoorten, waaronder gewone Letter, Legal, A4, enz. U kunt papier kiezen uit handmatige invoer, laden, cassettes. Papier kan horizontaal of verticaal dubbelzijdig worden bedrukt. Papier kan worden georiënteerd in portret, landschap of 180 graden rotatie van de eerste twee.
**Lettertype:** Ondersteunt bitmap- of TrueType-lettertypen, 8- of 16-bits codepunten. Bij het kiezen van een tekenset wordt een andere symbolensetcode gebruikt dan bij PCL 5. Als een bitmaplettertype wordt gebruikt, zijn veel schaalopdrachten niet beschikbaar. Wanneer TrueType-lettertypen worden gebruikt, worden descriptors met variabele lengte en vervolgblokken niet ondersteund. Omtreklettertype kan worden gedraaid, geschaald of geschoren.

#### Klasse 2.0 ####

**Compressie:** Een eigen JPEG-compressie toegevoegd genaamd JetReady.
**Papierverwerking:** Media kunnen worden omgeleid naar verschillende uitvoerbakken (maximaal 256). A6 en Japanse B6 vooraf ingestelde mediaformaten toegevoegd. Derde cassette-preset toegevoegd, 248 externe mediabronnen.
**Lettertype:** Tekst kan verticaal worden geschreven.

#### Klasse 2.1 ####

**Kleurverwerking:** Functie voor kleurafstemming toegevoegd.
**Compressie:** Delta Row toegevoegd.
**Papierverwerking:** Afdrukstand, mediaformaat zijn optioneel bij het declareren van een nieuwe pagina. B5, JIS 8K, JIS 16K, JIS Exec papiersoorten toegevoegd.

#### Klasse 3.0 ####

**Kleurverwerking:** Sta het gebruik van verschillende halftooninstellingen toe voor vector- of rasterafbeeldingen, tekst. Ondersteunt adaptieve halftonen.
**Protocol:** Ondersteunt PCL-doorvoer, waardoor PCL 5-functies kunnen worden gebruikt door PCL 6-streams. Sommige PCL 6-statussen blijven echter niet behouden bij gebruik van deze functie.
**Lettertype:** Ondersteunt PCL-lettertypen.
**Viewer/Converter:** PCLReader (freeware) kan elk niveau van PCL 6 (inclusief JetReady) naar elke printer bekijken, converteren of afdrukken.

## Referenties ##

* [PCL - Door Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)


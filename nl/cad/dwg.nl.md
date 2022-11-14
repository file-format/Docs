{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Bestandsindeling", "CAD", "Openen", "Maken"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over DWG-bestandsindelingen en API's die DWG-bestanden kunnen maken en openen.",
  "title" :"DWG-bestandsindeling",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een DWG-bestand?

Bestanden met de DWG-extensie vertegenwoordigen eigen binaire bestanden die worden gebruikt voor het bevatten van 2D- en 3D-ontwerpgegevens. Net als DXF, wat ASCII-bestanden zijn, vertegenwoordigt DWG het binaire bestandsformaat voor CAD-tekeningen (Computer Aided Design). Het bevat vectorafbeeldingen en metadata voor de weergave van de inhoud van CAD-bestanden. Er zijn gratis viewers beschikbaar voor het bekijken van DWG-bestanden op het Windows-besturingssysteem, zoals de gratis DWG TrueView van Autodesk. Er zijn ook andere toepassingen van derden die het bereiken van DWG-bestanden ondersteunen. DWG-bestanden bevatten door de gebruiker gemaakte informatie en omvatten:

* Ontwerpen
* Geometrische gegevens
* Kaarten en foto's

Dit formaat wordt veel gebruikt door architecten, ingenieurs en ontwerpers voor verschillende ontwerpdoeleinden.

## Korte geschiedenis ##

Het DWG-bestandsformaat is in de loop van de tijd geëvolueerd sinds de formele introductie in 1982. Een kort overzicht van de gebeurtenissen in het verleden vanuit historisch perspectief is als volgt.

**1982:** Autodesk heeft het DWG-bestandsformaat, dat in 1970 door Mike Riddle is ontwikkeld, in licentie gegeven als basis voor AutoCAD.

**1998:** Met de release van AutoCAD R14.01 heeft Autodesk bestandsverificatie toegevoegd via een functie genaamd DWGCHECK die een versleutelde controlesom en productcode, door Autodesk WaterMark genoemd, ingesloten in DWG-bestanden die door het programma zijn gemaakt.

**2006:** Autodesk heeft AutoCAD 2007 aangepast om "TrustedDWG-technologie" op te nemen om de tekstreeks "Autodesk DWG. Dit bestand is een vertrouwde DWG die het laatst is opgeslagen door een Autodesk-toepassing of een door Autodesk gelicentieerde toepassing" in de DWG-bestanden in te sluiten. Het doel hiervan was om gebruikers van Autodesk-software te helpen ervoor te zorgen dat deze bestanden zijn gemaakt door een Autodesk- of RealDWG-toepassing, wat zeker zou moeten helpen bij het verminderen van het risico op incompatibiliteit.

## Bestandsstructuur ##

DWG is een van de meest gebruikte bestandsindelingen door een reeks toepassingen en heeft een robuuste bestandsstructuur. Aangezien DWG een binair bestandsformaat is, is het niet leesbaar voor mensen zoals het gewone ASCII [DXF](/nl/cad/dxf/) bestandsformaat. DWG-bestanden bevatten meestal informatie over de afbeeldingscoördinaten en alle bijbehorende metadata. Volledige [specificaties](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) van het DWG-bestandsformaat kunnen worden gedownload door OpenDesign. De bestandsstructuur van het DWG-bestandsformaat is als volgt samengevat.

**Header**: de bestandsheader bestaat uit DWG-headervariabelen en informatie over Cyclic Redundancy Check (CRC) die wordt gebruikt voor de foutdetectie. Elke subsectie is een gespecialiseerde vector waarin verschillende lengtes van bits worden gebruikt om verschillende labels weer te geven. De eerste 6 bits van de DWG Header-variabele staan bijvoorbeeld voor de versietekenreeks.

**Klassedefinities:** Een DWG-bestand kan verschillende klassen bevatten, afhankelijk van het specifieke doel van het .dwg-bestand. Informatie zoals klassemetadata, grootte van klassegegevensgebied, klassenummer en controlesom naast andere.

**Sjabloon**: dit is optioneel en voor R15- en R15-versies bevindt dit gedeelte zich onder het gedeelte Vrije ruimte voor objecten.

**Opvulling**: de metadata wordt voorzien van een suffix en een postfix met een specifiek aantal bytes, waardoor de oudere AutoCAD-softwareversies compatibel zijn met het nieuwe DWG-bestandsformaat.

**Afbeeldingsgegevens**: de metagegevens voor deze sectie zijn afhankelijk van het specifieke .dwg-type. Voor R14- en R15-gebruikers is dit gedeelte optioneel.

**Objectgegevens**: de objectgegevens bestaan uit een volledige lijst met tabelentiteiten, woordenboekitems, enz. die overeenkomen met de bestaande lijst met objecten.

**Objectmap**: de locatie van elk object in het bestand wordt gespecificeerd in dit gedeelte van het bestand. De meeste metagegevens in deze sectie zijn bestandshandvatten die een rol spelen bij de identificatie en opnieuw weergeven van het object.

**Object vrije ruimte**: deze sectie is optioneel voor alle gebruikers

**Tweede kop**: een duplicaat van de bestandskoptekst aan het einde van het DWG-bestand

## Referenties ##

* [specificaties DWG-bestandsindeling](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [De DWG-bestandsspecificatie](https://www.scan2cad.com/dwg/file-spec/)
* [DWG - Door Wikipedia](https://en.wikipedia.org/wiki/.dwg)


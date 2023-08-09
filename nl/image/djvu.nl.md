{
  "date" : "2019-10-11",
  "keywords" :[ "djvu-bestand", "djvu-bestandsformaat", "wat is een djvu-bestand", "bestand", "djvu-voorbeeld", "djvu-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DJVU-bestandsindeling",
  "description":"Meer informatie over DJVU-bestandsindeling en API's die DJVU-bestanden kunnen maken en openen.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een DJVU-bestand?

DjVu, uitgesproken als "déjà vu", is een grafisch bestandsformaat bedoeld voor gescande documenten en boeken, met name die welke de combinatie van tekst, tekeningen, afbeeldingen en foto's bevatten. Het is ontwikkeld door AT&T Labs. Het maakt gebruik van meerdere technieken, zoals scheiding van tekst- en achtergrondafbeeldingen in beeldlagen, progressief laden, rekenkundige codering en compressie met verlies voor bitonale afbeeldingen. Omdat het DJVU-bestand gecomprimeerde maar hoogwaardige kleurenafbeeldingen, foto's, tekst en tekeningen kan bevatten en daarom in minder ruimte kan worden opgeslagen, wordt het op internet gebruikt als eBooks, handleidingen, kranten, oude documenten, enz.

DjVu kan worden beoordeeld als superieur alternatief voor [PDF](/nl/pdf/). Bestandsextensies die aan DjVu zijn gekoppeld, zijn .DJVU of .DJV. DjVu kan compressieverhoudingen bereiken die ongeveer 5 – 10 beter zijn dan bestaande methoden zoals [JPEG](/nl/image/jpeg/) & [GIF](/nl/image/gif/) voor kleurendocumenten en 3 – 8 keer beter dan [TIFF]( /image/tiff/) in zwart-wit documenten. Gescande documenten met 300 DPI met full colour tot 25 MB kunnen worden gecomprimeerd tot 30 tot 100 KB. Op dezelfde manier kunnen zwart-witdocumenten worden gecomprimeerd tot 5 tot 30 KB. De gemiddelde HTML-pagina kan tot 50 KB zijn, daarom kunnen deze documenten zonder problemen op het net worden geüpload.

## Korte geschiedenis ##

De DjVu-technologie is ontwikkeld in AT&T-labs door [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner en Paul G van 1996 tot 2001. Het DjVu-bestandsformaat heeft verschillende revisies ondergaan, waarvan de meest recente uit 2005.


|Versie|Releasedatum|Opmerkingen
---|---|---|
|1–19|1996–1999|Dit zijn de ontwikkelingsversies.
|20|April 1999|Enkele pagina is gewijzigd in Multipage formaat.
|23|Juli 2002|CID chunk
|24|Februari 2003|LTAnno chunk
|21|September 1999|Indirect opslagformaat vervangen. Tekst zoeklaag is toegevoegd.
|22|April 2001|Paginaoriëntatie, kleur JB2
|25|Mei 2003|NAVM-brok. Ondersteuning voor DjVu-bladwijzers is toegevoegd.
|26|April 2005|Tekst/regel-annotaties

## DjVu-bestandsindeling ##

DjVu-documenten zijn IFF85-bestanden. De structuur biedt een hiërarchie van containers die informatie bevatten in een DjVu-bestand. Deze containers worden ook wel “Chunks” genoemd. Chunk type en Chunk ID beschrijven hoe de chunk wordt gebruikt. Er is een header van 4 bytes gevolgd door een IFF-structuur. De eerste vier bytes van een DjVu-bestand zijn 0x41 0x54 0x26 0x54. Deze sectie bespreekt de verschillende soorten DjVu-documenten en de bijbehorende brokken waaruit ze bestaan.


|Chunk-ID|Gebruik
---|---|
|FORM|De samengestelde chunk met de eerste vier databytes van de FORM chunk die een secundaire identifier zijn.
|FORM:DJVM|Een DjVu-document met meerdere pagina's. Samengestelde brok die de DIRM-brok bevat.
|FORM:DJVU|Eén pagina DjVu-document. Samengestelde chunk die de chunks bevat waaruit een pagina in een djvu-document bestaat.
|FORM:DJVI|Een “gedeeld” DjVu-bestand dat is opgenomen via de INCL-chunk. Gedeelde annotaties en vormenwoordenboek.
|FORM:THUM|Samengestelde chunk die de TH44 chunks bevat die de ingebedde thumbnails zijn.
|DIRM|Paginanaaminformatie voor documenten met meerdere pagina's.
|NAVM|Bladwijzerinformatie
|ANTa, ANTz|Annotaties inclusief zowel initiële weergave-instellingen als overlay-hyperlinks, tekstvakken, enz.
|TXTa, TXtz|Unicode Tekst en lay-outinformatie.
|Djbz|Gedeelde vormtafel.
|Sjbz|BZZ gecomprimeerde JB2-bitonale gegevens die worden gebruikt om masker op te slaan.
|FG44|IW44-gegevens gebruikt om voorgrond op te slaan
|BG44|IW44-gegevens gebruikt om achtergrond op te slaan
|TH44|IW44-gegevens die worden gebruikt om ingebedde miniatuurafbeeldingen op te slaan
|WMRM|JB2-gegevens vereist om een watermerk te verwijderen
|FGbz|Kleur JB2-gegevens. Geeft een kleur voor elke (blit of vorm?) in de corresponderende Sjbz-chunk.
|INFO|Informatie over de a DjVu-pagina
|INCL|De ID van een opgenomen FORM:DJVI-chunk.
|BGjp|JPEG-gecodeerde achtergrond
|FGjp|JPEG-gecodeerde voorgrond
|Smmr|G4 gecodeerd masker

### DJVU-compressie

Een enkele afbeelding is verdeeld in veel verschillende afbeeldingen en vervolgens wordt elke afbeelding afzonderlijk gecomprimeerd. Voor het maken van een DjVu-bestand wordt de afbeelding eerst gescheiden in drie afbeeldingen, een achtergrond, voorgrond en een maskerafbeelding. Meestal zijn de achtergrond- en voorgrondafbeeldingen kleurenafbeeldingen met een lagere resolutie; maar de maskerafbeelding is een afbeelding met een hogere resolutie en meestal wordt de tekst daar opgeslagen. Na de scheiding worden de voorgrond- en achtergrondafbeeldingen gecomprimeerd via een op wavelet gebaseerd compressiealgoritme IW44, terwijl de maskerafbeelding wordt gecomprimeerd met een andere methode, JB2 genaamd.

De JB2-coderingsmethode elimineert een groot deel van de redundantie in de tekstafbeelding door identieke vormen op de pagina te identificeren, zoals meerdere keren dat een teken in een bepaald lettertype voorkomt. JB2 codeert eerst de bitmap van elke unieke vorm door gebruik te maken van de redundantie tussen vergelijkbare vormen. Vervolgens codeert het de locaties waar elke vorm op de pagina verschijnt. Zowel JB2 als IW44 vertrouwen op een nieuw type adaptieve binaire rekenkundige coder, de ZP-coder genaamd, die de resterende redundantie binnen een paar procent van de Shannon-limiet perst. De ZP-coder is adaptief en sneller dan andere benaderende binaire rekenkundige coders.

## Referenties ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [DjVu-bestandsindeling](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)


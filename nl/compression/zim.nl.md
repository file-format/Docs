{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIM-bestandsindeling - OpenZIM-archiefbestand",
  "description":"Meer informatie over ZIM-bestandsindeling en API's die ZIM-bestanden kunnen maken en openen.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Wat is een ZIM-bestand? ##

Bestanden met de extensie .zim zijn archieven die zijn gemaakt om Wiki-inhoud offline op te slaan. Het wordt beschouwd als het meest geschikte open bestandsformaat om Wikipedia op een USB op te slaan. Het slaat de inhoud van de site op in een compact formaat. De naam komt van "Zeno IMproved", het eerdere Zeno-bestandsformaat. ZIM wordt onderhouden door [openZIM ](https://openzim.org/)project dat wordt gesponsord door Wikimedia CH en ondersteund door de Wikimedia Foundation. ZIM-bestanden kunnen worden geopend door toepassingen zoals Kiwix en ZIMReader. Het OpenZIM-project heeft de implementatie van het ZIM-bestandsformaat op [Github](https://github.com/openzim) gehost voor bijdragen van de OpenSource-gemeenschap.

## Specificaties ZIM-bestandsindeling

Het ZIM-bestandsformaat is ontwikkeld bovenop [Zeno-bestandsformaat](https://openzim.org/wiki/Zeno_file_format) en is niet achterwaarts compatibel. De formaatspecificaties van het ZIM-bestandsformaat zijn [online beschikbaar](https://openzim.org/wiki/ZIM_file_format) door openZIM ter referentie van de ontwikkelaar. OpenZIM heeft C++ open source implementatie geleverd, [LibZim](https://openzim.org/wiki/Zimlib), voor het lezen en schrijven van ZIM-bestanden.

Het ZIM-bestandsformaat gebruikt LZMA2-compressie om de inhoud compact te maken.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM-bestandsindeling" >}}


### ZIM-koptekst

Een ZIM-bestand begint met een header die op offset 0 staat. Alle bestanddelen zijn gebaseerd op little-endian en alle gehele getallen zijn gehele getallen zonder teken, dwz uint_16, uint_32, uint_64.

|Veldnaam |Type| Offset| Lengte| Beschrijving|
---|---|---|---|---|
|magicNumber| geheel getal| 0| 4| Magisch getal om het bestandsformaat te herkennen, moet 72173914 (0x44D495A)| . zijn
|majorVersie| geheel getal| 4| 2| Hoofdversie van het ZIM-bestandsformaat (5 of 6)|
|minorVersie| geheel getal| 6| 2| Kleine versie van het ZIM-bestandsformaat|
|uuid| geheel getal| 8| 16| unieke id van dit zim-bestand|
|articleCount| geheel getal| 24| 4| totaal aantal artikelen|
|clusterCount| geheel getal| 28| 4| totaal aantal clusters|
|urlPtrPos| geheel getal| 32| 8| positie van de directory-pointerlijst geordend op URL|
|titlePtrPos| geheel getal| 40| 8| positie van de directory pointerlist geordend op Titel|
|clusterPtrPos| geheel getal| 48| 8| positie van de lijst met clusteraanwijzers|
|mimeListPos| geheel getal| 56| 8| positie van de MIME-typelijst (ook kopgrootte)|
|mainPage| geheel getal| 64| 4| hoofdpagina of 0xffffffff als er geen hoofdpagina|
|layoutPagina| geheel getal| 68| 4| lay-outpagina of 0xffffffffff als er geen lay-outpagina is|
|checksumPos| geheel getal| 72| 8| pointer naar de md5checksum van dit bestand zonder de checksum zelf. Dit wijst altijd 16 bytes voor het einde van het bestand.|

## Referenties ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)


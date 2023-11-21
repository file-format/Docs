{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO-bestand - Unix CPIO-archiefbestandsformaat",
  "description":"Leer wat een CPIO-bestand is en wat de API's zijn die CPIO-bestanden kunnen maken en openen.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Wat is een CPIO-bestand?

Een CPIO-bestand is een archiefbestand gemaakt in Unix's Copy In Copy Out (CPIO) -formaat. Het is vergelijkbaar met het TAR-bestandsformaat, behalve dat het niet-gecomprimeerd is. CPIO-bestanden kunnen apparaatbestanden, symbolische koppelingen en uitgebreide bestandskenmerken opslaan.

## CPIO-bestandsindeling

Een CPIO-archief wordt gemaakt als een binair bestand dat niet voor mensen leesbaar is. Het slaat de verzameling bestanden en mappen op. De inhoud van een CPIO-archief wordt geïdentificeerd met metadata-informatie zoals bestandsnamen, machtigingen, eigendom en tijdstempels. Deze metadata-informatie wordt ook opgeslagen in het archiefbestand voor zijdelingse toegang door het systeem.

## Formaat van CPIO-archief

Een CPIO-bestand bestaat uit een of meer aaneengeschakelde lidbestanden. Elk bestand in het archief bestaat uit een header, eventueel gevolgd door de bestandsinhoud zoals vermeld in de header. Het archief bevat aan het einde nog een header die wordt beschreven door een leeg bestand met de naam TRAILER!!.

### Soorten CPIO-archieven

Er zijn twee soorten CPIO-archieven. Deze verschillen alleen in de stijl van de header.

* ASCII-archieven - Deze CPIO-archieven hebben een afdrukbare header die onderdeel wordt van het CPIO-archief als het archief zelf uit ASCII-bestanden bestaat
* Binaire archieven - Deze CPIO-archieven hebben binaire headers.

## Werken met CPIO-archief

### Hoe maak ik CPIO-archieven aan?

U kunt op Unix-achtige systemen een CPIO maken met behulp van de opdracht **cpio**. Met de volgende opdracht worden alle bestanden en mappen in de huidige map en de submappen ervan gevonden. Deze uitvoer wordt vervolgens doorgestuurd naar de cpio-opdracht, die een nieuw CPIO-archief genereert met de naam archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Hoe bestanden uit CPIO-archieven extraheren?

Met de volgende opdracht worden de bestanden uit een bestaand archief gehaald.

```
cpio -id < archive_cpio.cpio
```
Het leest het archive.cpio-bestand uit de standaardinvoer en extraheert de bestanden naar de huidige map.


## Referenties

* [CPIO - Door Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [CPIO-bestandsindeling](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)


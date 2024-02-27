{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ISO - Disk Image File Format",
  "description":"Hvad er en ISO-fil og API'er, der kan oprette og åbne ISO-filer.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso-da",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Hvad er en ISO-fil?

En fil med filtypenavnet .iso er en ukomprimeret arkivdiskbilledfil, der repræsenterer indholdet af hele data på en optisk disk såsom cd eller dvd. Baseret på [ISO-9660](https://www.iso.org/standard/17505.html)-standarden indeholder ISO-billedfilformatet diskdataene sammen med filsystemoplysningerne, der er gemt i det. Evnen til ISO-filer til at indeholde en nøjagtig kopi af indholdet gør den til den perfekte filtype til at lave kopier af cd'er/dvd'er og bruges mest til at gemme opstartsdata til installation. De fleste gange brændes ISO-filer til USB/CD/DVD som opstartbart indhold til opstart af maskinen til installation. ISO-filer har MIME-typen application/x-iso9660-image.

## ISO filformat

ISO-filformat er ikke som andre containerfilformater, selvom det arkiverer det angivne indhold af data. Arkivet oprettes som en binær fil med den nøjagtige struktur af indholdet og filsysteminformationen. ISO-filformatet er beskrevet af [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) som følger.

### Struktur på øverste niveau af ISO-fil

Filens overordnede struktur består af:

 * `System Area` - 32.768 bytes og er ubrugt af ISO_9660
 * Dataområde' - består af volumenbeskrivelsessæt og stitabeller, mapper og filer

### Volume Descriptor Set

Dataområdet starter med volumendeskriptorsættet, et sæt af en eller flere volumendeskriptorer, der afsluttes med en volumendeskriptorsætterminator. Disse fungerer samlet som en header for dataområdet, der beskriver dets indhold (svarende til BIOS-parameterblokken, der bruges af FAT-, HPFS- og NTFS-formaterede diske).

Et volumenbeskrivelsessæt er som vist nedenfor.

|Volume Descriptor Set|
---|
|Lydstyrkebeskrivelse #1|
|...|
|Lydstyrkebeskrivelse #N|
|Lydstyrkebeskrivelse sæt terminator|

#### Volume Descriptor

Hver volumenbeskrivelse er 2048 bytes stor og har følgende struktur:

|Del |Type |Identifier |Version |Data|
---|---|---|---|---|
|Størrelse |1 byte |5 bytes (altid 'CD001') |1 byte (altid 0x01) |2.041 bytes|

## Referencer

* [Optisk diskbillede - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)

* [Filsignaturer](https://www.garykessler.net/library/file_sigs.html)

* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)



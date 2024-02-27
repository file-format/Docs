{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CPIO-fil - Unix CPIO-arkivfilformat",
  "description":"Lær at vide, hvad en CPIO-fil og API'er er, der kan oprette og åbne CPIO-filer.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio-da",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Hvad er en CPIO fil?

En CPIO-fil er en arkivfil, der er oprettet i Unix's Copy In Copy Out-format (CPIO). Det ligner TAR-filformatet, bortset fra at det er ukomprimeret. CPIO-filer kan gemme enhedsfiler, symbolske links og udvidede filattributter.

## CPIO filformat

Et CPIO-arkiv oprettes som en binær fil, der ikke kan læses af mennesker. Det gemmer samlingen af filer og mapper. Indholdet af et CPIO-arkiv identificeres med metadataoplysninger såsom filnavne, tilladelser, ejerskab og tidsstempler. Disse metadataoplysninger gemmes også i arkivfilen, så systemet kan få adgang til siden.

## Format af CPIO-arkiv

En CPIO-fil består af en eller flere sammenkædede medlemsfiler. Hver fil i arkivet består af en header eventuelt efterfulgt af filindhold som nævnt i headeren. Arkivet indeholder en anden header i slutningen, der er beskrevet af en tom fil ved navn TRAILER!!.

### Typer af CPIO-arkiver

Der er to typer CPIO-arkiver. Disse forskellige kun i stil med overskriften.

* ASCII-arkiver - Disse CPIO-arkiver har en printbar header, der bliver en del af CPIO-arkivet, hvis selve arkivet består af ASCII-filer

* Binære arkiver - Disse CPIO-arkiver har binære overskrifter.


## Arbejder med CPIO Archive

### Hvordan oprettes CPIO-arkiver?

Du kan oprette en CPIO på Unix-lignende systemer ved hjælp af kommandoen **cpio**. Den følgende kommando finder alle filer og mapper i den aktuelle mappe og dens undermapper. Dette output sendes derefter til cpio-kommandoen, der vil generere et nyt CPIO-arkiv med navnet archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Hvordan udtrækkes filer fra CPIO-arkiver?

Følgende kommando udpakker filerne fra et eksisterende arkiv.

```
cpio -id < archive_cpio.cpio
```
Den vil læse filen archive.cpio fra standardinput og udpakke filerne til den aktuelle mappe.


## Referencer

* [CPIO - af Wikipedia](https://en.wikipedia.org/wiki/Cpio)

* [CPIO File Format](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)


{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SHSH-fil - iPhone/iPod Touch SHSH Blob-filformat",
  "description":"Lær om, hvad en SHSH-fil er.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh-da",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Hvad er en SHSH fil?

En SHSH-fil, også kendt som en Signature HaSH, er en digital signatur, der bruges af Apple til at autentificere og verificere firmwareopdateringer til iOS-enheder såsom iPhones, iPads og iPods.

## Forskellen mellem SHSH og SHSH2 filformater

Ligesom en SHSH2-fil indeholder SHSH-filen en unik identifikator for enheden kaldet et ECID (Exclusive Chip ID), samt oplysninger om firmwareversionen installeret på enheden. Dog blev SHSH-filer brugt i ældre versioner af iOS (før iOS 10) og er siden blevet erstattet af SHSH2-filer.

## SHSH-filformat - flere oplysninger

SHSH-filer gemmes på disk i binært filformat. De interne filstrukturdetaljer for dette filformat er ikke offentligt tilgængelige.

SHSH-filer er vigtige for brugere, der ønsker at nedgradere deres enheds firmware til en tidligere version, der ikke længere er underskrevet af Apple. Ved at gemme SHSH-filerne til en specifik firmwareversion, når den stadig signeres af Apple, kan brugere senere bruge dem til at omgå Apples signaturbekræftelse og installere den firmwareversion på deres enhed. Denne proces er også kendt som jailbreaking.

## Referencer

* [SHSH Blob - Af Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)

* [TSS Saver](https://tsssaver.1conan.com/v2/)



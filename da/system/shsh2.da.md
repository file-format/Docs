{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SHSH2-fil - iOS SHSH Blob-filformat",
  "description":"Lær om, hvad en SHSH2-fil er.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2-da",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Hvad er en SHSH2 fil?

En SHSH2-fil, også kendt som en SHSH-blob eller ECID SHSH, er en digital signatur, der bruges af Apple til at autentificere og verificere firmwareopdateringer til iOS-enheder såsom iPhones, iPads og iPods. Den indeholder en unik identifikator for enheden, der er kendt som ECID (Exclusive Chip ID). Den indeholder også oplysninger om den firmwareversion, der er installeret på enheden.

## SHSH2 filformat - flere oplysninger

SHSH2-filer gemmes på disk i binært filformat, og de interne filstrukturdetaljer for dette filformat er ikke offentligt tilgængelige.

Når en ny version af iOS er installeret på en Apple-enhed som iPhone, iPad eller Mac, genereres en SHSH2-fil. Denne SHSH2-fil sendes til Apple-servere, som læser og verificerer denne digitale signaturfil. Baseret på disse oplysninger tillader eller forhindrer serveren installationen.

Det samme sker, når der anmodes om en opdatering. Når en bruger anmoder om en opdatering eller gendannelse af deres enhed via iTunes eller en anden software, vil Apples servere kontrollere, at SHSH2-filen matcher enhedens ECID og firmwareversion, før opdateringen tillades at fortsætte.

## Referencer

* [SHSH Blob - Af Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)

* [TSS Saver](https://tsssaver.1conan.com/v2/)



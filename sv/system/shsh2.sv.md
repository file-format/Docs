{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2-fil - iOS SHSH Blob-filformat",
  "description":"Läs mer om vad en SHSH2-fil är.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Vad är en SHSH2 fil?

En SHSH2-fil, även känd som en SHSH-blob eller ECID SHSH, är en digital signatur som används av Apple för att autentisera och verifiera firmwareuppdateringar för iOS-enheter som iPhones, iPads och iPods. Den innehåller en unik identifierare för enheten som är känd som ECID (Exclusive Chip ID). Den innehåller också information om den firmwareversion som är installerad på enheten.

## SHSH2 filformat - Mer information

SHSH2-filer sparas på skiva i binärt filformat och de interna filstrukturdetaljerna för detta filformat är inte tillgängliga offentligt.

När en ny version av iOS installeras på en Apple-enhet som iPhone, iPad eller Mac, genereras en SHSH2-fil. Denna SHSH2-fil skickas till Apple-servrar som läser och verifierar denna digitala signaturfil. Baserat på denna information tillåter eller förhindrar servern installationen.

Detsamma händer när en uppdatering begärs. När en användare begär en uppdatering eller återställning av sin enhet via iTunes eller annan programvara kommer Apples servrar att kontrollera att SHSH2-filen matchar enhetens ECID och firmware-version innan uppdateringen fortsätter.

## Referenser

* [SHSH Blob - Av Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)


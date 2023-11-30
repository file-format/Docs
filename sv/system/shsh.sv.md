{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH-fil - iPhone/iPod Touch SHSH Blob-filformat",
  "description":"Läs mer om vad en SHSH-fil är.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Vad är en SHSH fil?

En SHSH-fil, även känd som Signature HaSH, är en digital signatur som används av Apple för att autentisera och verifiera firmwareuppdateringar för iOS-enheter som iPhones, iPads och iPods.

## Skillnaden mellan SHSH och SHSH2 filformat

Liksom en SHSH2-fil innehåller SHSH-filen en unik identifierare för enheten som kallas "ECID" (Exclusive Chip ID), samt information om den fasta programvaran som är installerad på enheten. Men SHSH-filer användes i äldre versioner av iOS (före iOS 10) och har sedan ersatts av SHSH2-filer.

## SHSH-filformat - Mer information

SHSH-filer sparas på skiva i binärt filformat. De interna filstrukturdetaljerna för detta filformat är inte tillgängliga offentligt.

SHSH-filer är viktiga för användare som vill nedgradera enhetens firmware till en tidigare version som inte längre signeras av Apple. Genom att spara SHSH-filerna för en specifik firmwareversion när den fortfarande signeras av Apple kan användare senare använda dem för att kringgå Apples signaturverifiering och installera den firmwareversionen på sin enhet. Denna process är också känd som "jailbreaking".

## Referenser

* [SHSH Blob - Av Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)


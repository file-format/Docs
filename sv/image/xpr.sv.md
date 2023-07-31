{
  "date" : "2022-03-21",
  "keywords" :[ "xpr-fil", "xpr-filformat", "vad är en xpr-fil", "fil", "xpr-exempel", "xpr-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPR-filformat - Microsoft Expression Design Graphic File",
  "description":"Läs mer om XPR-filformat och API:er som kan skapa och öppna XPR-filer.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## Vad är XPR fil?

En XPR-fil är en vektorbildsfil som skapats med programvaran Microsoft Expression Graphics (EGD) som nu har utgått. Den innehåller grafikinformation som kan användas som användargränssnittsmockup. XPR-filer ersattes senare av .design-filer i Microsoft Expression Design. XPR-filer kan öppnas med Microsoft Expression Studio som har upphört ett tag nu.

## Sårbarhet i XPR-filformat

XPR-filer identifierades för att gynna en sårbarhet i Microsoft Expression Design, vilket leder till att fjärrkod kan köras. I det rapporterade problemet, om en användare öppnade en legitim .xpr-fil som är belagd i nätverkskatalogen tillsammans med DLL-filen (dynamic link library), kunde Microsoft Expression Design försöka ladda DLL-filen och exekvera koden den innehöll. Detta fixades senare av Microsoft i en säkerhetsuppdatering.

## Referenser

* [Sårbarhet i uttrycksdesign kan tillåta fjärrexekvering av kod (2651018)](https://learn.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)


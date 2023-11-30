{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om 4DL-filformat och API:er som kan skapa och öppna 4DL-filer.",
  "title" :"4DL - 4th Dimension Database Log File",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## Vad är en 4DL fil?

En 4DL-loggfil används för att registrera ändringar som gjorts i en 4D-databasfil (.4DD). Denna fil lagras bredvid databasfilen och delar ett liknande filnamn. Dess syfte är att noggrant spåra och upprätthålla en omfattande register över de uppdateringar som implementerats i databasen. En [4DD-fil](/sv/database/4dd/), jämfört med 4DL-filen, är huvudsakligen associerad med 4:e dimensionerna av 4D Inc.

## 4DL-filformat - Mer information

Vanligtvis lagras flera 4DL-filer tillsammans med en 4DD-fil. Således kan den första versionen av loggfilen heta 0001.4dl, men de laterala versionerna av loggfilerna kommer att sparas som 0002.4dl, 0003.4dl, och så vidare. Nu, om själva loggfilen genomgår 3 efterföljande sparar, kommer den att märkas som "db1[0005-0003].4dl."

## Referenser

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))

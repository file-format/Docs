{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDMP-fil - Windows Heap Dump-filformat",
  "description":"Läs mer om HDMP-filformat och API:er som kan skapa och öppna HDMP-filer.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Vad är en HDMP fil?

HDMP-fil är en okomprimerad minnesdump när ett program eller program kraschar på grund av ett fel. Den skapas endast av Windows XP/Vista och innehåller en dump av programmets status när den kraschade. Eftersom de är okomprimerade tar HDMP-filerna mer utrymme på skivan jämfört med Minidump [MDMP](/sv/system/mdmp/)-filerna som komprimeras för rapporteringsändamål.

Applikationer som kan användas för att **öppna** eller analysera HDMP-filer inkluderar Microsoft Visual Studio med felsökningsverktyg för Windows.

## HDMP filformat

HDMP-filer lagras på skiva som binära filer och ger ingen fördel om de öppnas utan lämpliga applikationer. Dessa innehåller relevanta systemdata som registrerats när felet inträffade.

### Skillnad mellan HDMP och MDMP filformat

HDMP är okomprimerade minnesdumpfiler. Däremot är MDMP minidumpfiler som komprimeras för att minska filstorleken och skickas till Microsoft för att rapportera problemet.

## Referens ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


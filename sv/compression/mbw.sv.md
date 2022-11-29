{
  "date" : "2021-05-28",
  "keywords" :[ "MBW", "MBRWizard", "fil", "format", "tillägg", "komprimerad", "Firesage Solutions" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBW filformat",
  "description":"Läs mer om MBW-filformat och API:er som kan skapa och öppna MBW-filer.",
  "linktitle" : "MBW",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-05-28"
}

## Vad är MBW fil? ##

En fil med filändelsen .mbw är i första hand associerad med MBRWizard av Firesage Solutions. Master Boot Record Wizard (MBRWizard) säkerhetskopierar din dators MBR och sparar den till en MBW-fil som kan återställas vid behov. Förutom MBR- och VBR-kopior (Volume Boot Record) kan dessa filer innehålla GPT, användardefinierade sektorer eller hela diskavbildningar. MBR är en viktig, 512-byte lång skiva på din hårddisk som gör att ditt operativsystem kan starta. Den kan också innehålla partitionstabellen och en 32-bitars signatur som identifierar diskmediet.

## Operativsystem som stöds ##

MPW-filformatet stöds endast av Windows-operativsystemet.

## Möjliga problem när du öppnar filen ##

Om du inte kan öppna och köra filen MBW kan det finnas ett av följande möjliga problem:

* Korrupt MBW-fil
* Fel länkar till MBW-filen i registerposter
* Raderad beskrivning av MBW från Windows-registret
* En infekterad fil med en oönskad skadlig kod
* Datorn har inte tillräckliga hårdvaruresurser för att hantera MBW-filen
* Drivrutiner som används av datorn för att öppna en MBW-fil är föråldrade


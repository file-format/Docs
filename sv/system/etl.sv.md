{
  "date" : "2022-02-22",
  "keywords" :[ "ETL", "tillägg", "fil", "format", "system", "drivrutin", "Windows enhetsdrivrutin", "program", "dator", "applikation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ETL-filer - Microsoft Event Trace Log File",
  "description":"Läs mer om ETL-filformat och API:er som kan skapa och öppna ETL-filer.",
  "linktitle" : "ETL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-02-22"
}

## Vad är ETL fil?

ETL-filer är loggfiler som innehåller händelseloggar genererade av Microsoft Operating System Kernel. Dessa loggfiler inkluderar program- och systemnivåfel, varningar och andra händelsedata. ETL-filer är användbara för att analysera och felsöka problem på systemnivå. Vanliga problem som registreras i ETL-filer inkluderar de som genereras av diskåtkomster och sidfel. Microsoft tillhandahåller två applikationer, Tracerpt och Event Viewer för att läsa och visa innehållet i ETL-filer. ETL-filer kan konverteras till andra filformat som [TXT](/sv/ordbehandling/txt/) och [CSV](/sv/spreadsheet/csv/) med hjälp av Tracerpt.

## ETL filformat

ETL-filer sparas på skiva i komprimerat binärt format för att minska diskutrymmet.

## Öppna ETL-filer med Windows Performance Analyzer

ETL-fildata kan läsas och visualiseras i såväl tabell- som grafiskt format med hjälp av Microsoft Windows Performance Analyzer (WPA)-applikationen. Guiden [Öppna och analysera ETL-filer](https://docs.microsoft.com/en-us/windows-hardware/test/wpt/opening-and-analyzing-etl-files-in-wpa) ger information om hur du arbetar med ETL-filer.

## Referenser

* [Windows Performance Analyzer](https://docs.microsoft.com/en-us/windows-hardware/test/wpt/getting-started--windows-performance-analyzer--wpa-)
* [WPA Quick Start Guide](https://docs.microsoft.com/en-us/windows-hardware/test/wpt/wpa-quick-start-guide)


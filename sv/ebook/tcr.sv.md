{
  "date" : "2021-03-09",
  "keywords" :[ "TCR", "Psion", "tillägg", "format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig mer om TCR-filformat för Psion 3-serien och API:er som kan skapa och öppna tcr-filer.",
  "title" :"TCR - Psion Series 3 eBook File",
  "linktitle" : "TCR",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-09"
}

## Vad är en TCR fil?

I början av 90-talet introducerades TCR-filformatet för de gamla **Psion Series 3** handdatorerna. Företaget använde sin plattformsspecifika komprimering och detta format har mycket begränsat stöd för textformatering. Det är ett ZVR-baserat filformat och ger en jämförelsevis bättre komprimeringshastighet än PalmDOC. Det fungerar också mycket bra med FontMachine. Även om TCR-filformatet tillhör en utgående enhet, kan detta filformat fortfarande läsas med hjälp av vissa e-läsare. Detta filformat kan även ses på ett skrivbord med Sumatra PDF och med applikationen Caliber i Windows och Linux.

## Tekniska detaljer

Eftersom TCR-filformatet är baserat på en ZVR-kompressor som kan reducera många filer med cirka 50% av deras ursprungliga storlek. Kompressionsschemat som används av over är lite gammalt. Den komprimerade filen börjar med en ordbok över de 256 möjliga symbolerna som kan visas i den komprimerade filen. Ordboken innehåller en fast alternativ sträng för var och en av dessa symboler. Dekomprimeringen har blivit väldigt snabb även i OPL, och den kan börja när som helst i den komprimerade filen.

## Problem med att öppna en TCR-fil ##

Om du inte kan öppna och köra filen TCR; det betyder inte att du inte har lämplig programvara installerad på din enhet. Det kan finnas andra problem som gör att filen inte fungerar korrekt. De möjliga problemen kan vara något av följande:

- Korruption av en TCR-fil.
- Fel länkar till TCR-filen i registerposter.
- Raderad beskrivning av TCR från Windows-registret
- Skadad installation av en applikation som stöder TCR-formatet
- En infekterad TCR-fil med oönskad skadlig kod.
- Datorn har inte tillräckliga hårdvaruresurser för att hantera filen TCR.
- Drivrutiner som används av datorn för att öppna en TCR-fil är föråldrade.




## Referenser

* [TCR - By MobileRead](https://wiki.mobileread.com/wiki/TCR)
* [ZVR Compressed Text File Reader](https://iay.org.uk/zvr/)


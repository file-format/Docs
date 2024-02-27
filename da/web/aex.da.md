{
  "date": "2019-10-11",
  "keywords": [
"aex",
"aex-fil",
"filformat",
"filtype",
"hvad er en aex fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AEX - Alpha Five Compiled Global Functions File",
  "description": "Lær at vide, hvad en AEX-fil og API'er er, der kan oprette og åbne AEX-filer.",
  "linktitle": "AEX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ae-dax"
}
},
  "lastmod": "2021-12-07"
}

## Hvad er en AEX fil?

En AEX-fil (med .aex-udvidelse) er en kompileret [Xbasic](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml)-fil, der indeholder kompileret programkode til globale funktioner. Det kan bruges i webapplikationer ved at kalde dem fra serversidens [.a5w](/web/a5w/) sider. AEX-filer blev indlæst og fjernet ved at kalde henholdsvis a5w_load_aex- og a5w_unload_aex-funktionerne fra A5W-filer. Men i en ny implementering indlæses disse filer i hukommelsen ved at inkludere i filen a5_application.5i. Xbasic programmeringssprog bruges af Alpha Anywhere software til udvikling af mobil- og webapplikationer.

## AEX-filformat - flere oplysninger

AEX-filer gemmes på disk i binært filformat og indeholder kompileret kode af funktioner skrevet i Xbasic. Xbasic script-kommandoudsagn bestemmer strukturen og flowet af eksekveringen, herunder udførelse eller stop af en gentagen handling, eller valg mellem to eller flere trin baseret på betingelser. [Xbasic Language Reference](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml) kan konsulteres for detaljerede oplysninger om det.

## Referencer

 * [Alpha Five](https://www.alphasoftware.com/)
 * [Alpha Five-dokumentation](https://documentation.alphasoftware.com/documentation/pages/index.html)
 * [Xbasic Guide](https://documentation.alphasoftware.com/pages/Guides/Xbasic/index.xml)


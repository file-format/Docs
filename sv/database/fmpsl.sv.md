{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om FMPSL-filformat och API:er som kan skapa och öppna FMPSL-filer.",
  "title" :"FMPSL-filformat - FileMaker Pro 12 Snapshot Link File",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Vad är en FMPSL fil?

En FMPSL-fil är en ögonblicksbildsfil av databasen skapad med FileMaker Pro 12. Den lagrar de sökta resultaten från databasen tillsammans med annan information som visuell layout och synlig information. FMPSL-filen kan användas för att återställa alla dessa data i en annan instans av FileMaker Pro-databasen. Det här filformatet introducerades i och med lanseringen av FileMaker Pro v 12. Före denna version introducerades ögonblicksbildlänkarna som FPSL-filformat i FileMaker Pro v 11. FMPSL-filer kan öppnas med programvaran FileMaker Pro Advanced. Andra filformat som stöds av FileMaker Pro inkluderar [FP5](/sv/database/fp5/), [FP7](/sv/database/fp7/) och [FMP12](/sv/database/fmp12/).

## FMPSL filformat

Den interna filformatsinformationen för FMPSL-filer är inte tillgänglig offentligt för utvecklarens referens.

### Hur sparar jag poster som FMPSL-fil?

Data från FileMaker Pro-databasen kan sparas som en ögonblicksbildlänkfil med hjälp av följande steg.

1. Sök i posterna från databasen som måste sparas som en ögonblicksbildlänkfil.
1. Använd alternativet Skicka post som ögonblicksbildlänk från menyn, spara filen genom att ange ett filnamn.
1. Använd posterna som bläddras i för att spara hela den hittade uppsättningen poster.

Den genererade ögonblicksbildsfilen kommer att sparas på skiva med det angivna namnet.

## Referenser

* [Konvertera tidigare versioner av FileMaker Pro-filformat till FMP12-filformat](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Spara poster som en ögonblicksbildlänkfil](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)


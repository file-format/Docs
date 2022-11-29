{
  "date" : "2021-08-17",
  "keywords" :[ "udf-fil", "udf-filformat", "vad är en udf-fil", "fil", "udf-exempel", "udf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om UDF-filformat och API:er som kan skapa och öppna UDF-filer.",
  "title" :"UDF - Universal Disk Format File",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Vad är en UDF fil?
Filen med filtillägget .udf är ett skivavbildningsformat som vanligtvis används för att spara filer på optiska media; kan användas för att bränna DVD-skivor, CD-skivor och andra optiska medier; lagrar en samling filer med den katalogstruktur som anges i UDF-standarden; tillåter att filer raderas och ändras på målskivan även efter att de har skrivits. Optical Storage Technology Association satte UDF-filsystemet som en standard för att bilda ett gemensamt filsystem för alla optiska medier, såsom för omskrivbara optiska medier och skrivskyddade media.

## UDF-filformat
UDF-filformatet är ett öppet leverantörsneutralt filsystem för datordatalagring för ett brett utbud av media. Det har använts ofta för DVD-skivor och nyare optiska skivformat. Vanligtvis behärskar programvaran ett UDF-filsystem i en batchprocess och skriver det till optiskt media i ett enda pass. Men när den skriver paket till omskrivbara media tillåter UDF att filer skapas, raderas och ändras på skivan som liknar ett allmänt filsystem på flyttbara media som flash-enheter eller disketter.
### UDF-specifikationer
UDF-standarden definierar följande tre filsystemvarianter:

- **Plain Build**: Detta är originalformatet som stöds i alla UDF-versioner. Det introducerades i den första versionen av standarden, detta format kan användas på alla typer av diskar som möjliggör slumpmässig läs- eller skrivåtkomst, såsom DVD+RW, hårddiskar och DVD-RAM-media.
- **VAT build**: Används specifikt för att skriva till engångsmedia. Momsen är en extra struktur på skivan som tillåter paketskrivning; det vill säga ommappning av fysiska block när filer eller annan data på skivan ändras eller raderas. För skriv-en gång-media är hela skivan virtualiserad, vilket gör skriv-en gång-naturen transparent för användaren; skivan kan behandlas på samma sätt som man skulle behandla en omskrivbar skiva.
- **Sparad (RW) build**: Används specifikt för att skriva till omskrivbara media. Den lägger till en extra spartabell för att hantera de fel som så småningom kommer att uppstå på delar av skivan som har skrivits om flera gånger. Denna tabell sparar koll på utslitna sektorer och mappar om dem till fungerande. Defekthanteringen av UDF gäller inte system som redan implementerar en annan form av defekthantering, såsom Mount Rainier (MRW) för optiska skivor, eller en diskkontroller för en hårddisk.
 




## Referenser


* [Windows Imaging Format - av Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



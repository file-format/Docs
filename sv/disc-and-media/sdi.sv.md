{
  "date" : "2021-08-13",
  "keywords" :[ "sdi-fil", "sdi-filformat", "vad är en sdi-fil", "fil", "sdi-exempel", "sdi-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om SDI-filformat och API:er som kan skapa och öppna SDI-filer.",
  "title" :"SDI - Windows System Deployment Image File",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Vad är SDI fil?
Filen med tillägget .sdi innehåller en load blob, boot blob och en del blob; används vanligtvis av Windows Embedded Studio för att skapa RAM-diskar eller startskivor för att ladda och installera Windows. SDI är en förkortning för System Deployment Image. Windows Embedded Studio är ett program som används för att skapa skivavbildningar för Windows. Egentligen innehåller det här programmet SDI File Manager-program och ett kommandoradsverktyg som heter **sdimgr.exe**, båda kan användas för att deplisera, skapa och redigera SDI-bilder.

## SDI-filformat
SDI-filformatet används ofta för att möjliggöra användningen av en virtuell disk för att starta upp ett system. Vissa versioner av Microsoft Windows aktiverar **RAM-start**, vilket är viktigt för att ladda en SDI-fil i minnet och sedan starta från den. SDI-filformatet möjliggör också för nätverksstart genom att använda PXE (Preboot Execution Environment). Den används också för bildbehandling av hårddiskar.
### SDI-filsektioner
Själva SDI-filen kan delas upp i följande sektioner:
- **Boot BLOB**: Detta innehåller själva startprogrammet, STARTROM.COM. Detta är en analog till startsektorn på en hårddisk.
- **Load BLOB**: Denna innehåller vanligtvis NTLDR och startas av boot BLOB.
- **Del BLOB**: Detta innehåller den faktiska starttiden; inkluderar också filerna boot.ini och ntdetect.com som bör finnas i rotkatalogen för körningen.
- **Disk BLOB**: Detta är en platt HDD-bild som börjar med en MBR. Den används för bildbehandling av hårddisken istället för att starta. Endast Disk BLOBs kan också monteras med Microsofts verktyg.


## Referenser

* [System Deployment Image - av Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)



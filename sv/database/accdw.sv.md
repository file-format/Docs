{
  "date" : "2021-08-30",
  "keywords" :[ "ACCDW", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om ACCDW-filformat och API:er som kan skapa och öppna ACCDW-filer.",
  "title" :"ACCDW - Microsoft Access Database Link File",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-30"
}

## Vad är en ACCDW fil?

En fil med filtillägget .accdw är en länkfil skapad med Microsoft Access och innehåller information om länken för att ladda ner en Access-databasfil, dvs. [ACCDB](/sv/database/accdb/) från SharePoint-servern. Detta låter användarna dela databasfiler som finns på distans. Genom att öppna ACCDB-filen laddas den länkade ACCDB-filen ned som en lokal kopia på användarens dator. Den nedladdade filen sparas på standardplatsen för nedladdning och kan nås genom att navigera till den. Vanligtvis laddas dessa filer ner och lagras med namnet "SiteServer.accdb" som hänvisar till klientdatabaserna.

## ACCDW-filformat - Mer information

ACCDW-filen är en XML-fil som tillhandahåller en länk till SharePoint-webbplatsen där Access-tjänsterna finns. Det är bara en genväg och kräver internetanslutning för att köra dem. I händelse av online cachelagras SharePoint lokalt för att ge möjlighet att ta den offline senare.

## Referenser

* [Nedladdad .accdw-fil](https://learn.microsoft.com/en-us/shows/)
* [Access 2016 Specifikationer](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Ladda ner .accdw-fil](https://social.technet.microsoft.com/Forums/en-US/7bf02e9e-6246-44da-9513-4cf8f2cc2fb2/downloaded-accdw-file?forum=sharepointgeneralprevious)
* [Vilket Access-filformat ska jag använda?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=en-us&rs=en-us&ad=us)


{
  "date": "2021-08-30",
  "keywords": [
"ACCDW",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om ACCDW filformat og API'er, der kan oprette og åbne ACCDW filer.",
  "title": "ACCDW - Microsoft Access Database Link File",
  "linktitle": "ACCDW",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-daw"
}
},
  "lastmod": "2021-08-30"
}

## Hvad er ACCDW fil?

En fil med filtypenavnet .accdw er en linkfil oprettet med Microsoft Access og indeholder oplysninger om linket til at downloade en Access-databasefil, dvs. [ACCDB](/database/accdb/) fra SharePoint-serveren. Dette giver brugerne mulighed for at dele databasefiler, der hostes eksternt. Åbning af ACCDW-filen downloader den linkede ACCDB-fil som en lokal kopi på brugerens computer. Den downloadede fil gemmes på standard downloadplacering og kan tilgås ved at navigere til den. Normalt downloades og gemmes disse filer med navnet SiteServer.accdb, der refererer til klientdatabaserne.

## ACCDW-filformat - flere oplysninger

ACCDW-filen er en XML-fil, der giver et link til SharePoint-webstedet, hvor Access Services er hostet. Det er kun en genvej og kræver internetforbindelse for at køre dem. I tilfælde af online cachelagres SharePoint lokalt for at give mulighed for at tage det offline senere.

## Referencer

* [Access 2016 Specifikationer](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Downloader .accdw-fil](https://social.technet.microsoft.com/Forums/en-US/7bf02e9e-6246-44da-9513-4cf8f2cc2fb2/downloaded-accdw-file)
* [Hvilket Access-filformat skal jeg bruge?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

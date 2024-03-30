{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDE", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Lär dig om ACCDE-filformat och API:er som kan skapa och öppna ACCDE-filer.",
  "title" :"ACCDE-filformat - Microsoft Access 2007-databasfil",
  "linktitle" : "ACCDE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Vad är en ACCDE fil?

En fil med filtillägget .accde är ett Microsoft Access 2007-filformat för att skapa Execute Only-databasfiler för att skydda anpassad databaskod. Den kompilerar all VBA-kod till körbar endast så att den inte kan ses eller redigeras. ACCDE-filformatet ersätter MDE-filformatet som användes av tidigare versioner av Microsoft Access. ACCDE är [ACCDB](/sv/database/accdb/)-filer i endast körbart läge och mer kompakta på grund av frånvaron av källkod. Den kompakta storleken på dessa filer förbättrar minnesanvändningen och förbättrar applikationens prestanda. ACCDE-filer kan öppnas med Microsoft Access 365.

## ACCDE filformat

Alla Microsoft Access 2007+-filer använder Jet ACE (Access-databasmotor) som använder ACCDB-filformatsfamiljen. Microsoft tillhandahåller dock inte en implementering med öppen källkod eller en detaljerad teknisk specifikation.

## Referenser

* [Hur döljer man VBA-kod för användare?](https://support.microsoft.com/en-us/office/hide-vba-code-from-users-ce6ab610-af07-4008-91e0-1ef1b796ff18)
* [MDB-verktyg](https://github.com/mdbtools/mdbtools/blob/master/HACKING)

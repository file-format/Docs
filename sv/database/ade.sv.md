{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om ADE-filformat och API:er som kan skapa och öppna ADE-filer.",
  "title" :"ADE - Access Project Extension File",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Vad är en ADE-fil?

En fil med filtillägget .ade är en Microsoft Access-projektfil som innehåller den kompilerade utdata av informationen i Microsoft Access ADP-projektfilen. Information i Access-projektfilen, annan än Visual Basic for Applications (VBA), är tillgänglig i kompilerad form i ADE-filer. Data lagras i komprimerat format i dessa filer för att minska filstorleken och förbättra prestandan i Access. Eftersom ADE är den kompilerade utdata från Access-projektfilen förblir all VBA-källkod som är en del av projektet skyddad genom att den inte tillåts vara en del av utdata. ADE-filer kan öppnas i Microsoft Access 365.

## ADE-filformat - Mer information

ADE är kompilerade Access Database-filer som lagras på skiva som binära filer. Den interna filstrukturen för dessa filer är inte känd.

ADE-filerna kan skapa problem vid öppning baserat på den version av Microsoft Access som har använts för att skapa dessa filer. Accessdatabaser som använder 64-bitarsversionen av Microsoft Access 2010 och som är kompilerade som MDE-, [ACCDE](/sv/database/accde/) eller ADE-filer måste kompileras om i Microsoft Access 2021 Service Pack 1 (SP1) för att fungerar korrekt med Access 2010 SP1. Det här problemet uppstår eftersom Access 2010 SP1 använder en nyare version av filen VBE7.dll (version 7.00.1619).

## Referenser

* [Problem med Access ADE-filer](https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Vilka åtkomstfilformat att använda](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)


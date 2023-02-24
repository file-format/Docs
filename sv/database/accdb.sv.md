{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om ACCDB-filformat och API:er som kan skapa och öppna ACCDB-filer.",
  "title" :"ACCDB-filformat - Microsoft Access 2007-databasfil",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Vad är en ACCDB fil?

En fil med filtillägget .accdb är en Microsoft Access 2007-databasfil som lagrar användardata i tabeller. Den stöder lagring
anpassade formulär, SQL-frågor och annan data. ACCDB-filer ersatte [MDB](/sv/database/mdb/)-filer efter att Microsoft bytte till XML-baserad filstruktur. ACCDB-filer kan fortfarande konverteras till MDB med gammal kompatibilitet. Men ACCDB är det allmänt använda Access-databasfilformatet nu. Microsoft stödde också ytterligare funktioner i ACCDB-format som möjlighet att lagra filbilagor, binär data och stöd för flera värden.

## ACCDB filformat

Liksom MDB finns det inga offentliga specifikationer tillgängliga för ACCDB-filformat. Microsoft stöder åtkomst till dessa filer programmässigt via Open Database Connectivity (ODBC) standard och Visual Basic for Applications (VBA).

### En insikt

En hex-dump av en enkel ACCDB-fil antyder att det finns allmänna likheter i strukturen med de senaste versionerna av föregångaren MDB Format Family. Båda filformaten använder fasta sidstorlekar på 4096 byte. En annan likhet mellan ACCDB och MDB är formen av det magiska numret, som inkluderar strängen "Standard ACE DB" för ACCDB. En version eller kompatibilitetskod finns på samma plats i båda formaten. mdbtools | HACKING-filen säger "Offset 0x14 innehåller Jet-versionen av denna databas" och den inofficiella MDB-guiden håller med. Informationen i dessa källor, i kombination med Wikipedia-posten för [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), tyder på att ett värde på 0x02 indikerar ACE 12 (Access 2007) och 0x03 indikerar ACE 14 (Access 2010). En minimal databas skapad i Access 2010 och en liknande skapad i Access 2016 har dock båda 0x02 på den här platsen. En minimal databas skapad i Access 2016, men som definierade en kolumn med den nyligen introducerade datatypen "stort heltal", hade ett värde på 0x05. I ACCDB-filer verkar denna indikator återspegla filens kompatibilitet snarare än versionen av ACE-motorn som användes för att skapa den.

## Referenser

* [Access File Format](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Access 2016 Specifikationer](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Vilket Access-filformat ska jag använda?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)

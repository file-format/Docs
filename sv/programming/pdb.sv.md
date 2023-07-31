{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDB-filformat - En programdatabasfil",
  "description":"Läs mer om PDB-filformat och API:er som kan skapa och öppna PDB-filer.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är en PDB fil?

En fil med filtillägget .pdb är en programdatabasfil som innehåller felsökningsinformation för en kompilerad körbar fil (EXE/DLL). PDB-filer genereras av Microsofts kompilatorer när ett applikationsprogram kompileras i felsökningsläge. Förekomsten av PDB-fil kan hjälpa till med omvänd konstruktion av en körbar fil eftersom den innehåller betydande information om alla symboler i modulerna. Det är av denna anledning som dessa filer hålls åtskilda från den slutliga körbara filen. Microsofts [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) kan öppna en PDB-fil för att erhålla information som publik och export, globala symboler, lokala symboler, typdata, källfiler och radnummer.

## PDB filformat

PDB är Microsofts proprietära filformat och har inte dokumenterats officiellt någonstans ännu. Däremot finns en startdokumentation tillgänglig [här](https://github.com/Microsoft/microsoft-pdb) och kan refereras till.

### PDB-strömmar

PDB-filer består av flera strömmar där varje ström fungerar som en virtuell individuell fil och innehåller information. PDB-filskrivare kan skriva till dessa filer och filen slutförs först efter att en explicit commit har utfärdats. En kompilator kan fortsätta skriva till en PDB-fil men commit bara om all användarkod kompileras framgångsrikt. En PDB-fil består av följande strömmar:

|Strömnummer |Innehåll |Kort beskrivning|
---|---|---|
|1| Pdb (header) |Versionsinformation och information för att koppla denna PDB till EXE|
|2| Tpi (Typhanterare) |Alla typer som används i den körbara filen.|
|3| Dbi (Felsökningsinformation) |Innehåller sektionsbidrag och lista över 'Mods'|
|4| Namnkarta| Håller ett hastigt strängbord|
|4-(n+4)| n Mods (modulinformation)| Varje Mod-ström innehåller symboler och radnummer för en kompilation|
|n+4| Global symbol hash| Ett index som tillåter sökning i globala symboler efter namn|
|n+5| Offentlig symbol hash| Ett index som tillåter sökning i offentliga symboler efter adresser|
|n+6| Symbolposter| Faktiska symbolregister över globala och offentliga symboler|
|n+7| Skriv hash| Hash som används av TPI-strömmen.|

Varje ström i en PDB-fil består av flera sidor som inte nödvändigtvis är numrerade i följd.

### PDB-huvud

En PDB-fil har en Header som består av en signatur för att identifiera och validera det specifika formatet. Längden på signaturen beror på PDB-formatet. Rubriken kan vara längre än en sida.

### PDB Metadata
PDB-metadata är ansvarig för att känna igen alla komponentströmmar, vilket ger längden och sekvensen av sidor för varje ström. Order ges till strömmar i följd; börjar med 0. Det finns också en oordnad rotström, som innehåller en del av metadata.

## Referenser
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)


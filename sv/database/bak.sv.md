{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "tillägg", "fil", "filformat", "BAK-filtyp", "BAK-filtillägg", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om BAK-filformat och API:er som kan skapa och öppna BAK-filer.",
  "title" :"BAK File Format - Databas Backup File",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Vad är BAK fil?

En fil med filtillägget .bak är vanligtvis en säkerhetskopia som används av olika programvaruverktyg för att lagra säkerhetskopior av data. Ur databasperspektiv används en BAK-fil av Microsoft SQL Server för att lagra innehållet i en databas. Alla data och filer som är associerade med databasen lagras i detta filformat för att kunna hämtas i fall databasen kan bli korrupt eller ogiltig av någon anledning. Säkerhetskopieringsfilerna kan lagras och indexeras på andra servrar av säkerhetsskäl. Flera applikationer kan skapa BAK-filer som SQL Server Management Studio, Transact-SQL och Windows PowerShell.

## BAK filformat

De interna detaljerna i en BAK-fil är inte kända men det antas allmänt att den är baserad på Microsoft Tape Format (MTF). MTF-specifikationer finns tillgängliga och kan refereras till för att förstå filens struktur. Dokumentet ger information om MTF-lagring för alla som har en allmän kunskap om lagringshantering, bandenheter och filsystem.

### Datauppsättningar

En datamängd är en samling objekt som skrivs till ett lagringsmedium (band, optisk disk, etc.) under säkerhetskopiering eller återställning av data. Datauppsättningar består av flera media vid stora datavolymer.

### Grundläggande element i MTF

En MTF-fil består av några grundläggande element som utgör dess byggstenar. Dessa element är:

#### Beskrivningsblock

Deskriptorblock (DBLK) används för formatkontroll och utgör den primära grunden för en MTF-fil. En enda MTF-fil definierar flera DBLK:er för varje unik roll. Varje DBLK är ett datablock med variabel längd som är uppdelat i följande fyra delar:

* `Common Block Header` - Struktur med fast längd som är gemensam för alla DBLK. Detta är den enda Block Header som krävs.
* `DBLK Type Information` - Block med fast längd som är specifikt för den typ av DBLK som definieras
* `Operating System Data` - Specifik data som definieras baserat på typen av DBLK och operativsystem
* `DBLK Information` - DBLK-specifik information med variabel längd som inte kan sparas med Fixed Length DBLK-information.

 {{< figure src="../bak.png" alt="Microsoft SQL backup filformat" >}}

#### Dataström

Dataströmmar i en MTF-fil används för datainkapsling och justering. Den består av en Stream Header, följt av Stream Data. En strömhuvud kan endast kapsla in en enda typ av strömdata.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL backup filformat" >}}

#### FileMarks

Ett filmärke används för logisk separation och snabb åtkomst inom ett media. Filmärken emuleras av enhetsdrivrutinen eller genom att använda blocket Soft Filemark Descriptor om enheten som används inte tillhandahåller filmärken.

## Referenser ##

* [[MS-BCP]: Bulk Copy Format](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5?redirectedfrom=MSDN)


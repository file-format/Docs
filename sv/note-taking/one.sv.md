{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote-filformat",
  "description":"Läs mer om ONE-filformat och API:er som kan skapa och öppna ONE-filer.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en .ONE-fil? ##

Filer som representeras av .ONE-tillägget skapas av Microsoft OneNote-applikationen. OneNote låter dig samla information med applikationen som om du använder din utkastplatta för att göra anteckningar. OneNote-filer kan innehålla olika element som kan placeras på icke-fixerade platser på dokumentsidor. Dessa element kan innehålla text, digitaliserad handstil och objekt som kopierats från andra applikationer inklusive bilder, ritningar och multimedia (ljud/video) klipp. Microsoft erbjuder nu onlineversionen av OneNote som en del av Office365 där anteckningar kan delas med andra OneNote-användare över internet.

## .ONE Filformatspecifikationer ##

OneNote-filformatet ger ett effektivt sätt att representera digitala anteckningar som hierarkiska uppsättningar av avsnitt och sidor. Varje sida innehåller användardefinierat innehåll i en specifik struktur för representation av filformatet Document Object Model (DOM). Datamodellen för detta format är som illustreras nedan.

### Strukturöversikt ###

Som illustreras i datamodellen för OneNote-filformatet består ett OneNote-dokument av olika element.

#### Sektion ####

En sektion är den översta behållaren i en OneNote-fil som ytterligare innehåller olika element i den som:

* Sidor
* Metadata
* Egenskaper

Metadata och egenskaper inkluderar avsnittets namn, identifiering av sidorna som finns i avsnittet och i vilken ordning dessa sidor visas. Termen "sektion" hänvisar till alla sidor som finns i en sektion och representationen av dessa data i en OneNote®-versionslagringsfil, som har filnamnstillägget .one.

#### Sida ####

Användardefinierat innehåll i ett OneNote-dokument finns på en sida. Sidinformation inkluderar text, listor, tabeller, sidtitlar, bilder och anteckningstaggar. En sida består av konturobjekt till vilka de flesta av de ingående objekten läggs till. Varje sida kan tilldelas ett namn för meningsfull representation och objekt kan också läggas till direkt på sidorna. En sida kan vidare innehålla undersidor i ett hierarkiskt system.

#### Egenskaper och egenskapsuppsättningar ####

OneNote-innehåll består av egenskaper, egenskapsuppsättningar och fildataobjekt. En egenskapsuppsättning är en samling egenskaper som representerar någon typ av innehåll. Ett fildataobjekt är ett block av binär data som innehåller bilder, inbäddade filer eller ljud-/videoinnehåll.

#### OneNote Notebook ####

En anteckningsbok är en samling avsnittsfiler som är lagrade i samma katalog. En samling egenskaper används för att ange inställningar som ordning på sektionerna i anteckningsboken och färgen på anteckningsboken.

### Filstruktur ###

En revisionsarkiv MÅSTE börja med en **Rubrik**-struktur. Resten av filen är uppdelad i block av byte, där storleken och strukturen för varje block specificeras av fältet som refererar till det. Ett block är tillgängligt om det refereras av strukturen **Rubrik**, eller om det refereras av ett fält i ett annat nåbart block. Data utanför strukturen **Rubrik** och eventuella block som kan nås MÅSTE ignoreras.

Alla strukturer är justerade på 1-byte gränser. Alla heltal är signerade om inte annat anges. Alla fält är [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) om inget annat anges.

#### Rubrik ####

Rubriken för .ONE-filen består av bitar som innehåller olika unika ID och fält för representation av filinformation enligt följande:

`guidFileType (16 byte):` En GUID som anger typen av revisionsarkivet. MÅSTE vara ett av värdena från följande tabell.


|Filformat|Värde
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` En GUID som anger identiteten för denna versionsarkivfil. BÖR vara globalt unik.

`guidLegacyFileVersion (16 byte):` MÅSTE vara "{00000000-0000-0000-0000-0000000000000}" och MÅSTE ignoreras.

`guidFileFormat (16 bytes):` En GUID som anger att filen är en versionsarkivfil. MÅSTE vara "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 byte):` Ett heltal utan tecken. MÅSTE vara ett av värdena i följande tabell, beroende på filtyp.

|Filformat|Värde
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldest CodeThatHasWrittenToThisFile (4 byte):` Ett osignerat heltal. MÅSTE vara ett av värdena i följande tabell, beroende på filformatet för denna fil.


|Filformat|Värde
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewest CodeThatHasWrittenToThisFile (4 byte):` Ett heltal utan tecken. MÅSTE vara ett av värdena i följande tabell, beroende på filformatet för denna fil.

|Filformat|Värde
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 byte):` Ett heltal utan tecken. MÅSTE vara ett av värdena i följande tabell, beroende på filformatet för denna fil.

|Filformat|Värde
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 byte):` En **FileChunkReference32**-struktur som MÅSTE ha värdet "fcrZero".

`fcrLegacyTransactionLog (8 byte):` En **FileChunkReference32**-struktur som MÅSTE vara "fcrNil".

`cTransactionsInLog (4 byte):` Ett heltal utan tecken som anger antalet transaktioner i transaktionsloggen. FÅR INTE vara noll.

`cbLegacyExpectedFileLength (4 byte):` Ett heltal utan tecken som MÅSTE vara noll och MÅSTE ignoreras.

`rgbPlaceholder (8 byte):` Ett heltal utan tecken som MÅSTE vara noll och MÅSTE ignoreras.

`fcrLegacyFileNodeListRoot (8 byte):` En **FileChunkReference32**-struktur som MÅSTE vara "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 byte):` Ett heltal utan tecken som MÅSTE vara noll och MÅSTE ignoreras.

`fNeedsDefrag (1 byte):` MÅSTE ignoreras.

`fRepairedFile (1 byte):` MÅSTE ignoreras.

`fNeedsGarbageCollect (1 byte):` MÅSTE ignoreras.

`fHasNoEmbeddedFileObjects (1 byte):` Ett heltal utan tecken som MÅSTE vara noll och MÅSTE ignoreras.

`guidAncestor (16 bytes):` En GUID som specificerar fältet **Header.guidFile** i innehållsförteckningsfilen, givet av följande tabell:


|Innehållsförteckning Filformat|Plats för innehållsförteckningsfil
--- | --- |
|Section File - .One|Innehållsförteckningsfilen finns i samma katalog som den här filen.
|Innehållsförteckningsfil - .onetoc2|Innehållsförteckningsfilen finns i den här filens överordnade katalog.

Om GUID är {00000000-0000-0000-0000-000000000000} refererar det här fältet inte till en innehållsförteckningsfil.

`crcName (4 byte):` Ett osignerat heltal som specificerar CRC-värdet för namnet på denna versionslagringsfil. Namnet är Unicode-representationen av filnamnet med dess tillägg och ett extra nolltecken i slutet. Denna CRC beräknas alltid med hjälp av CRC-algoritmen för .one-filen, oavsett detta versionslagringsfilformat.

`fcrHashedChunkList (12 bytes):` En **FileChunkReference64x32**-struktur som specificerar en referens till det första **FileNodeListFragment** i en hashad chunklista. Om värdet på strukturen **FileChunkReference64x32** är "fcrZero" eller "fcrNil", finns inte den hashade bitlistan.

`fcrTransactionLog (12 bytes):` En **FileChunkReference64x32**-struktur som specificerar en referens till den första **TransactionLogFragment**-strukturen i en transaktionslogg. Värdet på fältet **fcrTransactionLog** FÅR INTE vara "fcrZero" och FÅR INTE vara "fcrNil".

`fcrFileNodeListRoot (12 byte):` En **FileChunkReference64x32** struktur som specificerar en referens till en rotfilsnodlista. Värdet på fältet **fcrFileNodeListRoot** FÅR INTE vara "fcrZero" och FÅR INTE vara "fcrNil".

`fcrFreeChunkList (12 bytes):` En **FileChunkReference64x32**-struktur som specificerar en referens till den första **FreeChunkListFragment**-strukturen. Om värdet på strukturen **FileChunkReference64x32** är "fcrZero" eller "fcrNil", så finns inte den fria bitlistan.

`cbExpectedFileLength (8 bytes):` Ett osignerat heltal som specificerar storleken, i byte, på denna versionslagringsfil.

`cbFreeSpaceInFreeChunkList (8 bytes):` Ett heltal utan tecken som SKA specificera storleken, i byte, på det lediga utrymmet som specificeras av listan över lediga bitar.

`guidFileVersion (16 byte):` En GUID. När antingen värdet för fältet **cTransactionsInLog** eller fältet **guidDenyReadFileVersion** ändras, MÅSTE **guidFileVersion** ändras till en ny GUID.

`nFileVersionGeneration (8 byte):` Ett heltal utan tecken som anger antalet gånger filen har ändrats. MÅSTE ökas när fältet **guidFileVersion** ändras.

`guidDenyReadFileVersion (16 byte):` En GUID. När det befintliga innehållet i filen ändras, exklusive **Header**-strukturen för filen och oanvända lagringsblock, MÅSTE **guidDenyReadFileVersion** ändras till en ny GUID.

`grfDebugLogFlags (4 byte):` MÅSTE vara noll. MÅSTE ignoreras.

`fcrDebugLog (12 byte):` En **FileChunkReference64x32** struktur som MÅSTE ha värdet "fcrZero". MÅSTE ignoreras.

`fcrAllocVerificationFreeChunkList (12 byte):` En **FileChunkReference64x32** struktur som MÅSTE vara "fcrZero". MÅSTE ignoreras.

`bnCreated (4 byte):` Ett osignerat heltal som specificerar byggnumret för programmet som skapade denna versionslagringsfil. BÖR ignoreras.

`bnLastWroteToThisFile (4 bytes):` Ett osignerat heltal som anger byggnumret för det program som senast skrev till denna versionslagringsfil. BÖR ignoreras.

`bnOldestWritten (4 bytes):` Ett osignerat heltal som specificerar byggnumret för det äldsta programmet som skrev till denna versionsarkivfil. BÖR ignoreras.

`bnNewestWritten (4 byte):` Ett osignerat heltal som specificerar byggnumret för den senaste applikationen som skrev till denna versionslagringsfil. BÖR ignoreras.

`rgbReserved (728 byte):` MÅSTE vara noll. MÅSTE ignoreras.

## Referenser ##

* [[MS-ONESTORE] - OneNote-filformat](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


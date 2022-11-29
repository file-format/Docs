{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad en _XLSX-fil och API:er är som kan skapa och öppna _XLSX-filer.",
  "title" :"Vad är en _XLSX-fil?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Vad är en _XLSX fil?

En fil med tillägget .\_xlsx är faktiskt en [XLSX](/sv/spreadsheet/xlsx/)-fil som har bytt namn av någon annan applikation. Detta kan hända i vissa fall när filnamnet innehåller en . i slutet av filnamnet. \_XLSX-filerna kan öppnas i Microsoft Excel liknande XLSX-filerna genom att återigen byta namn på dessa till .xlsx-tillägget.

## _XLSX-filformat - Mer information

_XLSX-filerna skiljer sig inte från XLSX-filerna och använder Open XML-standarden som antogs av Microsoft redan 2000. Före XLSX var [XLS](/sv/spreadsheet/xls/) det primära filformatet som användes för att arbeta med Excel-kalkylblad för att spara dokument i binärt format. Detta nya XML-baserade filformat kom med fördelar som små filstorlekar, motståndskraft mot filkorruption och välformaterad bildrepresentation. Detta nya XML-baserade filformat blev en del av Office 2007 och utförs även i de nya versionerna av Microsoft.

## \_XLSX filformatspecifikationer

Eftersom en \_XLSX-fil är en XLSX-fil som har bytt namn, har den samma specifikationer som originalfilen. Det är bara en arkivfil som är baserad på [ZIP](/sv/compression/zip/) arkivfilformat. Om du vill se innehållet i det här arkivet byter du bara namn på filen till filtillägget .zip och extraherar den för att se de ingående filerna i denna Excel-arbetsbok. En tom arbetsbok, när den extraheras till sina filer, har följande ingående filer och mappar.

### [Content_Types].xml

Detta är den enda filen som finns på basnivån när zip-filen extraheras. Den listar innehållstyperna för delar i paketet. Alla referenser till XML-filerna som ingår i paketet hänvisas till i denna XML-fil.

### \_rels (mapp)

Det här är Relations-mappen som innehåller en enda XML-fil som lagrar relationerna på paketnivå. Länkar till nyckeldelarna av Xlsx-filerna finns i den här filen som URI:er. Dessa URI:er identifierar typen av relation mellan varje nyckeldel och paketet. Detta inkluderar förhållandet till primära Office-dokument som finns som xl/workbook.xml och andra delar inom docProps som kärnegenskaper och utökade egenskaper.

### docProps

Denna mapp innehåller de övergripande dokumentegenskaperna. Dessa inkluderar en uppsättning kärnegenskaper, en uppsättning utökade eller programspecifika egenskaper och en miniatyrbild av dokumentet. En tom arbetsbok har två filer i den här mappen, nämligen app.xml och core.xml. core.xml innehåller information som författare, datum skapat och sparat och modifierat. App.xml innehåller information om innehållet i filen.

### xl (mapp)

Detta är huvudmappen som innehåller all information om innehållet i arbetsboken. Som standard har den följande mappar:

* \_rels
*tema
* arbetsblad

och följande xml-filer:

* styles.xml
* arbetsbok.xml

## Referenser

* [MS-XLSX - .xlsx filformat](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


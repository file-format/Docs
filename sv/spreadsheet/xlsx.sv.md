{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "fil", "tillägg", "filformat", "Excel", "kalkylblad" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om vad en XLSX-fil är och API:er som kan skapa och öppna XLSX-filer.",
  "title" :"XLSX-filformat - Vad är en XLSX-fil?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Vad är en XLSX fil?

**XLSX** är ett välkänt format för Microsoft Excel-dokument som introducerades av Microsoft med lanseringen av Microsoft Office 2007. Baserat på struktur organiserad enligt Open Packaging-konventionerna som beskrivs i [Del 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) av OOXML-standarden ECMA-376, är det nya formatet ett zip-paket som innehåller ett antal XML-filer. Den underliggande strukturen och filerna kan undersökas genom att helt enkelt packa upp .xlsx-filen.

## Kort historia av XLSX-filformat

XLSX-filformatet introducerades 2007 och använder Open XML-standarden anpassad av Microsoft redan 2000. Före XLSX var det vanliga filformatet [XLS](/sv/spreadsheet/xls/) som var rent binärt filformat. Den nya filtypen har lagt till fördelarna med små filstorlekar, färre förändringar av korruption och välformaterad bildrepresentation. Det var i början av 2000 när Microsoft bestämde sig för att gå för förändringen för att passa standarden för **Office Open XML**. År 2007 blev detta nya filformat en del av Office 2007 och används även i de nya versionerna av Microsoft Office.

## XLSX filformatspecifikationer

De officiella [XLSX-filformatsspecifikationerna](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) är tillgängliga online från Microsoft. För att se vad som finns inuti XLSX-filen byter du bara namn på den till [ZIP](/sv/compression/zip/)-filen genom att ändra dess tillägg och sedan extrahera den för att se de ingående filerna i denna Excel-arbetsbok. En tom arbetsbok, när den extraheras till sina filer, har följande ingående filer och mappar.

### [Content_Types].xml ###

Detta är den enda filen som finns på basnivån när zip-filen extraheras. Den listar innehållstyperna för delar i paketet. Alla referenser till XML-filerna som ingår i paketet hänvisas till i denna XML-fil.

### \_rels (mapp) ###

Det här är Relations-mappen som innehåller en enda XML-fil som lagrar relationerna på paketnivå. Länkar till nyckeldelarna av Xlsx-filerna finns i den här filen som URI:er. Dessa URI:er identifierar typen av relation mellan varje nyckeldel och paketet. Detta inkluderar förhållandet till primära Office-dokument som finns som xl/workbook.xml och andra delar inom docProps som kärnegenskaper och utökade egenskaper.

### docProps ###

Denna mapp innehåller de övergripande dokumentegenskaperna. Dessa inkluderar en uppsättning kärnegenskaper, en uppsättning utökade eller programspecifika egenskaper och en miniatyrbild av dokumentet. En tom arbetsbok har två filer i den här mappen, nämligen app.xml och core.xml. core.xml innehåller information som författare, datum skapat och sparat och modifierat. App.xml innehåller information om innehållet i filen.

### xl (mapp) ###

Detta är huvudmappen som innehåller all information om innehållet i arbetsboken. Som standard har den följande mappar:

* \_rels
*tema
* arbetsblad

och följande xml-filer:

* styles.xml
* arbetsbok.xml

## XLSX-formatexempel ##


För varje Excel-kalkylblad som finns i en arbetsbok finns det en XML-fil. Du kan hitta dessa XML-filer i mappen xl/worksheets. All information som finns i ett kalkylblad är organiserad i olika avsnitt i XML-filen. Låt oss undersöka ett exempel på ett arbetsblad från en arbetsbok som visas i följande bild.

{{< figure src="../XLSX file format.png" alt="XLSX filformat" >}}

Som kan ses innehåller detta kalkylblad innehåll i cellerna A1 till B2 och en bild. Dessutom är cell G13 för närvarande den aktiva cellen i kalkylbladet. Låt oss nu undersöka filen xl/worksheets/sheet1.xml för att se hur denna information representeras i XML-filen. Innehållet i denna XML-fil är som visas nedan.

{{< figure src="../XLSX File Format Details.png" alt="XPS filformat" >}}

1. Fliken har en temafärg applicerad på den. Det nämns i XML-filen med taggen<tabColor> efter tema-id.
1. Tabben Valt värde är satt till 1 vilket visar att detta är det valda arket
1. Som kan ses i första bilden ovan är cell G13 i kalkylbladet aktiv cell som också nämns i XML-filen.
1. Fliken sheetData representerar data som finns i kalkylbladet. Du kan dock se att det ursprungliga innehållet i kalkylbladet inte finns någonstans i det här avsnittet. Detta beror på att texten är indirekt hänvisad från "sharedStrings" XML-ark. Denna länkning säkerställer att varje text endast sparas en gång och kan refereras igen för att spara utrymme.
1. Bilden som kan ses hänvisas till med referens-id "rId2"

## Bidra

Måste dela något om filformaten XLSX eller Spreadsheet? Du kan lägga upp dina resultat i avsnittet [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Referenser

* [[MS-XLSX] - XLSX-filformat](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


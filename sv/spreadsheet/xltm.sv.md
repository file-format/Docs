{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "fil", "tillägg", "filformat", "Excel Open XML Macro", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad en XLTM-fil och API:er är som kan skapa och öppna dem.",
  "title" :"Vad är en XLTM-fil?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Vad är en XLTM fil?

XLTM-filtillägget representerar filer som genereras av Microsoft Excel som makroaktiverade mallfiler. XLTM-filer liknar [XLTX](/sv/spreadsheet/xltx/) i annan struktur än att de senare inte stöder att skapa mallfiler med makron. Sådana mallfiler används för att generera och ställa in layout, formatering och andra inställningar tillsammans med makron för att underlätta att skapa liknande XLSX-filer då.

## Kortfattad bakgrund ##

Det var i början av 2000 när Microsoft bestämde sig för att gå för förändringen för att passa standarden för **Office Open XML**. Dokument, av olika typer, under denna nya standard identifierades genom att lägga till "X" i deras tillägg, där "X" är för XML. År 2007 blev detta nya filformat en del av Office 2007 och används även i de nya versionerna av Microsoft Office. Den nya filtypen har lagt till fördelarna med små filstorlekar, mindre förändringar av korruption och välformaterad bildrepresentation.

## XLTM filformatspecifikationer ##

XLTM-filer är baserade på Office OpenXML-filformatet och använder XML och [ZIP](/sv/Compression/ZIP/) för att minska filstorleken. Dessa kan öppnas med Microsoft Excel genom att dubbelklicka på filen. Filorganisationen i ett XLTM-filformat kan observeras genom att döpa om filen till ZIP och sedan extrahera dess innehåll till skiva.

### [Content_Types].xml ###

Detta är den enda filen som finns på basnivån när zip-filen extraheras. Den listar innehållstyperna för delar i paketet. Alla referenser till XML-filerna som ingår i paketet hänvisas till i denna XML-fil.

### \_rels (mapp) ###

Det här är Relations-mappen som innehåller en enda XML-fil som lagrar relationerna på paketnivå. Länkar till nyckeldelarna av Xltx-filerna finns i den här filen som URI:er. Dessa URI:er identifierar typen av relation mellan varje nyckeldel och paketet. Detta inkluderar förhållandet till primära Office-dokument som finns som xl/workbook.xml och andra delar inom docProps som kärna och utökade egenskaper.

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

## Referenser ##

* [MS-XLSX filformat](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


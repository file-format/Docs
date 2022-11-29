{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "fil", "tillägg", "filformat", "Excel binär kalkylbladsfil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad en XLSB-fil och API:er är som kan skapa och öppna dem.",
  "title" :"Vad är en XLSB-fil?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Vad är en XLSB fil?

XLSB-filformatet anger det binära filformatet för Excel, som är en samling poster och strukturer som anger innehåll i Excel-arbetsboken. Innehållet kan inkludera ostrukturerade eller semistrukturerade tabeller med siffror, text eller både siffror och text, formler, externa dataanslutningar, diagram och bilder. Till skillnad från [XLSX](/sv/spreadsheet/xlsx/) (som är baserat på Open XML-filformat), representerar XLSB en binär Excel-arbetsboksfil. XLSB-filer kan läsas och skrivas till snabbare vilket gör dem användbara för att arbeta med stora filer. XLSB används sällan för att lagra arbetsböcker eftersom XLSX (och tidigare [XLS](/sv/spreadsheet/xls/)) är de vanligaste användarvalda filformaten för att spara arbetsböcker. Den kan öppnas av Microsoft Office 2007 och senare.

## Specifikationer för XLSB-filformat ##

Filformatspecifikationerna för XLSB-filformat offentliggjordes redan 2008 som version 1.0. Sedan dess har specifikationerna reviderats flera gånger och den senaste versionen av specifikationerna (v 10.0) publicerades i april 2018. Specifikationerna är tillgängliga för allmänheten av Microsoft som [[MS-XLSB] - Excel Binary File Format specifications](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) och bör konsulteras av alla för att läsa eller skriva filer i XLSB-filformat.

## XLSB-filstruktur ##

En XLSB-fil är ett paket som består av en samling delar. Dessa delar innehåller information om innehållet i en arbetsbok, inklusive arbetsboksdata och paketets struktur. Vissa delar innehåller information lagrad med binära poster, vissa som XML, medan andra innehåller information lagrad som en binär ström av byte. Varje binär post innehåller noll eller fler strukturerade fält som innehåller arbetsboksdata.

#### Paket ####

Ett XLSB-paket är ett [ZIP](/sv/compression/zip/)-arkiv som måste innehålla exakt en arbetsboksdel. Den här delen måste vara målet för en relation i den här paketrelationsdelen. Arbetsboksdelen är startdelen i XLSB-dokumentet.

#### Del ####

En del är en ström av bytes som har en associerad innehållstyp som anger arten och typen av innehåll som lagras i delen. Vissa delar lagrar information i binärt format medan andra lagrar information som XML. Avsnittet [delaruppräkning](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) i specifikationsdokumentet listar giltiga delar, innehållstyper och obligatoriska/valfria relationer mellan alla delar i ett paket.

#### Förhållande ####

En källa och en målresurs är sammankopplade genom en relation. En relation kan vara:

**Paketrelation:** där målet är en del och källan är paketet som helhet

**Del-till-del-relation:** där målet är en del och källan är en del i paketet

**Explicit relation:** där en resurs refereras från innehållet i en källdel genom att referera till ID-attributvärdet för ett relationselement

**implicit relation** är en relation som inte är explicit

**Intern relation:** där målet är en del av paketet

**Extern relation:** där målet är en extern resurs som inte finns i paketet

#### Spela in ####

En post är den grundläggande byggstenen som används för att lagra information om funktioner i en arbetsbok. Varje binär post är en sekvens av bytes med variabel längd. En binär post består av tre komponenter:

* en posttyp
* en rekordstorlek, och
* postdata som är specifik för den posttypen.

**Record Type:** Posttypen visar den typ av post som anges av posten. Den specificerar också strukturen för postdata som är specifik för denna post. De giltiga posttyperna listas i avsnittet [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) i specifikationsdokumentet. Posttypen måste vara en eller två byte och måste vara större än eller lika med 128 och mindre än 16384.

**Record Size:** Poststorleken anger antalet byte som anger den totala storleken på postdata. Detta värde MÅSTE vara en till fyra byte. Detta värde MÅSTE vara en byte om den höga biten i den låga byten är lika med 0; annars MÅSTE detta värde vara större än en byte. Om antalet byte är större än en byte, specificerar den höga biten i varje successiv byte om ytterligare en byte används. Om den höga biten för den andra byten är lika med 1, MÅSTE detta värde använda ytterligare en tredje byte. Om den höga biten för den tredje byten är lika med 1, MÅSTE detta värde använda ytterligare en fjärde byte. Den höga biten i den fjärde byten MÅSTE ignoreras. Värdet består av de sju låga bitarna av varje byte kombinerat. De låga, minst signifikanta bitarna finns inom den första byten, och varje successiv byte innehåller bitar av högre ordning än den föregående byten.

**Record Data:** Postdatakomponenten innehåller fält som motsvarar en viss posttyp och utgör resten av posten. Ordningen och strukturen för fälten för en given posttyp som listas i Record Enumeration specificeras i motsvarande avsnitt för den posttypen i Records. Den totala storleken på postdatakomponenten MÅSTE vara lika med poststorleken. Fält i postdatakomponenten kan innehålla enkla värden, matriser av värden, strukturer av flera fält, matriser av fält och matriser av strukturer.

#### XLSB Record Exempel ####

Följande posttyp och poststorlek anger en **BrtCommentText**-post med en storlek på 200 byte:

11111101 00000100 11001000 00000001 [Record Fields]

Den första byten är 11111101, som anger ett lågt värde på 125 och att posttypen kräver en andra byte. Den andra byten är 00000100, vilket anger ett högt värde på 4 * 128, vilket är lika med 512. Posttypvärdet är 125 + 512, eller 637, vilket motsvarar en posttyp **BrtCommentText**. Nästa byte är 11001000, vilket anger ett lågt värde på 72 och att poststorleken kräver en andra byte. Den andra byten är 00000001, vilket anger ett högre värde på 1 * 128 och att poststorleken inte kräver en extra byte. Poststorleken är 72 + 128, eller 200, vilket anger den totala storleken, i byte, för postdatakomponenten. Fälten i postdatakomponenten specificeras av **BrtCommentText**.

## Referenser ##

* [[MS-XLSB] - Excel (.xlsb) binärt filformat](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)


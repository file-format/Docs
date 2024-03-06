{
  "date": "2019-12-10",
  "keywords": [
"XLSX",
"failu",
"pagarinājumu",
"faila formātā",
"Excel",
"Izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet, kas ir XLSX fails un API, kas var izveidot un atvērt XLSX failus.",
  "title": "XLSX faila formāts — kas ir XLSX fails?",
  "linktitle": "XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-lvx"
}
},
  "lastmod": "2019-12-10"
}

## Kas ir XLSX fails?

**XLSX** is well-known format for Microsoft Excel documents that was introduced by Microsoft with the release of Microsoft Office 2007. Pamatojoties uz struktūru, kas organizēta saskaņā ar Open Packaging Conventions, kā norādīts OOXML standarta ECMA-376 [Part 2](https://www.ecma-international.org/publications-and-standards/standards/ecma-376/), jaunais formāts ir zip pakotne, kas satur vairākus XML failus. Pamatstruktūru un failus var pārbaudīt, vienkārši izpakojot .xlsx failu.

## Īsa XLSX faila formāta vēsture

XLSX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Pirms XLSX izplatītais faila formāts bija [XLS](/spreadsheet/xls/), kas bija tīrs binārais faila formāts. Jaunajam faila tipam ir pievienotas maza izmēra failu priekšrocības, mazākas bojājumu izmaiņas un labi formatētu attēlu attēlojums. Tas bija 2000. gada sākumā, kad Microsoft nolēma veikt izmaiņas, lai pielāgotos **Office Open XML** standartam. Līdz 2007. gadam šis jaunais faila formāts kļuva par Office 2007 daļu un tiek izmantots arī jaunajās Microsoft Office versijās.

## XLSX faila formāta specifikācijas

Oficiālā [XLSX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) ir pieejama tiešsaistē no Microsoft. Lai redzētu, kas atrodas XLSX failā, vienkārši pārdēvējiet to par [ZIP](/compression/zip/) failu, mainot tā paplašinājumu, un pēc tam izvelciet to, lai skatītu šīs Excel darbgrāmatas veidojošos failus. Tukšā darbgrāmatā, kas izvilkta tās failos, ir šādi faili un mapes.

### [Satura_veidi].xml ###

Šis ir vienīgais fails, kas tiek atrasts bāzes līmenī, kad tiek izvilkts zip. Tajā ir norādīti pakotnes daļu satura veidi. Visas atsauces uz pakotnē iekļautajiem XML failiem ir norādītas šajā XML failā.

### \_rels (mape) ###

Šī ir mape Relationships, kurā ir viens XML fails, kurā tiek saglabātas pakotnes līmeņa attiecības. Saites uz galvenajām Xlsx failu daļām ir ietvertas šajā failā kā URI. Šie URI identificē katras galvenās daļas attiecību veidu ar pakotni. Tas ietver saistību ar primāro biroja dokumentu, kas atrodas kā xl/workbook.xml, un citām docProps daļām kā pamata un paplašinātos rekvizītus.

### docProps ###

Šajā mapē ir ietverti vispārējie dokumenta rekvizīti. Tie ietver galveno rekvizītu kopu, paplašinātu vai lietojumprogrammai raksturīgu rekvizītu kopu un dokumenta sīktēlu priekšskatījumu. Tukšā darbgrāmatā šajā mapē ir divi faili, proti, app.xml un core.xml. core.xml satur tādu informāciju kā autors, izveides un saglabāšanas datums un modificēšana. App.xml satur informāciju par faila saturu.

### xl (mape) ###

Šī ir galvenā mape, kurā ir visa informācija par darbgrāmatas saturu. Pēc noklusējuma tai ir šādas mapes:

* \_rels

* tēma

* darba lapas


un šādi xml faili:

* styles.xml

* darbgrāmata.xml


## XLSX formāta piemērs ##


Katrai darbgrāmatā iekļautajai Excel darblapai ir viens XML fails. Šos XML failus varat atrast mapē xl/worksheets. Visa darblapā esošā informācija ir sakārtota dažādās XML faila sadaļās. Apskatīsim darblapas paraugu no darbgrāmatas, kas parādīta nākamajā attēlā.

{{< figure src="../XLSX file format.png" alt="XLSX faila formāts" >}}

Kā redzams, šajā darblapā ir saturs šūnās A1 līdz B2 un attēls. Turklāt šūna G13 pašlaik ir darblapas aktīvā šūna. Tagad apskatīsim failu xl/worksheets/sheet1.xml, lai redzētu, kā šī informācija ir attēlota XML failā. Šī XML faila saturs ir parādīts tālāk.

{{< figure src="../XLSX File Format Details.png" alt="XPS faila formāts" >}}

1. Cilnei ir piemērota motīva krāsa. Tas ir minēts XML failā ar tagu<tabColor> pēc tēmas id.
1. Cilnes Selected vērtība ir iestatīta uz 1, kas parāda, ka šī ir atlasītā lapa
1. Kā redzams pirmajā attēlā, darblapas šūna G13 ir aktīva šūna, kas ir minēta arī XML failā.
1. Cilne sheetData attēlo darblapā ietvertos datus. Tomēr var redzēt, ka darblapas oriģinālais saturs šajā sadaļā nav atrodams. Tas ir tāpēc, ka teksts ir netieši norādīts no sharedStrings XML lapas. Šī saistīšana nodrošina, ka katrs teksts tiek saglabāts tikai vienu reizi un uz to var atsaukties vēlreiz, lai ietaupītu vietu.
1. Attēlam, kā redzams, ir atsauce ar atsauces ID rId2

## Piedalieties

Vai vēlaties kopīgot informāciju par XLSX vai izklājlapu failu formātiem? Jūs varat publicēt savus atklājumus sadaļā [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Atsauces

* [[MS-XLSX] — XLSX faila formāts](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)



{
  "date": "2019-12-10",
  "keywords": [
"XLTX",
"failu",
"pagarinājumu",
"faila formātā",
"Excel Open XML",
"Izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir XLTX fails un API, kas tos var izveidot un atvērt.",
  "title": "Kas ir XLTX fails?",
  "linktitle": "XLTX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-lvx"
}
},
  "lastmod": "2019-12-10"
}

## Kas ir XLTX fails?

Faili ar paplašinājumu .xltx ir Microsoft Excel veidņu faili, kuru pamatā ir Office OpenXML faila formāta specifikācijas. To izmanto, lai izveidotu standarta veidnes failu, ko var izmantot, lai ģenerētu [XLSX](/spreadsheet/xlsx/) failus, kuriem ir tādi paši iestatījumi kā XLTX failā.

## Īsa vēsture

Tas bija 2000. gada sākumā, kad Microsoft nolēma veikt izmaiņas, lai pielāgotos **Office Open XML** standartam. Dažādu veidu dokumenti saskaņā ar šo jauno standartu tika identificēti, to paplašinājumos pievienojot X, kur X ir XML. Līdz 2007. gadam šis jaunais faila formāts kļuva par Office 2007 daļu un tiek izmantots arī jaunajās Microsoft Office versijās. Jaunajam faila tipam ir pievienotas maza izmēra failu priekšrocības, mazākas bojājumu izmaiņas un labi formatētu attēlu attēlojums.

## XLTX faila formāta specifikācijas

XLTX faili ir balstīti uz Office OpenXML faila formātu un izmanto XML un [ZIP](/compression/zip/), lai samazinātu faila lielumu. Tas tika izveidots, izlaižot Microsoft Office 2007, lai aizstātu bināro XLT faila formātu. Līdzīgi kā XLTX, XLT faila formātu var izmantot, lai izveidotu [XLS](/spreadsheet/xls/) failus, izmantojot Microsoft Excel 2003 un 2007. Tos var atvērt programmā Microsoft Excel, veicot dubultklikšķi uz faila. Failu organizēšanu XLTX faila formātā var novērot, pārdēvējot failu par ZIP un pēc tam izvelkot tā saturu diskā.

### [Satura_veidi].xml ###

Šis ir vienīgais fails, kas tiek atrasts bāzes līmenī, kad tiek izvilkts zip. Tajā ir norādīti pakotnes daļu satura veidi. Visas atsauces uz pakotnē iekļautajiem XML failiem ir norādītas šajā XML failā.

### \_rels (mape) ###

Šī ir mape Relationships, kurā ir viens XML fails, kurā tiek saglabātas pakotnes līmeņa attiecības. Saites uz galvenajām Xltx failu daļām ir ietvertas šajā failā kā URI. Šie URI identificē katras galvenās daļas attiecību veidu ar pakotni. Tas ietver saistību ar primāro biroja dokumentu, kas atrodas kā xl/workbook.xml, un citām docProps daļām kā galvenos un paplašinātos rekvizītus.

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


## Atsauces Nr.

* [[MS-XLSX] — .Xlsx faila formāts](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)



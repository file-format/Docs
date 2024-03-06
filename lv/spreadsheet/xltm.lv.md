{
  "date": "2019-12-10",
  "keywords": [
"XLTM",
"failu",
"pagarinājumu",
"faila formātā",
"Excel Open XML makro",
"Izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir XLTM fails un API, kas tos var izveidot un atvērt.",
  "title": "Kas ir XLTM fails?",
  "linktitle": "XLTM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-lvm"
}
},
  "lastmod": "2019-12-10"
}

## Kas ir XLTM fails?

XLTM faila paplašinājums apzīmē failus, kas ir ģenerēti programmā Microsoft Excel kā veidņu faili ar iespējotu makro. XLTM faili ir līdzīgi [XLTX](/spreadsheet/xltx/) pēc struktūras, izņemot to, ka vēlākais neatbalsta veidņu failu izveidi ar makro. Šādi veidņu faili tiek izmantoti, lai ģenerētu un iestatītu izkārtojumu, formatējumu un citus iestatījumus kopā ar makro, lai pēc tam atvieglotu līdzīgu XLSX failu izveidi.

## Īsa vēsture ##

Tas bija 2000. gada sākumā, kad Microsoft nolēma veikt izmaiņas, lai pielāgotos **Office Open XML** standartam. Dažādu veidu dokumenti saskaņā ar šo jauno standartu tika identificēti, to paplašinājumos pievienojot X, kur X ir XML. Līdz 2007. gadam šis jaunais faila formāts kļuva par Office 2007 daļu un tiek izmantots arī jaunajās Microsoft Office versijās. Jaunajam faila tipam ir pievienotas maza izmēra failu priekšrocības, mazākas bojājumu izmaiņas un labi formatētu attēlu attēlojums.

## XLTM faila formāta specifikācijas ##

XLTM faili ir balstīti uz Office OpenXML faila formātu un izmanto XML un [ZIP](/compression/zip/), lai samazinātu faila lielumu. Tos var atvērt programmā Microsoft Excel, veicot dubultklikšķi uz faila. Failu organizēšanu XLTM faila formātā var novērot, pārdēvējot failu par ZIP un pēc tam izvelkot tā saturu diskā.

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

* [MS-XLSX faila formāts](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)



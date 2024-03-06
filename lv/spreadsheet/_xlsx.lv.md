{
  "date": "2019-12-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir _XLSX fails un API, kas var izveidot un atvērt _XLSX failus.",
  "title": "Kas ir _XLSX fails?",
  "linktitle": "_XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-_xls-lvx"
}
},
  "lastmod": "2021-11-22"
}

## Kas ir _XLSX fails?

Fails ar paplašinājumu .\_xlsx patiesībā ir fails [XLSX](/spreadsheet/xlsx/), ko pārdēvē kāda cita lietojumprogramma. Tas var notikt noteiktos gadījumos, kad faila nosaukumā ir . faila nosaukuma beigās. \_XLSX failus var atvērt programmā Microsoft Excel līdzīgi kā XLSX failus, atkārtoti pārdēvējot tos par paplašinājumu .xlsx.

## _XLSX faila formāts — vairāk informācijas

The _XLSX files are no different than the XLSX files and use the Open XML standard adopted by Microsoft back in 2000. Pirms XLSX [XLS](/spreadsheet/xls/) bija galvenais faila formāts, ko izmantoja darbam ar Excel izklājlapām, lai saglabātu dokumentus binārā formātā. Šim jaunajam XML faila formātam bija tādas priekšrocības kā mazi failu izmēri, izturība pret failu bojājumiem un labi formatētu attēlu attēlojums. Šis jaunais XML faila formāts kļuva par Office 2007 daļu, un tas tiek izmantots arī jaunajās Microsoft versijās.

## \_XLSX faila formāta specifikācijas

Tā kā \_XLSX fails ir pārdēvēts XLSX fails, tam ir tādas pašas specifikācijas kā oriģinālajam failam. Tas ir tikai arhīva fails, kura pamatā ir [ZIP](/compression/zip/) arhīva faila formāts. Ja vēlaties skatīt šī arhīva saturu, vienkārši pārdēvējiet failu uz .zip paplašinājumu un izvelciet to, lai skatītu šīs Excel darbgrāmatas veidojošos failus. Tukšā darbgrāmatā, kas izvilkta tās failos, ir šādi faili un mapes.

### [Satura_veidi].xml

Šis ir vienīgais fails, kas tiek atrasts bāzes līmenī, kad tiek izvilkts zip. Tajā ir norādīti pakotnes daļu satura veidi. Visas atsauces uz pakotnē iekļautajiem XML failiem ir norādītas šajā XML failā.

### \_rels (mape)

Šī ir mape Relationships, kurā ir viens XML fails, kurā tiek saglabātas pakotnes līmeņa attiecības. Saites uz galvenajām Xlsx failu daļām ir ietvertas šajā failā kā URI. Šie URI identificē katras galvenās daļas attiecību veidu ar pakotni. Tas ietver saistību ar primāro biroja dokumentu, kas atrodas kā xl/workbook.xml, un citām docProps daļām kā pamata un paplašinātos rekvizītus.

### docProps

Šajā mapē ir ietverti vispārējie dokumenta rekvizīti. Tie ietver galveno rekvizītu kopu, paplašinātu vai lietojumprogrammai raksturīgu rekvizītu kopu un dokumenta sīktēlu priekšskatījumu. Tukšā darbgrāmatā šajā mapē ir divi faili, proti, app.xml un core.xml. core.xml satur tādu informāciju kā autors, izveides un saglabāšanas datums un modificēšana. App.xml satur informāciju par faila saturu.

### xl (mape)

Šī ir galvenā mape, kurā ir visa informācija par darbgrāmatas saturu. Pēc noklusējuma tai ir šādas mapes:

* \_rels

* tēma

* darba lapas


un šādi xml faili:

* styles.xml

* darbgrāmata.xml


## Atsauces

* [MS-XLSX — .xlsx faila formāts](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)



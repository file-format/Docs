{
  "date": "2019-12-10",
  "keywords": [
"XLM",
"failu",
"pagarinājumu",
"faila formātā",
"Microsoft Excel makro fails",
"Izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir XLM makro fails un API, kas var izveidot un atvērt XLM failus.",
  "title": "Kas ir XLM fails?",
  "linktitle": "XLM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-lvm"
}
},
  "lastmod": "2019-12-10"
}

## Kas ir XLM fails?

XLM, kas paredzēts Excel makro, ir izklājlapu failu veids, ko izmanto makro glabāšanai. No lietojumprogrammas viedokļa makro ir instrukciju kopums, kas tiek izmantots procesu automatizēšanai. Makro tiek izmantots, lai ierakstītu darbības, kas tiek atkārtoti veiktas faila formātam [XLS](/spreadsheet/xls/), un atvieglo darbību veikšanu, vēlreiz palaižot makro. Makro tiek ieprogrammēti ar Microsoft Visual Basic for Applications (VBA) no Excel darbgrāmatas, izmantojot Visual Basic redaktoru, un tos var palaist/atkļūdot tieši no turienes.

## Īsa vēsture ##

Microsoft Excel supported programming of macros since its first public launch. The features of macros remained the same through subsequent versions fo Excel with extension as per new features. XLM was the default macro language for Excel through Excel 4.0. Programmā Excel 5.0 pēc noklusējuma tika ierakstīti makro VBA, taču ar versiju 5.0 XLM ierakstīšana joprojām bija atļauta kā opcija. Pēc versijas 5.0 šī opcija tika pārtraukta. Visas Excel versijas, tostarp Excel 2010, var palaist XLM makro, lai gan Microsoft neiesaka to izmantot.

## Makro ierakstīšana XLM formātā ##

Excel nodrošina vienkāršas darbības makro ierakstīšanai. Lai strādātu ar makro, jums ir jābūt instalētiem izstrādātāja rīkiem. Kad makro ierakstīšana ir procesā, tā ieraksta katru lietotāja darbību, kas tiks atskaņota vēlāk. Makro ierakstīšana faktiski ietver visas darbības, ko lietotājs veic pēc ierakstīšanas sākuma. Tādējādi, ja šūnas saturu iestatāt treknrakstā, slīprakstā un iestatāt teksta pamatojumu pēc makro ierakstīšanas sākšanas, visas šīs komandas tiks ierakstītas. Katram ierakstītajam makro var piešķirt arī saīsni ātrai atskaņošanai vēlāk. Makro ierakstīšana ģenerē VBA kodu makro veidā, ko var rediģēt, izmantojot Visual Basic redaktoru (VBE).

## Excel objekta modelis ##

Makro aizmugurē tiek izmantotas VBA rutīnas, un šim nolūkam ievērojiet [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model). Šis modelis identificē izklājlapas objektus mijiedarbībai ar izklājlapu, izmantojot lietotāja definētas komandu rīkjoslas, komandjoslas vai ziņojumu lodziņus. Piemēram, ar darbgrāmatas objektu tiek piešķirta piekļuve darbgrāmatas rekvizītiem. Tāpat modelī ir darblapas objekts, lai programmatiski strādātu ar darbgrāmatas darblapām.

## Makro un drošība ##

VBA ļauj piekļūt visām pielietojuma jomām, kā arī failu sistēmai, kā arī var būt bīstams. Tas rada bažas, koplietojot darbgrāmatu ar kādu, kurš var palaist failu savā galā. Tas ir, Microsoft Excel brīdina par šāda faila atvēršanu. Makro var tikt sertificēti ar ciparparakstu, lai citi lietotāji varētu pārbaudīt, vai tie ir uzticami. Tādējādi makro var iespējot pēc to avota pārbaudes.

## Atsauces Nr.

* [[MS-XLS] — Excel binārā faila formāta struktūra](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [Makro programmēšana](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)



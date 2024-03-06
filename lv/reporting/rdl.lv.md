{
  "date": "2021-03-01",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDL — ziņojuma definīcijas valodas fails",
  "keywords": [
"rdl",
"ziņojuma definīcijas valoda",
"XmlTextWriter",
"XSD",
"RDL elements"
],
  "description": "Uzziniet par RDL faila formātu, kas ir SQL Server Reporting Services pārskata definīcijas XML attēlojums.",
  "linktitle": "RDL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rd-lvl"
}
},
  "lastmod": "2021-03-01"
}

## Kas ir RDL fails? ##

RDL (Report Definition Language) ir Microsoft noteiktais etalons pārskatu definēšanai. RDL fails sastāv no viena vai vairākiem RDL elementiem. Tā kā RDL elements sastāv no tā datu veida un kardinalitātes. Elements var būt vienkāršs vai sarežģīts. Vienkāršajam elementam nav pakārtota elementa vai atribūtu, savukārt sarežģītajam elementam ir atvasinājumi un neobligāti atribūti.

## RDL XML shēmas definīcija
XML shēmas definīcijas (XSD) fails apstiprina RDL failu. Shēma nosaka noteikumus, kur RDL elementi var atrasties .rdl failā. RDL elements var būt vienkāršs vai sarežģīts. Vienkāršam elementam nav pakārtotu elementu vai atribūtu, savukārt sarežģītajam elementam ir atvasinājumi un pēc izvēles atribūti.

## RDL izveide
Tā kā RDL pēc būtības ir atvērts un paplašināms, var izveidot daudzas lietojumprogrammas un rīkus, kas ģenerē RDL failus, pamatojoties uz tās XML shēmu. Viens no vienkāršākajiem veidiem, kā no lietojumprogrammas izveidot RDL, ir izmantot Microsoft .NET Framework klases nosaukumvietā **System.Xml** un System.Linq nosaukumvietā. Jo īpaši **XmlTextWriter** klasi var izmantot, lai rakstītu RDL. Varat ģenerēt pilnīgu pārskata definīciju no sākuma līdz beigām jebkurā .NET Framework lietojumprogrammā, izmantojot **XmlTextWriter**. Izstrādātāji var arī pievienot pielāgotus pārskata vienumus ar pielāgotiem rekvizītiem, lai paplašinātu RDL.

## RDL veidi
Nākamajā tabulā ir uzskaitīti RDL elementos izmantotie veidi un atribūti.

|Tips|Apraksts|
---|---|
|Binārs |Īpašums ar 64 bāzes kodētu bināro vērtību.|
|Būla| Īpašums ar patiesu vai nepatiesu objekta vērtību. Ja vien nav norādīts citādi, izlaistā neobligātā Būla objekta vērtība ir False.|
|Date	|A property with a fully specified date or datetime value specified in ISO8601 date format: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Īpašums ar virknes teksta vērtību, kurai jābūt vienai no norādīto vērtību saraksta.|
|Pludināts |Īpašums ar mainīgu vērtību. Punktu (.) izmanto kā izvēles decimālo atdalītāju.|
|Integer |Īpašums ar veselu (int32) vērtību.|
|Language |Īpašums ar teksta vērtību, kas satur valodas un kultūras kodu, piemēram, en-us ASV angļu valodā. Vērtībai ir jābūt noteiktai valodai vai neitrālai valodai, kurai Microsoft .NET Framework ir definēta noklusējuma valoda.|
|Nosaukums |Īpašums ar virknes teksta vērtību. Nosaukumiem ir jābūt unikāliem vienuma nosaukumvietā. Ja nav norādīts, vienuma nosaukumvieta ir visdziļākais saturošais objekts, kuram ir nosaukums.|
|NormalizedString |Īpašums ar virknes teksta vērtību, kas ir normalizēta.|
|Izmērs |Izmēra elementā ir jāietver cipars (ar punkta rakstzīmi, ko izmanto kā neobligātu decimālo atdalītāju). Aiz numura ir jābūt CSS garuma mērvienības apzīmējumam, piemēram, cm, mm, collas, pt vai pc. Atstarpe starp numuru un apzīmējumu nav obligāta. Papildinformāciju par izmēru apzīmējumiem skatiet sadaļā CSS vērtību un vienību atsauce. RDL formātā Size maksimālā vērtība ir 160 collas. Minimālais izmērs ir 0 collas.|
|String |Īpašums ar virknes teksta vērtību.|
|UnsignedInt |Īpašums ar neparakstītu veselu skaitli (uint32) vērtību.|
|Variants |Īpašums ar jebkuru vienkāršu XML veidu.|

## RDL datu tipi
RDL datu tipa uzskaitījums definē atribūta, izteiksmes vai parametra datu tipu. Nākamajā tabulā parādīts, kā CLR datu tipi atbilst RDL datu tipiem.

|CLR tips(-i) |Atbilstošais datu tips|
---|---|
|Būla| Būla|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, baits, sbaits |Vesels skaitlis|
|Vienvietīgs, Divvietīgs |Pludiņš|
|String, Char, GUID, Timespan |String|


## Atsauces Nr.

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)


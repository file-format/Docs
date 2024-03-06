{
  "date": "2021-08-11",
  "keywords": [
"wim fails",
"wim faila formāts",
"kas ir wim fails",
"failu",
"wim piemērs",
"wim faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par WIM failu formātu un API, kas var izveidot un atvērt WIM failus.",
  "title": "WIM — Windows attēlveidošanas formāta fails",
  "linktitle": "WIM",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-wi-lvm"
}
},
  "lastmod": "2021-08-11"
}

## Kas ir WIM fails?
Faili ar .wim paplašinājumiem pirmo reizi tika redzēti operētājsistēmā Windows Vista. WIM pieder failiem balstītam attēlveidošanas formātam, kas parasti tika ieviests operētājsistēmā Microsoft Windows Vista. Tas nodrošina viena diska attēla izvietošanu dažādās datoru platformās. WIM faili tiek izmantoti, lai pārvaldītu failus, piemēram, atjauninājumus, draiverus un komponentus, nepārstartējot operētājsistēmas attēlu. AQ WIM fails satur failu kopu un saistītos metadatus, kas ir ļoti līdzīgi citiem diska failu formātiem.

## WIM failu formāti
WIM faila formāts nav līdzīgs sektoru formātiem, piemēram, VHD vai IS, patiesībā tas ir balstīts uz failiem, kas nozīmē, ka WIM informācijas pamatvienība ir fails. Pamata ieguvums, balstoties uz failiem, ir tāds, ka viena faila glabāšana, kas vairākas reizes norādīta failu sistēmas kokā, un aparatūras neatkarība. Tas samazina dažādu failu atvēršanas un aizvēršanas izmaksas, jo faili tiek glabāti vienā WIM. failu. WIM failos var saglabāt vairākus diska attēlus, uz kuriem atsaucas vai nu ar to unikālo nosaukumu, vai pēc to skaitliskā indeksa.
### Atbalsts kompresijas algoritmiem
WIM atbalsta šādas saspiešanas algoritmu saimes dilstošā ātrumā un augošā proporcijā:
- XPRESS
- LZX
- LZMS
- Cieta kompresija.
Pirmās trīs saimes ir balstītas uz LZ77, savukārt cietā saspiešana tika ieviesta kopā ar LZMS operētājsistēmās WIMGAPI Windows 8 un DISM Windows 8.1.
### Rīki WIM faila formātam
WIM faila formātu parasti atbalsta šādi rīki:

- **ImageX**: komandrindas rīks, ko izmanto, lai rediģētu, izveidotu un izvietotu Windows diska attēlus Windows attēlveidošanas formātā. Kopā ar attiecīgo WIMGAPI tas tiek izplatīts kā daļa no bezmaksas Windows automatizētās instalācijas komplekta. Sākot ar Windows Vista, Windows iestatīšana izmanto WAIK API, lai instalētu Windows.
- **DISM**: rīks, kas ieviests operētājsistēmās Windows 7 un Windows Server 2008 R2, kas var veikt ar pakalpojumu saistītus uzdevumus Windows instalācijas attēlā, neatkarīgi no tā, vai tas ir tiešsaistes attēls vai bezsaistes attēls mapē vai WIM failā. šis rīks varēja pievienot un atvienot attēlus, pievienot ierīces draiveri bezsaistes attēlam un vaicāt instalētos ierīces draiverus bezsaistes attēlā.
 



## Atsauces 

* [Windows attēlveidošanas formāts — Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)




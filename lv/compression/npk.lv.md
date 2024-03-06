{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "NPK faila formāts",
  "description":"Uzziniet par NPK faila formātu un API, kas var izveidot un atvērt NPK failus.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk-lv",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Kas ir NPK fails?

NPK fails ir programmatūras jaunināšanas pakotnes fails, ko **MikroTik** maršrutētāji izmanto maršrutētāja operētājsistēmas jaunināšanai. Tas ir saspiests binārais arhīvs, kas tiek ielādēts maršrutētājā programmatūras atjauninājumu instalēšanai. Informācija, kas atrodas NPK failos, ietver tīkla informāciju, piemēram, IP adresi un IP pakalpojumu, savienotāju informāciju (ethernet saskarnes un seriālo portu), e-pasta iestatīšanu, tilta konfigurāciju un vietējo lietotāju pārvaldību.

## NPK faila formāts

NPK faili tiek glabāti kā saspiests binārais arhīvs. Tas ir slēgts faila formāts, ko izmanto tikai paši MikroTik. Nav paredzēts izveidot RouterOS papildinājumus, izmantojot trešās puses. NPK failus uztur pats MikroTik, un to jauninātās versijas var lejupielādēt no [MikroTik](https://mikrotik.com/download) vietnes lejupielādes sadaļām.

Kad maršrutētājā tiek augšupielādēts NPK fails, maršrutētāja operētājsistēma nedarbojas, ja vien tā netiek pārstartēta. Tāpēc, lai varētu jaunināt maršrutētāja OS, ir nepieciešama restartēšana.

## Atsauces

* [MikroTik — maršrutētāja operētājsistēmas jaunināšana](https://mikrotik.com/download)

* [Kā izveidot NPK failus](https://forum.mikrotik.com/viewtopic.php?t=87126)



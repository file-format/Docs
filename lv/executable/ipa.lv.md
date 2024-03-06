{
  "date": "2021-08-30",
  "keywords": [
"ipa fails",
"ipa faila formāts",
"kas ir ipa fails",
"failu",
"ipa piemērs",
"ipa faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par IPA faila formātu un API, kas var izveidot un atvērt IPA failus.",
  "title": "IPA — iOS lietojumprogrammu pakotnes fails",
  "linktitle": "IPA",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ip-lva"
}
},
  "lastmod": "2021-08-30"
}

## Kas ir IPA fails?
Fails ar paplašinājumu .ipa pieder iOS un tiek dēvēts par lietojumprogrammu pakotnes failu. Šis ir arhīva fails (saspiests, izmantojot [ZIP](/compression/zip/) saspiešanu), kurā tiek saglabāta iOS lietojumprogramma, taču šo lietojumprogrammu var instalēt tikai MacOS ierīcēs, kuru pamatā ir iOS vai ARM, piemēram, iPad, iPhone vai iPod Touch. IPA failu instalēšanai var izmantot galvenokārt iTunes, Apple Configurator 2 vai jebkuru trešās puses programmatūru.

## IPA faila formāts
IOS izstrādātāji, kuri izstrādā lietotnes, izmantojot Apple Xcode, labi pārzina IPA failus, jo viņiem izstrādātās lietotnes ir jāiepako kā IPA faili, lai pārbaudītu lietotņu veikala izvietošanas nolūkos. Lai gan ir zināms, ka IPA faili ir instalēti kā iOS lietotnes, tomēr varat tos arī atspiest, lai skatītu ietvertos lietotņu datus. Tā kā IPA failā ir tikai viens mobilo tālruņu ARM arhitektūras binārs, bet x86 arhitektūrai tas nesatur, daudzus .ipa failus nevar instalēt iPhone simulatorā.
### .ipa faila struktūra
Šis piemērs parāda IPA struktūru:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Iepriekš minētā ir iebūvēta struktūra iTunes un App Store atpazīšanai. Saskaņā ar šo struktūru:
- Payload direktorijā ir visi lietotņu dati.
- iTunes Artwork fails ir 512 × 512 pikseļu PNG attēls, kurā ir ietverta lietotnes ikona, kas tiek rādīta iTunes un App Store lietotnē iPad.
- iTunesMetadata.plist satur dažādus informācijas bitus, sākot ar izstrādātāja vārdu un ID, informāciju par autortiesībām, paketes identifikatoru, lietotnes nosaukumu, žanru, izlaišanas datumu, pirkuma datumu utt.
- Mapē META-INF ir tikai metadati par to, kura programma tika izmantota, lai izveidotu IPA.


## Atsauces 

* [.ipa — Wikipedia](https://en.wikipedia.org/wiki/.ipa)




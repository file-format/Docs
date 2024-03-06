
{
  "date": "2022-02-06",
  "keywords": [
".apks failu",
"pagarinājumu",
"formātā",
"APK komplekta arhīvs",
"kā atvērt .apks failu",
"apks faila formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKS fails — APK kopas arhīvs",
  "description": "Uzziniet, kas ir APKS fails?",
  "linktitle": "APKS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-apk-lvs"
}
},
  "lastmod": "2022-02-06"
}

## Kas ir APKS fails?

Fails ar paplašinājumu .apks ir arhīva fails, kas ir Android pakotnes **APK** failu kolekcija. Katrs atsevišķais APK fails APKS failā tiek ģenerēts, ņemot vērā dažādus ierīču aspektus. Tie ietver arhitektūru, valodu, ekrāna blīvumu un citas ierīces funkcijas. APKS failus ģenerē **bundletool**. To izmanto, lai izveidotu Android App Bundle un konvertētu lietotņu komplektu dažādos APK failos izvietošanai ierīcēs.

## APKS faila formāts — plašāka informācija

APKS faili tiek saglabāti kā saspiesti faili, izmantojot [ZIP](/compression/zip/) faila formātu.

## Kā ģenerēt APKS failu?

Kad Android App Bundle (AAB) ir gatavs, tā darbību Google Play veikalā var pārbaudīt, lai to varētu ievietot ierīcē. Šim nolūkam APKS failus var ģenerēt no AAB failiem un instalēt testa ierīcēs, izmantojot Google Android [bundletool](https://developer.android.com/tools/bundletool). Tas nodrošina komandrindas rīkus, lai izveidotu APKS arhīva failu no APK, izmantojot šo komandu.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Lai ierīcē izvietotu APK, APKS failu var parakstīt ar ierīces parakstīšanas informāciju, kā norādīts tālāk.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Atsauces

 * [bundletool — komandrinda](https://developer.android.com/tools/bundletool)


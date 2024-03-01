
{
  "date": "2022-02-06",
  "keywords": [
".apks-tiedosto",
"laajennus",
"muoto",
"APK-sarjan arkisto",
"kuinka avata .apks-tiedosto",
"apks-tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKS-tiedosto - APK-sarjan arkisto",
  "description": "Lisätietoja siitä, mikä on APKS-tiedosto?",
  "linktitle": "APKS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-apk-fis"
}
},
  "lastmod": "2022-02-06"
}

## Mikä on APKS-tiedosto?

Tiedosto, jonka laajennus on .apks, on arkistotiedosto, joka on kokoelma Android-paketin **APK**-tiedostoja. Jokainen APKS-tiedoston yksittäinen APK-tiedosto luodaan laitteiden eri näkökohtia silmällä pitäen. Näitä ovat arkkitehtuuri, kieli, näytön tiheys ja muut laitteen ominaisuudet. APKS-tiedostot on luotu **bundletoolilla**. Sitä käytetään Android App Bundlen rakentamiseen ja sovelluspaketin muuntamiseen erilaisiksi APK:iksi laitteissa käyttöönotettaviksi.

## APKS-tiedostomuoto – lisätietoja

APKS-tiedostot tallennetaan pakattuina tiedostoina [ZIP](/compression/zip/)-tiedostomuodossa.

## Kuinka luoda APKS-tiedosto?

Kun Android App Bundle (AAB) on valmis, sen toimintaa Google Play -kaupassa voidaan testata laitteeseen asennettavaksi. APKS-tiedostoja voidaan luoda tätä tarkoitusta varten AAB-tiedostoista ja asentaa testilaitteisiin Googlen Androidin [bundletool](https://developer.android.com/tools/bundletool) avulla. Se tarjoaa komentorivityökalut APKS-arkistotiedoston luomiseen APK:ista seuraavan komennon avulla.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Jotta APK:t voidaan ottaa käyttöön laitteella, APKS-tiedosto voidaan allekirjoittaa laitteen allekirjoitustiedoilla seuraavasti.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Viitteet

 * [bundletool - komentorivi](https://developer.android.com/tools/bundletool)


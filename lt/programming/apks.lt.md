
{
  "date": "2022-02-06",
  "keywords": [
".apks failą",
"pratęsimas",
"formatu",
"APK rinkinio archyvas",
"kaip atidaryti .apks failą",
"apks failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKS failas – APK rinkinio archyvas",
  "description": "Sužinokite, kas yra APKS failas?",
  "linktitle": "APKS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-apk-lts"
}
},
  "lastmod": "2022-02-06"
}

## Kas yra APKS failas?

Failas su plėtiniu .apks yra archyvo failas, kuris yra Android paketo **APK** failų rinkinys. Kiekvienas atskiras APK failas APKS faile sugeneruojamas atsižvelgiant į įvairius įrenginių aspektus. Tai apima architektūrą, kalbą, ekrano tankį ir kitas įrenginio funkcijas. APKS failus generuoja **bundletool**. Jis naudojamas kuriant Android App Bundle ir konvertuojant programų paketą į skirtingus APK, skirtus diegti įrenginiuose.

## APKS failo formatas – daugiau informacijos

APKS failai išsaugomi kaip suglaudinti failai naudojant [ZIP](/compression/zip/) failo formatą.

## Kaip sugeneruoti APKS failą?

Kai Android App Bundle (AAB) yra paruoštas, jo veikimas Google Play parduotuvėje gali būti išbandytas, kad būtų galima įdiegti įrenginyje. Šiuo tikslu APKS failus galima sugeneruoti iš AAB failų ir įdiegti bandomuosiuose įrenginiuose naudojant Google Android [bundletool](https://developer.android.com/tools/bundletool). Jame pateikiami komandų eilutės įrankiai, skirti sukurti APKS archyvo failą iš APK naudojant šią komandą.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Norint įdiegti APK įrenginyje, APKS failas gali būti pasirašytas naudojant įrenginio pasirašymo informaciją, kaip nurodyta toliau.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Nuorodos

 * [bundletool – komandų eilutė](https://developer.android.com/tools/bundletool)



{
  "date": "2022-02-06",
  "keywords": [
".apks-fil",
"udvidelse",
"format",
"APK-sætarkiv",
"hvordan man åbner en .apks-fil",
"apks filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKS-fil - APK-sætarkiv",
  "description": "Lær om, hvad en APKS-fil er?",
  "linktitle": "APKS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-apk-das"
}
},
  "lastmod": "2022-02-06"
}

## Hvad er APKS fil?

En fil med filtypenavnet .apks er en arkivfil, der er en samling af Android-pakke-**APK**-filer. Hver enkelt APK-fil i APKS-filen genereres under hensyntagen til forskellige aspekter af enhederne. Disse omfatter arkitektur, sprog, skærmtæthed og andre enhedsfunktioner. APKS-filer genereres af **bundletool**. Det bruges til at bygge Android App Bundle og konvertere app bundle til forskellige APK'er til implementering på enheder.

## APKS-filformat - flere oplysninger

APKS-filer gemmes som komprimerede filer ved hjælp af filformatet [ZIP](/compression/zip/).

## Hvordan genererer man en APKS-fil?

Når Android App Bundle (AAB) er klar, kan dens adfærd i Google Play Butik testes til implementering på en enhed. APKS-filer kan til dette formål genereres fra AAB-filer og installeres på testenheder ved hjælp af Googles Android [bundletool](https://developer.android.com/tools/bundletool). Det giver kommandolinjeværktøjer til at oprette APKS-arkivfilen fra APK'er ved hjælp af følgende kommando.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

For at implementere APK'erne på en enhed kan APKS-filen signeres med enhedssigneringsoplysningerne som følger.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Referencer

 * [bundletool - kommandolinje](https://developer.android.com/tools/bundletool)


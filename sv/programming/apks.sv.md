
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS-fil - APK-uppsättningsarkiv",
  "description":"Läs mer om vad en APKS-fil är?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Vad är en APKS fil?

En fil med filtillägget .apks är en arkivfil som är en samling Android-paket **APK**-filer. Varje enskild APK-fil i APKS-filen genereras med hänsyn till olika aspekter av enheterna. Dessa inkluderar arkitektur, språk, skärmtäthet och andra enhetsfunktioner. APKS-filer genereras av **bundletool**. Det används för att bygga Android App Bundle och konvertera AAB-paket till olika APK-filer för distribution på enheter.

## APKS-filformat - Mer information

APKS-filer sparas som komprimerade filer i filformatet [ZIP](/sv/compression/zip/).

## Hur genererar man en APKS-fil?

När Android App Bundle (AAB) är klart kan dess beteende i Google Play Butik testas för implementering på en enhet. APKS-filer kan genereras, för detta ändamål, från AAB-filer och installeras på testenheter med hjälp av Googles Android [bundletool](https://developer.android.com/tools/bundletool). Den tillhandahåller kommandoradsverktyg för att skapa APKS-arkivfilen från APK:er med följande kommando.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

För att distribuera APK-filerna till en enhet kan APKS-filen signeras med enhetens signeringsinformation enligt följande.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Referenser

* [bundletool - kommandorad](https://developer.android.com/tools/bundletool)


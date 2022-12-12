
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor APKS – Archiv sady APK",
  "description":"Další informace o tom, co je soubor APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Co je soubor APKS?

Soubor s příponou .apks je archivní soubor, který je sbírkou souborů **APK** balíčku Android. Každý jednotlivý soubor APK v souboru APKS je generován s ohledem na různé aspekty zařízení. Patří mezi ně architektura, jazyk, hustota obrazovky a další funkce zařízení. Soubory APKS generuje **bundletool**. Používá se k sestavení balíčku Android App Bundle a převedení balíčku aplikací na různé soubory APK pro nasazení na zařízeních.

## Formát souboru APKS – Další informace

Soubory APKS se ukládají jako komprimované soubory ve formátu souboru [ZIP](/cs/compression/zip/).

## Jak vygenerovat soubor APKS?

Když je balíček Android App Bundle (AAB) připraven, jeho chování v obchodě Google Play lze otestovat pro nasazení do zařízení. Soubory APKS lze za tímto účelem vygenerovat ze souborů AAB a nainstalovat na testovací zařízení pomocí nástroje Android [bundletool] od Googlu (https://developer.android.com/studio/command-line/bundletool). Poskytuje nástroje příkazového řádku k vytvoření archivního souboru APKS z APK pomocí následujícího příkazu.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Chcete-li nasadit soubory APK do zařízení, lze soubor APKS podepsat pomocí informací o podpisu zařízení, jak je uvedeno níže.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Reference

* [bundletool – příkazový řádek](https://developer.android.com/studio/command-line/bundletool)


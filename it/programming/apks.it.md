
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File APK - Archivio set APK",
  "description":"Scopri cos'è un file APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Che cos'è un file APKS?

Un file con estensione .apks è un file di archivio che è una raccolta di file **APK** del pacchetto Android. Ogni singolo file APK nel file APKS viene generato tenendo in vista vari aspetti dei dispositivi. Questi includono architettura, lingua, densità dello schermo e altre funzionalità del dispositivo. I file APKS sono generati da **bundletool**. Viene utilizzato per creare Android App Bundle e convertire app bundle in APK diversi per la distribuzione sui dispositivi.

## Formato file APKS - Ulteriori informazioni

I file APKS vengono salvati come file compressi utilizzando il formato file [ZIP](/it/compression/zip/).

## Come generare un file APKS?

Quando l'Android App Bundle (AAB) è pronto, il suo comportamento su Google Play Store può essere testato per la distribuzione su un dispositivo. I file APKS possono essere generati, a tale scopo, da file AAB e installati su dispositivi di test utilizzando il [bundletool] di Google Android (https://developer.android.com/studio/command-line/bundletool). Fornisce strumenti da riga di comando per creare il file di archivio APKS dagli APK utilizzando il comando seguente.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Per distribuire gli APK su un dispositivo, il file APKS può essere firmato con le informazioni di firma del dispositivo come segue.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Riferimenti

* [bundletool - riga di comando](https://developer.android.com/studio/command-line/bundletool)


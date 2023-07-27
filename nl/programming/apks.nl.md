
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS-bestand - APK-setarchief",
  "description":"Meer informatie over wat een APKS-bestand is?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Wat is een APKS-bestand?

Een bestand met de extensie .apks is een archiefbestand dat een verzameling Android-pakket **APK**-bestanden is. Elk afzonderlijk APK-bestand in het APKS-bestand wordt gegenereerd met inachtneming van verschillende aspecten van de apparaten. Deze omvatten architectuur, taal, schermdichtheid en andere apparaatfuncties. APKS-bestanden worden gegenereerd door **bundletool**. Het wordt gebruikt om Android App Bundle te bouwen en app-bundels om te zetten in verschillende APK's voor implementatie op apparaten.

## APKS-bestandsindeling - Meer informatie

APKS-bestanden worden opgeslagen als gecomprimeerde bestanden met de bestandsindeling [ZIP](/nl/compression/zip/).

## Hoe een APKS-bestand genereren?

Wanneer de Android App Bundle (AAB) gereed is, kan het gedrag ervan in de Google Play Store worden getest voor implementatie op een apparaat. Voor dit doel kunnen APKS-bestanden worden gegenereerd uit AAB-bestanden en op testapparaten worden geïnstalleerd met behulp van Google's Android [bundletool](https://developer.android.com/tools/bundletool). Het biedt opdrachtregelhulpmiddelen om het APKS-archiefbestand van APK's te maken met behulp van de volgende opdracht.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Om de APK's op een apparaat te implementeren, kan het APKS-bestand als volgt worden ondertekend met de ondertekeningsinformatie van het apparaat.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Referenties

* [bundeltool - opdrachtregel](https://developer.android.com/tools/bundletool)


{
  "date" : "2019-10-11",
  "keywords" :[ "apk-bestand", "apk-bestandsindeling", "wat is een apk-bestand", "bestand", "apk-voorbeeld", "apk-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Wat is een APK-bestand?",
  "description":"Leer te weten wat een APK-bestand is en wat API's zijn die APK-bestanden kunnen maken en openen.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Wat is een APK-bestand?

Een bestand met de extensie .apk is een Google Android app-bestand dat wordt gebruikt om apps (applicaties) op de Android-apparaten te installeren. Het is gemaakt als een uitvoerbaar bestand met behulp van de officiële IDE Google Android Studio en wordt geüpload naar de Google Play Store om te worden gedownload en geïnstalleerd door eindgebruikers. APK-bestanden kunnen worden gegenereerd en beschikbaar worden gemaakt voor handmatige installatie en ook voordat ze naar de Google Play Store worden gepubliceerd. Dit helpt bij het testen van de functionaliteit en het gedrag van het gegenereerde APK-pakketbestand. Daarom moet men er zeker van zijn dat het APK-bestand afkomstig is van een vertrouwde bron en geen malware bevat.

## APK-bestandsindeling

APK-bestanden zijn verpakt als gecomprimeerd in [ZIP](/nl/compression/zip/) bestandsformaat dat kan worden geopend met elke software voor het openen van ZIP-bestanden. De .apk-extensie van een dergelijk bestand kan worden hernoemd naar .zip en het bestand openen in een ZIP-toepassing of de inhoud uitpakken.

## APK-pakketinhoud

Een enkel APK-bestand bevat alle benodigde bestanden die nodig zijn voor de installatie en uitvoering. Een APK-bestand, wanneer uitgepakt met een ZIP-toepassing, bevat de volgende bestanden en mappen.

* `META-INF/`: map die het manifestbestand, de handtekening en een lijst met bronnen in het archief bevat
* `lib/`: Directory met gecompileerde code gerelateerd aan specifieke platforms zoals armeabi-v7a, x86, arm64-v8a, etc.
* `res/`: Directory met niet-gecompileerde bronnen zoals afbeeldingen
* `assets/`: Directory met applicatie-assets, die kunnen worden opgehaald door AssetManager.
* `androidManifest.xml`: bevat de naam, versie-informatie en inhoud van het APK-bestand
* `classes.dex`: dit zijn gecompileerde Java-klassen die kunnen worden uitgevoerd op de virtuele Dalvik-machine en door de Android Runtime
* `resources.arsc`: samengesteld bronnenbestand zoals strings

## Hoe installeer ik een APK-bestand op een Android-apparaat?

Om een APK-bestand op uw Android-apparaten te installeren, kunnen de volgende stappen worden gebruikt.

1. Download de APK met een webbrowser
2. Tik erop - je zou het dan moeten kunnen zien downloaden in de bovenste balk van je apparaat
3. Zodra het is gedownload, opent u Downloads, tikt u op het APK-bestand en tikt u op Ja wanneer daarom wordt gevraagd.

Als u deze stappen volgt, wordt de installatie van de app op uw apparaat gestart.

## Referenties

* [APK-bestandsindeling](https://en.wikipedia.org/wiki/Android_application_package)


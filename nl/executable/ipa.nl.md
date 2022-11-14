{
  "date" : "2021-08-30",
  "keywords" :[ "ipa-bestand", "ipa-bestandsformaat", "wat is een ipa-bestand", "bestand", "ipa-voorbeeld", "ipa-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over IPA-bestandsindeling en API's die IPA-bestanden kunnen maken en openen.",
  "title" :"IPA - iOS-toepassingspakketbestand",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Wat is een IPA-bestand?
Een bestand met de extensie .ipa behoort tot de iOS en staat bekend als toepassingspakketbestand. Dit is een archiefbestand (gecomprimeerd met [ZIP](/nl/compression/zip/)-compressie) waarin een iOS-toepassing is opgeslagen, maar die toepassing kan alleen worden geïnstalleerd op een iOS- of ARM-gebaseerd MacOS-apparaat, zoals een iPad, iPhone of iPod touch. Voornamelijk iTunes, Apple Configurator 2 of software van derden kan worden gebruikt om IPA-bestanden te installeren.

## IPA-bestandsindeling
De IOS-ontwikkelaars die de apps ontwikkelen met behulp van de Apple Xcode zijn goed bekend met IPA-bestanden omdat ze hun ontwikkelde apps als IPA-bestanden moeten verpakken, hetzij voor het testen van de implementatie van de app store. Hoewel bekend is dat de IPA-bestanden zijn geïnstalleerd als iOS-apps, kunt u ze ook decomprimeren om de app-gegevens te bekijken. Aangezien een IPA-bestand slechts één binair bestand bevat voor de ARM-architectuur van mobiele telefoons en geen binair bestand voor de x86-architectuur, kunnen veel .ipa-bestanden niet op de iPhone Simulator worden geïnstalleerd.
### Structuur van een .ipa-bestand
Het volgende voorbeeld toont de structuur van een IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Het bovenstaande is een ingebouwde structuur die iTunes en App Store kunnen herkennen. Volgens deze structuur:
- De Payload-directory bevat alle app-gegevens.
- Het iTunes Artwork-bestand is een PNG-afbeelding van 512 × 512 pixels, met het pictogram van de app voor weergave in iTunes en de App Store-app op de iPad.
- De iTunesMetadata.plist bevat verschillende stukjes informatie, variërend van de naam en ID van de ontwikkelaar, de copyrightinformatie, de bundelidentificatie, de naam van de app, het genre, de releasedatum, de aankoopdatum, enz.
- De map META-INF bevat alleen metadata over welk programma is gebruikt om de IPA te maken.


## Referenties

* [.ipa - door Wikipedia](https://en.wikipedia.org/wiki/.ipa)



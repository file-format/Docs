{
  "date": "2021-08-30",
  "keywords": [
"ipa fil",
"ipa filformat",
"hvad er en ipa fil",
"fil",
"ipa eksempel",
"ipa filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om IPA-filformat og API'er, der kan oprette og åbne IPA-filer.",
  "title": "IPA - iOS Application Package File",
  "linktitle": "IPA",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ip-daa"
}
},
  "lastmod": "2021-08-30"
}

## Hvad er en IPA fil?
En fil med filtypenavnet .ipa tilhører iOS og er kendt som programpakkefil. Dette er en arkivfil (komprimeret ved hjælp af [ZIP](/compression/zip/)-komprimering), som gemmer en iOS-applikation, men den applikation kan kun installeres på en iOS- eller ARM-baseret MacOS-enhed, såsom en iPad, iPhone eller iPod Touch. Hovedsageligt kan iTunes, Apple Configurator 2 eller enhver tredjepartssoftware bruges til at installere IPA-filer.

## IPA filformat
De IOS-udviklere, der udvikler apps ved hjælp af Apple Xcode, er godt bekendt med IPA-filer, fordi de skal pakke deres udviklede apps som IPA-filer, enten for at teste app-butikkens implementeringsformål. Selvom IPA-filerne er kendt for at være installeret som iOS-apps, kan du dog også dekomprimere dem for at se de indeholdte appdata. Da en IPA-fil kun indeholder én binær fil til ARM-arkitekturen på mobiltelefoner, og den ikke indeholder en binær fil til x86-arkitekturen, kan mange .ipa-filer ikke installeres på iPhone-simulatoren.
### Struktur af en .ipa-fil
Følgende eksempel viser strukturen af en IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Ovenstående er en indbygget struktur, som iTunes og App Store kan genkende. I henhold til denne struktur:
- Nyttemappen indeholder alle appdata.
- iTunes Artwork-filen er et 512×512 pixel PNG-billede, der indeholder appens ikon til visning i iTunes og App Store-appen på iPad.
- iTunesMetadata.plist indeholder forskellige informationsbidder, lige fra udviklerens navn og id, copyright-oplysninger, bundle-id, navnet på appen, genre, udgivelsesdato, købsdato osv.
- META-INF mappen indeholder kun metadata om hvilket program der blev brugt til at oprette IPA'en.


## Referencer 

* [.ipa - af Wikipedia](https://en.wikipedia.org/wiki/.ipa)




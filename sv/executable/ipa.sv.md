{
  "date" : "2021-08-30",
  "keywords" :[ "ipa-fil", "ipa-filformat", "vad är en ipa-fil", "fil", "ipa-exempel", "ipa-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om IPA-filformat och API:er som kan skapa och öppna IPA-filer.",
  "title" :"IPA - iOS Application Package File",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Vad är en IPA fil?
En fil med filtillägget .ipa tillhör iOS och kallas applikationspaketfil. Detta är en arkivfil (komprimerad med [ZIP](/sv/compression/zip/)-komprimering) som lagrar en iOS-applikation, men den applikationen kan bara installeras på en iOS- eller ARM-baserad MacOS-enhet, som en iPad, iPhone eller Ipod Touch. Huvudsakligen kan iTunes, Apple Configurator 2 eller annan programvara från tredje part användas för att installera IPA-filer.

## IPA-filformat
IOS-utvecklarna som utvecklar apparna med hjälp av Apple Xcode är väl bekanta med IPA-filer eftersom de måste paketera sina utvecklade appar som IPA-filer antingen för att testa appbutikens distributionsändamål. Även om IPA-filerna är kända för att vara installerade som iOS-appar, men du kan också dekomprimera dem för att se appdata som finns. Eftersom en IPA-fil endast innehåller en binär fil för ARM-arkitekturen för mobiltelefoner och den inte innehåller en binär för x86-arkitekturen, kan många .ipa-filer inte installeras på iPhone-simulatorn.
### Strukturen för en .ipa-fil
Följande exempel visar strukturen för en IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Ovanstående är en inbyggd struktur för iTunes och App Store att känna igen. Enligt denna struktur:
- Payload-katalogen innehåller all appdata.
- iTunes Artwork-filen är en 512×512 pixlar PNG-bild, som innehåller appens ikon för visning i iTunes och App Store-appen på iPad.
- iTunesMetadata.plist innehåller olika bitar av information, allt från utvecklarens namn och ID, upphovsrättsinformation, paketidentifierare, namnet på appen, genre, releasedatum, inköpsdatum, etc.
- Mappen META-INF innehåller endast metadata om vilket program som användes för att skapa IPA:n.


## Referenser

* [.ipa - av Wikipedia](https://en.wikipedia.org/wiki/.ipa)



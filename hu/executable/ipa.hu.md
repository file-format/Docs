{
  "date" : "2021-08-30",
  "keywords" :[ "ipa fájl", "ipa fájl formátum", "mi az ipa fájl", "fájl", "ipa példa", "ipa fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az IPA fájlformátumról és az API-król, amelyek IPA-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"IPA – iOS alkalmazáscsomag fájl",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Mi az IPA fájl?
Az .ipa kiterjesztésű fájl az iOS rendszerhez tartozik, és alkalmazáscsomagfájlként ismert. Ez egy archív ([ZIP](/hu/compression/zip/) tömörítéssel tömörített) fájl, amely egy iOS alkalmazást tárol, de az alkalmazás csak iOS vagy ARM alapú MacOS eszközökre telepíthető, például iPad, iPhone vagy iPod touch. Elsősorban az iTunes, az Apple Configurator 2 vagy bármely harmadik féltől származó szoftver használható az IPA-fájlok telepítésére.

## IPA fájlformátum
Az Apple Xcode-ot használó alkalmazásokat fejlesztő IOS-fejlesztők jól ismerik az IPA-fájlokat, mert a kifejlesztett alkalmazásaikat IPA-fájlként kell csomagolniuk az alkalmazásbolt-telepítés teszteléséhez. Bár az IPA-fájlokról ismert, hogy iOS-alkalmazásként vannak telepítve, de kicsomagolhatja őket az alkalmazás adatainak megtekintéséhez. Mivel egy IPA fájl csak egy binárist tartalmaz a mobiltelefonok ARM architektúrájához, és nem tartalmaz binárist az x86 architektúrához, sok .ipa fájl nem telepíthető az iPhone Simulatorra.
### Az .ipa fájl szerkezete
A következő példa az IPA felépítését mutatja be:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
A fenti egy beépített struktúra az iTunes és az App Store felismeréséhez. Ennek a szerkezetnek megfelelően:
- A Payload könyvtár tartalmazza az összes alkalmazásadatot.
- Az iTunes Artwork fájl egy 512 × 512 pixeles PNG-kép, amely tartalmazza az alkalmazás ikonját az iTunesban és az iPad App Store alkalmazásban való megjelenítéséhez.
- Az iTunesMetadata.plist különféle információkat tartalmaz, kezdve a fejlesztő nevétől és azonosítójától, a szerzői jogi információktól, a csomagazonosítótól, az alkalmazás nevétől, műfajtól, megjelenési dátumtól, vásárlás dátumától stb.
- A META-INF mappa csak metaadatokat tartalmaz arról, hogy milyen programot használtak az IPA létrehozásához.


## Hivatkozások

* [.ipa – a Wikipedia által](https://en.wikipedia.org/wiki/.ipa)



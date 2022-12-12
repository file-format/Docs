{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S File - Mi az M4S fájl?",
  "description":"További információ az M4S fájlformátumról és az API-król, amelyek M4S fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Mi az M4S fájl?

Az M4S-fájl egy videó kis részlete, amelyet az **MPEG-DASH** adatfolyam-technikával az interneten streamelnek. Egy videó szegmenst tartalmaz bináris adatok formájában. A fogadó alkalmazás (általában webböngésző vagy médialejátszó) a vételi sorrendben játssza le ezeket a szegmenseket. Az első M4S szegmenst a benne lévő inicializálási adatok azonosítják. **összefoglalva**, az M4S-fájlok egy teljes fájl kis, egyedi médiaszegmensei.

## M4S fájlformátum

Az M4S-fájlok az [ISO Base Media File (ISOBMFF) formátumon] (https://www.w3.org/TR/mse-byte-stream-format-isobmff/) alapulnak. Egy nagy fájlnak ezek a kis szegmensei egymástól függetlenül letölthetők HTTP-n keresztül. Így ha nagy [MP4](/hu/video/mp4/) filmfájlja van, akkor az MPEG-DASH (Dynamic Adaptive Streaming over HTTP) technikával M4S szegmensfájlokként szegmentálva továbbítható. Ha ezt a nagy filmfájlt M4S-ként tölti le a lemezre, akkor több M4S-fájl is letöltődik. Ha ezeket az .m4s szegmenseket összefűzi, egy teljes lejátszható fájl jön létre. A médialejátszók csak akkor tudják lejátszani a fájlt, ha az első inicializálási szegmens is elérhető a fájlhoz.

## Az MPEG-DASH streamingről

Az MPEG-DASH adaptív bitrátájú adatfolyam-technikát használ, amely lehetővé teszi a kiváló minőségű médiatartalom interneten keresztüli streamelését. Ez úgy történik, hogy a tartalmat kis szegmensek sorozatára bontja, amelyeket HTTP-n keresztül streamelnek. Nagy médiafájlok, például filmek, podcastok vagy egy sportesemény élő közvetítése streamelhetők így. Ezek a szegmensek különböző bitsebességgel vannak kódolva. Az MPEG-DASH kompatibilis médialejátszók automatikusan kiválasztják a legnagyobb bitsebességű szegmenst egy bitsebesség-adaptációs algoritmus segítségével. Ezzel elkerülhető az események elakadása vagy újrapufferelése a lejátszás során.

### Nyílt forráskódú API M4S-fájlokhoz

Vannak nyílt forráskódú API-k, amelyek M4S-fájlok olvasására és konvertálására használhatók.

* [libdash](https://github.com/bitmovin/libdash) – .NET API M4S-fájlokhoz
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) – Javascript kliens M4S-fájlhoz
* [Go Library for Create Dash Files](https://github.com/zencoder/go-dash)

### Nyílt forráskódú API az M4S MP4-re konvertálásához

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referenciák ###

* [ISO Base Media File (ISOBMFF) formátum](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dinamikus adaptív adatfolyam HTTP-n keresztül – MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)


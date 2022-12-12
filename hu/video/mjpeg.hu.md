{
  "date" : "2021-02-15",
  "keywords" :[ "MJPEG", "fájl", "kiterjesztés", "formátum", "Motion JPEG", "tömörítés", "JPEG kép", "videó"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJPEG - Motion JPEG fájlformátum",
  "description":"További információ az MJPEG fájlformátumról és az API-król, amelyek MJPEG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MJPEG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Mi az az MJPEG fájl? ##

Az .mjpeg (Motion JPEG) kiterjesztésű fájl olyan videofájl, amely egy különálló videokocka JPEG-képként való tömörítésével jön létre. Ez eltér a szabványos MPEG-1 és MPEG-2 fájlformátumoktól, ahol a tömörítés interframe, és a következő képkockák tartalmának előrejelzése alapján történik. Az MJPEG-et számos alkalmazás támogatja, beleértve a webböngészőket, médialejátszókat, digitális fényképezőgépeket, webkamerákat és streaming szervereket. Az MJPEG fájlformátumot használni kívánó alkalmazásokhoz beépülő modulok állnak rendelkezésre.

## MJPEG fájlformátum ##

Az MJPEG a kiforrott tömörítési szabványon, azaz a [JPEG](/hu/image/jpeg/)-en alapul, amely jól definiált könyvtárakkal rendelkezik. Nem szabványosítható az olyan szabványokhoz, mint például az MPEG-2, és nem áll rendelkezésre olyan dokumentáció, amely a „Motion JPEG” teljes specifikációjaként hivatkozhatna. Ilyen szabvány hiányában a különböző gyártók kimenetei kompatibilitási problémákat vethetnek fel. Az olyan cégek azonban, mint a Microsoft és az Apple, dokumentálták, hogyan tárolják az M-JPEG fájlokat natív formátumukban, például [AVI](/hu/video/avi/) és [QT](/hu/video/qt/). Az [rfc2435](https://tools.ietf.org/html/rfc2435) leírja a JPEG-ben tömörített videók RTP Payload formátumát, és referenciaanyagként tekinthető meg.

## Hivatkozások ##

- [RFC2435 – RTP Payload Format for JPEG-Compressed Video](https://tools.ietf.org/html/rfc2435)
- [Motion JPEG - Wikipedia](https://en.wikipedia.org/wiki/Motion_JPEG)


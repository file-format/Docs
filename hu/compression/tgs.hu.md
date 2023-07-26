{
  "date" : "2019-10-11",
  "keywords" :[ "tgs fájl", "tgs fájlformátum", "mi az a tgs fájl", "fájl", "tgs példa", "tgs fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Telegram Animated Sticker File Format",
  "description":"További információ a TGS-fájlformátumról és az API-król, amelyek TGS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Mi az a TGS fájl?

A .tgs kiterjesztésű fájl egy animált matricafájl, amelyet a többplatformos üzenetküldő szolgáltatás, a [Telegram](https://core.telegram.org/stickers#animated-stickers) vezetett be. Az üzenetküldő alkalmazások felhasználói animált matricákat használnak, hogy továbbfejlesztett és élénkebb tartalmat küldjenek az üzenetekben, ellentétben a statikus grafikákkal, amelyek állóképek. A Telegram kezdetben a [WEBP](/hu/image/webp/) fájlformátumot használta az állóképmatricákhoz. A TGS fájlformátum nagyobb felbontásban és kisebb fájlméretben képes animációs adatokat tárolni, mint a statikus WEBP matricák. A TGS-fájlok megnyithatók olyan alkalmazásokkal, mint a Telegram, a 7-zip, az Apple Archive Utility és a Corel WinZip.

## TGS fájlformátum

A Telegram 2019 júliusában vezette be a TGS fájlformátumot a Lottie könyvtár alapján. A TGS-fájl [JSON](/hu/web/json/) szövegből áll, amelyet az Adobe After Effects animációjából exportálnak. Az exportált JSON-szöveg tömörítése gzip-tömörítéssel történik, amely csökkenti a fájl méretét. A szövegfájlról szóló JSON-információkat a rendszer szövegfájlban tárolja, amely a magas tömörítési arány alapja lesz.

### TGS matricák specifikációi

A TGS fájlformátum bizonyos korlátozásokat támaszt a TGS animált matricák létrehozásával kapcsolatban. Egy TGS animált fájl:

* A matrica/vászon méretének 512 × 512 képpontnak kell lennie.
* A matricatárgyak nem hagyhatják el a vásznat.
* Az animáció hossza nem haladhatja meg a 3 másodpercet.
* Minden animációnak hurkoltnak kell lennie.
* A matrica mérete nem haladhatja meg a 64 KB-ot a Bodymovinben történő renderelés után.
* Minden animációnak 60 képkocka/másodperc sebességgel kell futnia.

### Minta TGS JSON szöveg

Kibontott animált matrica a következő JSON-szövegtartalmat tartalmazza.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referenciák ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipédia](https://en.wikipedia.org/wiki/Gzip)


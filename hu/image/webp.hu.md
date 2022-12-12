{
  "date" : "2019-10-11",
  "keywords" :[ "webp fájl", "webp fájlformátum", "mi az a webp fájl", "fájl", "webp példa", "webp fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Google Raster Image File Format",
  "description":"További információ a WEBP fájlformátumról és az API-król, amelyek WEBP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a WEBP fájl?

A Google által bevezetett WebP egy modern raszteres webes képfájl formátum, amely veszteségmentes és veszteséges tömörítésen alapul. Ugyanolyan képminőséget biztosít, miközben jelentősen csökkenti a képméretet. Mivel a weboldalak többsége képeket használ az adatok hatékony reprezentációjaként, a WebP-képek használata weboldalakon a weboldalak gyorsabb betöltését eredményezi. A Google szerint a WebP veszteségmentes képek 26%-kal kisebbek a [PNG](/hu/image/png/) formátumokhoz képest, míg a WebP veszteséges képek 25-34%-kal kisebbek, mint a hasonló [JPEG](/hu/image/jpeg/) képek. A képeket a szerkezeti hasonlóság (SSIM) index alapján hasonlítja össze a WebP és más képfájlformátumok között. A WebP a [WebM](https://en.wikipedia.org/wiki/WebM) multimédiás tároló formátum testvérprojektje.

## WebP szolgáltatások áttekintése ##

A WebP-képek a tömörítési eljárást a környező blokkokból származó pixelek előrejelzésén alapuló tömörítési eljárást alkalmazzák, aminek eredményeként a képpontok többször használhatók egyetlen fájlban. Támogatja az animált képeket, és várhatóan több funkciót is támogat a jövőben. A Google elérhetővé tette a forráskódot [online](https://developers.google.com/speed/webp/download) kódolójához és dekódolójához, hogy szükség esetén használható legyen. A WebP lemezkép a következőket támogatja:

* **Veszteséges tömörítés:** A veszteséges tömörítés a [VP8](http://en.wikipedia.org/wiki/VP8) kulcskeret kódolásán alapul. A VP8 egy videotömörítési formátum, amelyet az On2 Technologies hozott létre a VP6 és VP7 formátumok utódjaként.
* **Veszteségmentes tömörítés:** A veszteségmentes tömörítési formátumot a WebP csapata fejlesztette ki.
* **Átlátszóság:** A 8 bites alfa-csatorna grafikus képekhez hasznos. Az Alpha-csatorna a veszteséges RGB-vel együtt használható, amely funkció jelenleg semmilyen más formátummal nem érhető el.
* **Animáció:** Támogatja a valódi színű animált képeket.
* **Metaadatok:** EXIF- és XMP-metaadatai lehetnek (például kamerák).
* **Színprofil:** Lehet, hogy beágyazott ICC-profilja van.

A veszteséges WebP-tömörítés prediktív kódolást használ a képek kódolásához, ugyanazt a módszert, amelyet a VP8 videokodek a videók kulcskockáinak tömörítésére használ. A prediktív kódolás a szomszédos pixelblokkok értékeit használja a blokkban lévő értékek előrejelzésére, majd csak a különbséget kódolja.

A veszteségmentes WebP tömörítés a már látott képrészleteket használja fel az új képpontok pontos rekonstruálására. Helyi palettát is használhat, ha nem talál érdekes egyezést.

## Fájlformátum ##

A WebP fájlformátum a RIFF (erőforráscsere fájlformátum) dokumentumformátumon alapul. A WebP konténer több és több funkciót is támogat, nem csak egyetlen képet tartalmaz VP8 kulcskeretként kódolva. A RIFF fájl alapvető eleme egy darab, amely a következőkből áll:


|Mező|Leírás
---|---|
|Chunk FourCC: 32 bites|Négy karakteres ASCII kód a csonk azonosítására
|Chunk Size: 32 bit (uint32)|A darab mérete nem tartalmazza ezt a mezőt, a darabazonosítót vagy a kitöltést
|Részlet hasznos terhelés: Részletméret bájt|Az adatterhelés. Ha a darab mérete páratlan, a rendszer hozzáad egy ~-~- kitöltési bájtot, amelynek 0 ~-~- kell lennie.
|ChunkHeader ('ABCD')|Az egyes darabok FourCC és Chunk Size fejlécének leírására szolgál, ahol az 'ABCD' a darab FourCC-je. Ennek az elemnek a mérete 8 bájt.

### WebP fejléc ###

A WebP fájl fejléce a következő:

* RIFF fejléc – 32 bit, amely az ASCII karaktereket reprezentálja: 'R' 'I' 'F' 'F'
* Fájlméret - 32 bit (uint32), amely a fájl méretét jelöli bájtokban, 8-as eltolástól kezdve. Ennek a mezőnek a maximális értéke 2^32 mínusz 10 bájt, így a teljes fájl mérete legfeljebb 4 GiB mínusz 2 bájt .
* 'WEBP' - 32 bit, amely az ASCII karaktereket képviseli 'W' 'E' 'B' 'P'

### Veszteséges fájlformátum ###

A WebP képek veszteséges fájlformátumot használnak, ha a kép veszteséges kódoláson alapul, és nem igényel speciális/kibővített funkciókat, mint például az átlátszóság, animáció, alfa stb. A veszteséges képek kisebbek, és a régebbi alkalmazások is támogatják őket.

A WebP fájl ebben az esetben a következőkből áll:

* 12 bájtos WebP fájlfejléc
* VP8 darab

A [VP8 adatformátum- és dekódolási útmutató] (https://tools.ietf.org/html/rfc6386) bemutatja a VP8 bitfolyam-formátum specifikációit.

### Veszteségmentes fájlformátum ###

Ez az elrendezés akkor használatos, ha a kép veszteségmentes kódoláson alapul, és nincs szükség a külső formátum által biztosított speciális szolgáltatásokra. Előfordulhat azonban, hogy a régebbi alkalmazások nem képesek olvasni az ilyen fájlokat.

A WebP fájl ebben az esetben a következőkből áll:

* 12 bájtos WebP fájlfejléc
* VP8L darab

## Referenciák ##

* [WebP fejlesztői referencia – a Google-tól](https://developers.google.com/speed/webp/)
* [WebP fájlformátum – Wikipédia](https://en.wikipedia.org/wiki/WebP)


{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKS fájlformátum",
  "keywords" :[ "mks", "matroska videó", "mkv formátum", "fájl", "formátum", "videó"],
  "description":"További információ az MKS fájlformátumról a csak a Matroska által létrehozott feliratokhoz és az MKS-fájlok létrehozására és megnyitására képes API-król.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Mi az MKS fájl?

Az MKS-fájlokat általában csak feliratokat tartalmazó Matroska-fájlokként ismerik. Bár a Matroska egy általános fájltároló, elkerüli az egyes formátumok információinak megtartását. Mivel egyes hang- vagy videótárolókban feliratokat használnak, a Matroska odafigyel néhány általános feliratformátum tárolására. Segít Matroskának, hogy összhangban legyen a növekedési rátával. A feliratok Matroskában való tárolásához kövesse az alábbi pontokat:

- A „.mks”. a kiterjesztést a Matroska fájl fogja használni (csak feliratot tartalmaz).
- A **CodecPrivate** az összes kodekkel kapcsolatos információ tárolására szolgál, amelyek globálisak egy teljes adatfolyamra vonatkozóan.
- Távolítsa el a kezdeti és leállítási időbélyegeket, amelyeket az időbélyegző natív tárolási formátumában használnak. Ehelyett használja a Blocks időbélyegzőt és az időtartamot.
- Bármit használhatsz átlátszó réteggel, beleértve a videót is.

## Általános feliratformátumok

Íme néhány rövid megjegyzés a Matroskában tárolt gyakoribb feliratformátumokról:

### Képek Feliratok
A VobSub feliratformátum az első képfelirat-formátum, amelyet a Matroskába importálnak. Ez a formátum a feliratok DVD-ről történő exportálásával jön létre. Ha a VobSub több adatfolyamból áll, a sávokat el kell választani a Matroskában való tárolás során.

### SRT-feliratok
Az SRT a legegyszerűbb és legalapvetőbb feliratformátumok közül. Négy részből áll, az alábbiak szerint:
 



1. Egy szám, amely a felirat sorrendjét jelzi.
2. A felirat megjelenési és eltűnési ideje a képernyőn.
3. Maga a felirat.
4. Egy üres sor a következő felirat kezdetének jelzésére.
 



### SSA/ASS feliratok
A Sub Station Alpha (SSA) a népszerű SubStation Alpha feliratszerkesztő által használt fájlformátum. Az SSA feliratokat széles körben használják a rajongók. Képes a modern funkciók megjelenítésére, pl. karaoke, pozicionálás, stílus stb.
 



### WebVTT Feliratok
A World Wide Web Consortium (W3C) kifejlesztette a WebVTT-t, amelynek rövidítése „Web Video Text Tracks Format”. Ezt a formátumot használják a külső szövegsáv-erőforrások megjelölésére a HTML elemmel kapcsolatban.

### HDMV bemutató grafikus feliratok
A HDMV prezentációs grafikus feliratformátum (HDMV PGS) bittérképek sorozata, és egyáltalán nem mondhatjuk szövegnek. Más szóval, azt mondhatjuk, hogy ez csak grafikus képek időzített sorozata. Az információ kinyeréséhez a PGS-t SRT-vé kell konvertálni.

### HDMV szöveges feliratok
A HDMV-szöveg a Blu-ray lemezeken használt szöveges feliratformátumként ismert. A Matroska csak az UTF-8 karakterkészletet engedélyezi When tárolja a TextST feliratokat.

### Digital Video Broadcasting (DVB) feliratok
A DVB feliratformátumot több nyelvű feliratozás TV-jeleken történő átvitelének és megjelenítésének szabályozására vezették be. Egy tipikus feliratozási formátum azt is lehetővé tenné bármely néző számára, hogy DVB-feliratos adásokat nézzen, függetlenül az átviteli rendszerek gyártójától.


## Referenciák ##

- [Matroska Feliratok](https://www.matroska.org/technical/subtitles.html)


{
  "date" : "2019-10-11",
  "keywords" :[ "mng fájl", "mng fájl formátum", "mi az mng fájl", "fájl", "mng példa", "mng fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MNG Fájlformátum - Többképes hálózati grafikus fájlformátum",
  "description":"További információ az MNG-fájlformátumról és az MNG-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az MNG fájl?

Az .mng kiterjesztésű fájl egy többképes hálózati grafikai fájlformátum, amely hasonló a [PNG](/hu/image/png/) képformátumhoz, de támogatja az animált képeket. Úgy fejlesztették ki, hogy elkerülje a PNG formátum túlterhelését az animációk további funkciójával. Az MNG is hasonló a [GIF](/hu/image/gif/) fájlokhoz, de több tömörítést használ, és támogatja a teljes alfa funkciót. Az MNG fájlok nem hivatalos MIME médiatípusa a video/x-mng. Az MNG-fájlok megnyithatók olyan alkalmazásokban, mint az ImageMagik és az IrfanView.

## MNG fájl formátum

Az MNG-fájlformátum hasonló a PNG-hez, és ugyanazt a csonk-struktúrát használja, mint a PNG-specifikációkban. Az MNG dekódernek képesnek kell lennie a PNG adatfolyamok dekódolására anélkül, hogy a dekódolási utasításokhoz speciális zászlókat adna meg. Az MNG több képet egy "keretbe" csoportosít, és néhány képet spriteként használnak az egyik helyről a másikra való mozgatáshoz. A mechanizmus lehetővé teszi a képadatok újrafelhasználását azok újraküldése nélkül. Az [MNG-specifikációk] (http://www.libpng.org/pub/mng/spec/) a fejlesztők számára elérhetők.

### MNG aláírás

Az MNG adatfolyam egy 8 bájtos aláírással kezdődik, amely a következőket tartalmazza:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Ez hasonló a PNG aláíráshoz, de PNG helyett MNG-t tartalmaz.

### MNG Frame

Az MNG-keret kisebb képek kétdimenziós képéből áll. Minden kis kép a sor és oszlop index kombinációjával érhető el. A formátum képes háromdimenziós "voxel" adatok tárolására, amelyek kétdimenziós síkok sorozatában vannak elrendezve. Minden síkot egy PNG vagy Delta-PNG adatfolyam képvisel. Minden Delta-PNG adatfolyam a szülő PNG-képtől való eltérésként határoz meg egy képet. Ez sokkal kompaktabb módot biztosít a következő képek megjelenítésére, mintha mindegyikhez teljes PNG adatfolyamot használnánk.

## Referenciák ##

* [MNG](http://www.libpng.org/pub/mng/)
* [MNG formátum v1.0](http://www.libpng.org/pub/mng/spec/)


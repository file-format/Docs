{
  "date" : "2019-10-11",
  "keywords" :[ "ico fájl", "ico fájl formátum", "mi az ico fájl", "fájl", "ico példa", "ico fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Képfájl formátum",
  "description":"További információ az ICO fájlformátumról és az API-król, amelyek ICO fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az ICO fájl?

Az ICO kiterjesztésű fájlok képfájltípusok, amelyek ikonként használhatók az alkalmazások [Microsoft Windowson] (https://www.microsoft.com/en-us/windows) ábrázolására. Ezek különböző méretben, színtámogatásban és felbontásban készülnek, hogy megfeleljenek a kijelző követelményeinek. Egy másik hasonló képfájlformátum a Microsoft Windows rendszeren a [CUR](/hu/image/cur/) a kurzor megjelenítéséhez, és egy hotspotot határoz meg a kép fejlécében. MacOS rendszeren az ICNS fájlformátumok ugyanazt a célt szolgálják, mint az ICO fájlok. Számos online webhely és alkalmazás kínál ilyen fájlok létrehozását, és más képformátumokat, például [BMP](/hu/image/bmp/), [PNG](/hu/image/png/) stb. ikonfájlformátumba konvertál. Az ICO-fájlok hivatalos IANA által regisztrált internetes médiatípusa az image/vnd.microsoft.icon.

## Rövid története ##

Az ikonok a Microsoft Windows 1.0 elindításával jelentek meg. Ezek 32x32 méretűek és monokróm színűek voltak. A win32 megjelenésével bevezették a valódi színes ikonképek támogatását akár 256x256 pixel méretig. A Windows XP volt az első, amely támogatta a 32 bites színes ikonképeket, lehetővé téve félig átlátszó területek, például árnyékok, élsimítások és üvegszerű effektusok hozzáadását az ikonhoz. A Microsoft csak legfeljebb 48 × 48 képpontos ikonméretet javasolt a Windows XP rendszerhez. A Windows Vista 256 × 256 pixeles ikonnézetet adott a Windows Intézőhöz, valamint támogatja a tömörített [PNG](/hu/image/png/) formátumot. Nagyobb felbontást és nagy DPI módot használó felhasználóknak nagyobb ikonformátumok (például 256 × 256) használata javasolt.

## ICO fájlformátum ##

Egyetlen ICO-fájl egy vagy több, többféle méretű és színmélységű kis képből áll. A különböző méretű képek jelenléte a megfelelő méretezést szolgálja különböző képernyőfelbontásoknál. Az ICO/CUR fájlokban lévő összes érték [little-endian](https://en.wikipedia.org/wiki/Little-endian) bájtsorrendben van ábrázolva.

Az ICO fájl egy ikon fejlécből, egy ikonkönyvtárból,

|Mező|Leírás
---|---|
|Ikonfejléc|Általános információkat tárol az ICO-fájlról.
|Könyvtár[1..n]|Általános információkat tárol a fájlban lévő összes képről.
|Ikon #1|Az első kép tényleges "adatai" régi ÉS/XOR DIB vagy újabb PNG formátumban
|...|
|Ikon #n|Az utolsó ikonkép adatai

### Fejléc ###

|Eltolás|Méret (byte-ban)|Cél
---|---|---|
|0|2|Fenntartva. Mindig 0-nak kell lennie.
|2|2|Képtípust határoz meg: 1 az ikon (.ICO) képéhez, 2 a kurzor (.CUR) képéhez. Más értékek érvénytelenek.
|4|2|Meghatározza a fájlban lévő képek számát.

### Könyvtár ###

Az ICO-fájlban található könyvtár, amelyet ICONDIR-struktúraként ábrázol, egy ICONDIRECTORY-struktúrát tartalmaz a fájlban lévő minden egyes képhez. Ugyanezt egy összefüggő blokk követi az összes kép bitmap adatával. Ez az alábbiak szerint történik.

|Eltolás|Méret|Leírás
---|---|---|
|0 (0)|1|Szélesség, 0-nak kell lennie, ha 256 képpont
|1 (1)|1|Magasság, 0 legyen, ha 256 képpont
|2 (2)|1|A színek száma 0 legyen, ha több mint 256 szín
|3 (3)|1|Fenntartva, 0-nak kell lennie
|4 (4)|2|A színsíkok .ICO formátumban 0 vagy 1, vagy az X hotspot .CUR formátumban.
|6 (6)|2|Bit per pixel .ICO formátumban vagy Y hotspot .CUR formátumban
|8 (8)|4|A bittérképes adatok mérete bájtokban.
|12 (C)|4|Eltolás a fájlban.

## Referenciák ##

* [ICO – a Wikipedia által](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA – vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)


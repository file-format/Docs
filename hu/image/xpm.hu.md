{
  "date" : "2019-10-11",
  "keywords" :[ "xpm fájl", "xpm fájlformátum", "mi az xpm fájl", "fájl", "xpm példa", "xpm fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap fájlformátum",
  "description":"További információ az XPM fájlformátumról és az XPM-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az XPM fájl?

Az .xpm kiterjesztésű fájl egy képfájlformátum, amelyet az X Windows System használt. Támogatja az átlátszó képpontokat, és általában az ikonok képponttérképeinek létrehozását célozza meg. Támogatja a monokróm, gra-scale és színes pixmap adatokat. Ezeket úgy tervezték, hogy kézzel szerkeszthetők legyenek, és a [C](/hu/programing/c/) kódba beépíthetők. Ebből a célból az XPM fájlok egyszerű szöveges fájlformátumúak, és a C programozási nyelv szintaxisát követik. Az XPM fájlok számos képnézegető alkalmazással megnyithatók, mint pl
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView és Canvas X.

## XPM fájlformátum

Az XPM fájlformátum C szintaxist használ annak érdekében, hogy ezek integrálódjanak a C és C++ programokba. A következő hat különböző részből áll.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

A szakaszok valójában egy karakterláncok tömbje, az alábbiak szerint.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Az alábbiakban az egyes szakaszok részleteit közöljük.

`<Values> ` - Ez a szakasz egy karakterlánc, amely négy vagy hat egész számot tartalmaz, amelyek a 10-es bázisban vannak, és megfelelnek a következőnek:

* pixmap szélessége és magassága
* a színek száma
* a karakterek száma pixelenként
* opcionális hotspot koordináták és XPMEXT címke

`<Colors> ` - Ez a szakasz annyi karakterláncot tartalmaz, ahány színt. Mindegyik karakterlánc a következő:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Ez a szakasz a következőkből áll<height> húrok és<width> \*<chars_per_pixel> karakterek. Minden<chars_per_pixel> hosszúságú karakterláncnak a korábban meghatározott csoportok egyikének kell lennie<Colors> szakasz.

`<Extension> ` - A kiterjesztés szakaszt fel kell címkézni, ha nem üres, a<Values> szakasz. Többből állhat<Extension> alszakaszok, amelyek a következő két típusúak lehetnek:

* egy önálló karakterlánc a következőképpen áll össze: XPMEXT<extension-name><extension-data>
* vagy több karakterláncból álló blokk: XPMEXT<extension-name><related extension-data composed of several strings>

## Hivatkozások

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM kézikönyv](http://www.xfree86.org/current/xpm.pdf)


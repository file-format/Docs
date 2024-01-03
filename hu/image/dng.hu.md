{
  "date" : "2019-10-11",
  "keywords" :[ "dng fájl", "dng fájlformátum", "mi az a dng fájl", "fájl", "dng példa", "dng fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG – digitális fényképezőgép képfájl formátuma",
  "description":"További információ a DNG-fájlformátumról és az API-król, amelyekkel DNG-fájlokat hozhat létre és nyithat meg.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a DNG fájl?

A DNG egy digitális fényképezőgép képformátum, amelyet nyers fájlok tárolására használnak. Az Adobe fejlesztette ki 2004 szeptemberében. Alapvetően digitális fényképezésre fejlesztették ki. A DNG a [TIFF](/hu/image/tiff/)/EP szabvány formátum kiterjesztése, és jelentős mértékben használ metaadatokat. Annak érdekében, hogy a digitális fényképezőgépekből származó nyers adatokat a könnyű rugalmassággal és művészi vezérléssel kezeljék, a fotósok a nyers fényképezőgép-fájlokat választják. A JPEG és TIFF formátumok a fényképezőgép által feldolgozott képeket tárolják, ezért ezeken a formátumokon nincs sok változtatási lehetőség.

## A DNG fájlformátum története és verziói

A DNG specifikációnak eddig 5 változata jelent meg. Az 1.0.0.0 verzió 2004 szeptemberében jelent meg a "2.3" (ACR és DNG Converter) kiadásával együtt. 2005 februárjában megjelent az 1.1.0.0 verzió. 2008 májusában megjelent az 1.2.0.0 verzió, amelyet a "4.4"-ben használnak. Az 1.3.0.0-s verzió 2009 júniusában jelent meg. Az 1.4.0.0-s verzió 2012-ben jelent meg.

## DNG fájlformátum

Míg a nyers kamerafájlok feldolgozatlan vagy alacsony feldolgozottságú adatokat rögzítenek közvetlenül az érzékelőről. Mivel hasonlóak a filmnegatívokhoz, ezért a nyers kameraformátumokat „digitális negatívoknak” is nevezik. A nyers formátumok előnye a végfelhasználó fokozott művészi kontrollja. A felhasználó különféle paraméter-tartományokat állíthat be a követelményeknek megfelelően, mint például a fehéregyensúly, a tónusleképezés, a zajcsökkentés, az élesítés és így tovább. Másrészt a nyers kamerafájlt bármilyen felhasználáshoz bármilyen szoftveren vagy konverteren keresztül fel kell dolgozni.

Mivel a nyers kamerafájlokhoz nem állt rendelkezésre szabványos formátum, ez számos problémát okozott a végfelhasználó számára. Ezeket a problémákat az Adobe orvosolta, és nem védett formátumot definiált a nyers kamerafájlok számára. A formátum Digital Negative vagy DNG néven ismert. A DNG-t a hardverek és szoftverek széles köre használhatja nyers fájlok feldolgozására. Ezenkívül a DNG köztes formátumként is használható olyan képek tárolására, amelyeket eredetileg saját nyers formátumú fényképezőgéppel rögzítettek.

### DNG fájlformátum specifikációi

Ebben a részben a DNG formátumot a TIFF 6.0 kiterjesztéseként ismertetjük.

* **Fájlkiterjesztések**: A DNG „.DNG” vagy „.TIF” kiterjesztést használ.
* **SubIFD fák**: A DNG nem támogatja a SubIFD láncokat, helyette a DNG a TIFF-EP specifikációiban említett SubIFD fák használatát javasolja. A legjobb minőségben és felbontásban a NewSubFileType 0 értéket használhatja, míg a gyengébb minőségű bélyegképeknél a NewSubFileType értéke 1. Az is ajánlott, bár nem kötelező, hogy az első IFD-nek alacsony minőségű vagy felbontású miniatűr legyen.
* **Bájtsorrend**: A bájtsorrendet a DNG-olvasóknak támogatniuk kell egy adott kameramodell fájljainál is.
* **Maszkolt képpontok**: A legtöbb kameraérzékelő fekete kódolással számítja ki a teljesen maszkolt képpontokat az érzékelő szélén. Ezeket a képpontokat a kép DNG formátumban való tárolása előtt beillesztheti vagy levághatja. Ha a maszkolt képpontok nincsenek levágva, akkor ezen képpontok területét meg kell említeni az ActiveArea címkében. Az ezekből a pixelekből összegyűjtött információkat a fekete kódolási szintről vagy a nyers adatok tárolása előtt kell felhasználni, vagy bele lehet foglalni egy DNG-fájlba, amely meghatározza a fekete szín szintjét.
* **Hibás képpontok**: A nyers adatok DNG-ként való tárolása előtt a hibás képpontokat ki kell zárni.
* **Metaadatok**: A metaadatok a következő módok bármelyikén szerepelhetnek a DNG-ben:
** TIFF-EP vagy EXIF metaadat címkék használatával
** Az IPTC metaadat-címkén (33723) keresztül
** Az XMP metaadat-címke használata (700)
* **Tulajdonjogosult adatok**: Általában a szállítók saját átalakítóik által felhasználandó nyers fájlba foglalnak bele védett adatokat. A DNG a védett adataikat privát címkékben, privát IFD-kben és privát MakerNote-ban tárolja. A szállítóknak a DNGPrivateData és a MakerNoteSafety címkéket kell használniuk annak biztosítására, hogy a DNG-fájlokat szerkesztő alkalmazások megőrizzék ezeket a védett adatokat.

Az alábbiakban felsorolunk néhány fontos korlátozást és kiterjesztést a TIFF-címkékre.

**BitsPerSample**

8-32 bit/minta támogatott. Ha a SamplesPerPixel nem egyenlő 1-gyel, akkor minden mintánál azonos mélységnek kell lennie. De ha a BitsPerSample nem egyenlő 8-mal, 16-tal vagy 32-vel, akkor a biteket bájtokba kell csomagolni az 1-es TIFF alapértelmezett FillOrder 1-es (big-endian) használatával.

**kompresszió**

Két tömörítési címkeérték támogatott:

* 1. érték: Tömörítetlen adatok.
* 7. érték: JPEG tömörített adatok, vagy alapvonal DCT JPEG, vagy veszteségmentes JPEG tömörítés.

**Fotometrikus értelmezés**

A következő értékek csak miniatűr és előnézeti IFD-k esetén támogatottak:

* 1 = BlackIsZero. Feltételezhető, hogy gamma 2.2 színtérben van.
* 2 = RGB. Feltételezhető, hogy az sRGB színtérben van.
* 6 = YCbCr. JPEG kódolású előnézeti képekhez használatos.

A következő értékek támogatottak a nyers IFD-nél, és ezek a kamera natív színterének számítanak:

* 32803 # CFA (Color Filter Array).
* 34892 # LinearRaw.

**Orientáció**

Az orientációs címkét a fájlböngészők használják, hogy azok veszteségmentesen forgathassák a DNG-fájlokat. A DNG olvasóknak támogatniuk kell az összes lehetséges tájolást, beleértve a tükrözött tájolást is.

## Jellemzők a DNG legújabb verziójában

A DNG 2012. október 1.4-es verziója a következő speciális funkciókkal rendelkezik.

* Alapértelmezett felhasználói vágás
* Átláthatóság
* Lebegőpontos (HDR)
* Veszteséges tömörítés
* Proxyk

## Referenciák ##

* [DNG-specifikációk – Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0.0.pdf)
* [Digitális negatív – Wikipédia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG – A digitális fényképezőgépek nyers adatainak nyilvános archív formátuma](https://helpx.adobe.com/photoshop/digital-negative.html)


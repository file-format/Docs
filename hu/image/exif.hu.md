{
  "date" : "2019-10-11",
  "keywords" :[ "exif fájl", "exif fájl formátum", "mi az exif fájl", "fájl", "exif példa", "exif fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"További információ az EXIF fájlformátumról és az API-król, amelyek EXIF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az EXIF fájl?
Az EXIF az „Exchangeable Image File Format” rövidítése, a meghatározást először a [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) adta meg 1985-ben. A szabványt a Japan Electronics és Az Informatikai Iparágak Szövetsége (JEITA) mától. Az EXIF a főként digitális fényképezőgépek és szkennerek által használt kép- és hangformátumok specifikációinak szabványa.

Az EXIF szabvány tartalmazza a címkézési és metaadat-információkat a képfájllal együtt. A metaadatok olyan információkat tartalmazhatnak, mint a fényképezőgép modellje, zársebesség, dátum és idő, rekeszérték, gyártó, expozíciós idő, X felbontás, Y felbontás stb. Az EXIF adatok alapértelmezés szerint el vannak rejtve. Az EXIF adatok megtekintéséhez ki kell választani a nézet tulajdonságait a képnézegető alkalmazáson belül. Az Exif-metaadatok miniatűröket, valamint technikai és elsődleges képadatokat is tartalmazhatnak egyetlen képfájlban.

## Előzmények és verziók ##

* 1995 októberében a JEIDA létrehozta az 1-es verziót. Ebben a verzióban a JEIDA meghatározta a struktúrát, amely képadatformátumból és attribútum-információkból, valamint alapvető címkékből áll.
* 1997 novemberében az 1.1-es verziót az 1. verzió legtöbb címkéjével vezették be, de kiegészítették az opcionális attribútum-információkkal és a formátumműveletekkel kapcsolatos rendelkezéseket is.
* 1998. június, 2-es verzió sRGB színtérrel, tömörített miniatűrökkel és hangfájlokkal.
* 1998. december, 2.1-es verzió továbbfejlesztett tárolási és attribútuminformációkkal.
* 2002. február, 2.2-es verzió, továbbfejlesztett 2.1-es verzió, nyomtatási kikészítés hozzáadásával.
* 2003. szeptember, 2.21-es verzió opcionális színtérrel, Adobe RGB néven.

## EXIF fájl formátum

Az EXIF a következő fájlformátumokat használja speciális metaadatok hozzáadásával.

1. [JPEG](/hu/image/jpeg/) - diszkrét koszinusz transzformáció (DCT) tömörített képfájlokhoz.
1. [TIFF](/hu/image/tiff/) Rev. 6.0 (RGB vagy YCbCr) tömörítetlen képfájlokhoz.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) audiofájlokhoz (lineáris [PCM](https:/) /en.wikipedia.org/wiki/Pulse-code_modulation) vagy ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM a tömörítetlen hangadatokhoz, és [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) a tömörített hangadatokhoz).

### Az EXIF által használt jelölő ###

A 0xFFE0~~0xFFEF jelölő a felhasználói alkalmazások által használt "Application Marker". A régebbi digi kamerák például JFIF-et (JPEG File Interchange Format) használnak a képek tárolására. A JFIF az APP0 (0xFFE0) jelölőt használja a digi kamera konfigurációs adatainak és miniatűrökének beillesztéséhez. Ezenkívül az EXIF alkalmazásjelölőt is használ az adatok beszúrására, de az EXIF az APP1 (0xFFE1) jelölőt használja, hogy elkerülje a JFIF formátummal való ütközést. Minden EXIF fájlformátum ebből a formátumból indul ki.


|SOI Marker|APP1 Marker|APP1 Data|Other Marker
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

A SOI (0xFFD8) Markerből indul ki, tehát egy JPEG fájl. Ezután azonnal következik az APP1 Marker. Az EXIF összes adata ezen az APP1 adatterületen tárolódik. Az "SSSS" része a felső táblázatban az APP1 adatterület (EXIF adatterület) méretét jelenti. Kérjük, vegye figyelembe, hogy az "SSSS" méret magában foglalja a leíró méretét is. Az „SSSS” után elindulnak az APP1 adatok. Az első rész egy speciális adat annak azonosítására, hogy EXIF vagy nem, ASCII karakter "EXIF" és 2 bájt 0x00. Az APP1 Marker terület után a többi JPEG jelölő következik.

### Exif adatstruktúra ###

Az EXIF adatok (APP1) durva szerkezete az alábbiak szerint látható. Ahogy fentebb tárgyaltuk, az EXIF-adatok az "EXIF" ASCII-karakterből és 2 bájt 0x00-ból indulnak ki, majd az EXIF-adatok következnek. Az EXIF TIFF formátumot használ az adatok tárolására.


|FFE1|APP1 Marker
---|---|
|SSSS|APP1 adat|APP1 adatméret
|45786966 0000|Exif fejléc
|49492A00 08000000|TIFF fejléc
|XXXX. . . .|IFD0 (főkép)|Könyvtár
|LLLLLLLL|Link az IFD1-hez
|XXXX. . . .|Az IFD0 adatterülete
|XXXX. . . .|Exif SubIFD|Könyvtár
|00000000|Link vége
|XXXX. . . .|Az Exif SubIFD adatterülete
|XXXX. . . .|IFD1(thumbnail image)|Könyvtár
|00000000|Link vége
|XXXX. . . .|Az IFD1 adatterülete
|FFD8XXXX. . . XXXXFFD9|Indexkép

#### TIFF fejléc ####

A 8 bájtos [TIFF](/hu/image/tiff/) fájlfejléc a következő információkat tartalmazza:

`Bájtok 0-1:` A fájlon belül használt bájtsorrend. A törvényes értékek: „II”(4949.H)„MM” (4D4D.H).

A „II” formátumban a bájtok sorrendje mindig a legkisebb jelentőségű bájttól a legjelentősebb bájtig terjed mind a 16 bites, mind a 32 bites egész számok esetében. Ezt nevezzük little-endian byte ordernek. Az „MM” formátumban a bájtok sorrendje mindig a legjelentősebbtől a legkevésbé jelentősig terjed, mind a 16 bites, mind a 32 bites egész számok esetében. Ezt nevezik big-endian byte ordernek.

`2-3 bájt:` Tetszőleges, de gondosan megválasztott szám (42), amely tovább azonosítja a fájlt TIFF-fájlként. A bájtok sorrendje a 0-1 bájtok értékétől függ.

`4-7 bájt:` Az első IFD eltolása (byte-ban). A könyvtár a fejléc után bárhol lehet a fájlban, de szóhatáron kell kezdődnie. Az Image File Directory különösen követheti az általa leírt képadatokat. Az olvasóknak követniük kell a mutatókat, bárhová is vezetnek. A bájteltolás kifejezést ebben a dokumentumban mindig a TIFF-fájl elejéhez viszonyított helyre utaljuk. A fájl első bájtjának eltolása 0.

#### Képfájl könyvtár ####

Az IFD információkat tartalmaz a képről, valamint a tényleges képadatokra mutató mutatókat. Ez a címtárbejegyzések számának (azaz a mezők számának) 2 bájtos számlálójából áll, amelyet 12 bájtos mezőbejegyzések sorozata követ. , amelyet a következő IFD 4 bájtos eltolása követ (vagy 0, ha nincs). Egy TIFF-fájlban legalább 1 IFD-nek kell lennie, és minden IFD-nek tartalmaznia kell legalább egy bejegyzést.

##### IFD bejegyzés #####

Minden 12 bájtos IFD bejegyzés a következő formátumú.


|Bájtok|Leírás
---|---|
|0-1|A mezőt azonosító címke
|2-3|A mező típusa
|4-7|A jelzett típus száma
|8-11|Az Értékeltolás, a mező értékének fájleltolása (byte-ban). Az érték várhatóan szóhatáron kezdődik; a megfelelő Értékeltolás így páros szám lesz. Ez a fájleltolás bárhová mutathat a fájlban, még a képadatok után is

A TIFF mező egy logikai entitás, amely TIFF címkéből és annak értékéből áll. Ez a logikai koncepció IFD bejegyzésként valósul meg, plusz a tényleges érték, ha nem fér bele az érték/eltolás részbe, az IFD bejegyzés utolsó 4 bájtja. A TIFF mező és az IFD bejegyzés kifejezések a legtöbb kontextusban felcserélhetők.

#### Miniatűr ####

Az Exif formátum a kép miniatűrjét tartalmazza (a Ricoh RDC-300Z kivételével). Általában az IFD1 mellett található. A bélyegképeknek 3 formátuma van; JPEG formátum (a JPEG YCbCr-t használ), RGB TIFF formátum, YCbCr TIFF formátum.

##### JPEG formátumú bélyegkép #####

Ha a Compression(0x0103) Tag értéke az IFD1-ben '6', akkor az indexkép formátuma JPEG. A legtöbb Exif-kép JPEG formátumot használ miniatűrként. Ebben az esetben a bélyegkép eltolását a JpegIFOffset(0x0201) címkével IFD1-ben, a bélyegkép méretét pedig a JpegIFByteCount(0x0202) címkével kaphatja meg. Az adatformátum közönséges JPEG formátum, 0xFFD8-tól kezdődik és 0xFFD9-ig ér véget. Úgy tűnik, hogy a JPEG formátum és a 160x120 pixeles méret az Exif2.1 vagy újabb miniatűr formátuma javasolt.

##### TIFF formátumú bélyegkép #####

Ha a Compression(0x0103) címke értéke az IFD1-ben '1', akkor a miniatűr képformátum nem tömörítés (TIFF-kép). A miniatűr adatok kezdőpontja a StripOffset(0x0111) címke, a bélyegkép mérete a StripByteCounts(0x0117) címke összege.

## Referenciák ##

* [EXIF – a Wikipédia által](https://en.wikipedia.org/wiki/Exif)
* [EXIF-fájlformátum](https://www.media.mit.edu/pia/Research/deepview/exif.html)


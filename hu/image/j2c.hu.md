{
  "date" : "2019-10-11",
  "keywords" :[ "j2c fájl", "j2c fájlformátum", "mi az a j2c fájl", "fájl", "j2c példa", "j2c fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"További információ a J2C fájlformátumról és az API-król, amelyek J2C fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Mi az a J2C fájl?

A .j2c kiterjesztésű fájl a JPEG fájlformátum egyik változata, és a wavelet-tömörítéssel van tömörítve. A jelölők és szegmensek rendszere közel azonos a JPEG 2000 fájlformátummal. A J2C fájlformátum a JPEG 2000 állvány 1. részében meghatározott, amely támogatja a veszteséges és veszteségmentes tömörítést is. A JPEG 2000 kódfolyamot [JP2](/hu/image/jp2/) vagy más fájlformátumba való beágyazásra tervezték, bár előfordulhat, hogy önmagában is megjelenik egy fájlban. A J2C fájl megnyitható az Adobe Photoshop 2020, az Adobe Illustrator 2020 és a Corel Paintshop Pro segítségével.

## J2C fájlformátum

A J2C fájlformátum megegyezik a JPEG 2000 fájlformátumával, amelyet gyakran .jp2 és .jpc formátumban mentenek el. Emiatt a J2C fájlok ugyanazt a megközelítést követik a metaadatok XML formátumban történő kódolásakor, ahol az 12234-1 szabványt referenciaként használják az Exif címkék és az XML összetevők között. Tovább javítja a JPEG 2000 part-2 kiterjesztéssel, amely egyetlen képben egyesíti az animációs mechanizmust és a kódfolyam konfigurációkat. Az ilyen kiterjesztett fájlformátumú fájlok [.jpx](/hu/image/jpx/) néven kerülnek mentésre.

### JPEG2000 fájl elrendezése

A JPEG2000 számos alkalmazást támogat a bővíthető fájlformátumoknak való megfelelés alapján. Bár a legegyszerűbb típus tartalmazhat egyetlen képet, a bonyolultabb típusok egymásra halmozott vagy időalapú sorrendbe rendezett képeket tartalmazhatnak.

#### JP2 doboz
Ez a JP2 fájlformátum legfelső szintű építőeleme, amely típus- és hosszúságú mezőket tartalmaz a fejlécben, valamint egy adatszekciót. A dobozok legfigyelemreméltóbb típusa az összefüggő kódfolyam doboz. Ez a doboz adatrészében a JPEG2000 kódfolyamot tárolja.

#### JPEG2000 CodeStream

A JPEG2000 CodeStream egy bájtok sorozata, amely a JPEG2000 tömörített kép dekódolásához szükséges. Abban az esetben, ha a fájlban nincs más, mint ez a kódfolyam, akkor ezt nyers kódfolyamfájlnak nevezzük. Általában a JPEG kódfolyam a JPEG2000 tömörítési algoritmus alkalmazása egy képen, bár nem ez az egyetlen módja.

#### Csempealkatrészek ####

A JPEG2000 kódolású kép csomagoknak nevezett adategységek gyűjteménye. Ezeket a csomagokat a kódfolyamban tartják fenn a csempe-részeknek nevezett csomagcsoportokon belül. A kép kódolása előtt a kódoló a képet egy téglalap alakú blokkokból álló rácsra osztja, amelyeket csempéknek neveznek, ahol minden csempét külön kódolnak, a többi csempétől függetlenül.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 fájlformátum" >}}

## J2C tömörítés
A JPEG 2000 wavelet-tömörítési technológiát használ, ami gyorsítja azt a tényt, hogy viszonylag kevés pixel jelenik meg bármely nézetablakban vagy ablakban, amelyet a néző megjelenít. Ezt nyomatékosíthatja, hogy nagyon nagy méretű (gigabájtban) képek esetén csak néhány megabájt pixel jelenik meg a képernyőn. Ez segít gyorsan lekérni és megjeleníteni a képadatoknak csak azt a részét, amely a képernyő képpontjainak feltöltéséhez szükséges. Ehhez nagysebességű dekompressziós technológiára is szükség van, hogy felgyorsítsa a képlekérési mechanizmust a menet közben szükséges képek létrehozásához.

A J2C kihasználja a gyors kibontás előnyeit, és csak a pixeladatokhoz szükséges információkat kéri le, hogy a látható képek egy részét gyorsan megjelenítse a képernyőn. A J2C elsősorban adatok megtekintésére és nem szerkesztésére készült.

## J2C azonosítás
A JPEG 2000 fájlok "FF 4F FF 51" aláírási bájtokkal rendelkeznek.

### Mime típusok
A JPEG 2000 fájlokhoz regisztrált Mime típusok a következők:
* image/j2c
* kép/jpx
* kép/jpm
* videó/mj2

## Fejlesztések a JPEG szabványhoz képest
A JPEG-szabványhoz képest a következők:
* Kiváló tömörítési teljesítmény
* Több felbontású ábrázolás
* Progresszív átvitel pixelenként és felbontásonként
* Veszteségmentes vagy veszteséges tömörítés kiválasztása
* Hibatűrő képesség, rugalmas fájlformátum
* Nagy dinamikatartomány támogatása
* Oldalsó csatorna térinformációi

## Referenciák ##
* [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)


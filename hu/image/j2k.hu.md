{
  "date" : "2019-10-11",
  "keywords" :[ "j2k fájl", "j2k fájlformátum", "mi az a j2k fájl", "fájl", "j2k példa", "j2k fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"További információ a J2K fájlformátumról és az API-król, amelyek J2K fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## Mi az a J2K fájl?

A **J2K** fájl egy olyan kép, amelyet a DCT-tömörítés helyett a wavelet-tömörítéssel tömörítenek. Ezt a fájlformátumot a Joint Photography Experts Group (JPEG) 2000 fájlok használják. A J2K fájlok XML formátumban tárolják a képfájl metaadatait, ellentétben a .jpeg vagy .jpg fájlokkal, amelyek erre a célra az EXIF formátumot használják. A J2K fájlok támogatják a 15 bites színt, az alfa-átlátszóságot és a veszteségmentes tömörítést. Számos kereskedelmi API létezik a JPEG 2000 képek dekódolására, például a J2K-Codec. A J2K fájl Windows operációs rendszeren a szabványos képnézegetőkkel nyitható meg.

## J2K fájlformátum ##

A J2K fájlformátum megegyezik a JPEG 2000 fájlformátumával, amelyet gyakran .jp2 és .jpc formátumban mentenek el. Emiatt a J2K fájlok ugyanazt a megközelítést követik a metaadatok XML formátumban történő kódolásakor, ahol az 12234-1 szabványt használják referenciaként az Exif címkék és az XML összetevők között. Tovább javítja a JPEG 2000 part-2 kiterjesztéssel, amely egyetlen képben egyesíti az animációs mechanizmust és a kódfolyam konfigurációkat. Az ilyen kiterjesztett fájlformátumú fájlok .jpx formátumban kerülnek mentésre.

### JPEG2000 fájl elrendezése ###

A JPEG2000 számos alkalmazást támogat a bővíthető fájlformátumoknak való megfelelés alapján. Bár a legegyszerűbb típus tartalmazhat egyetlen képet, a bonyolultabb típusok egymásra halmozott vagy időalapú sorrendbe rendezett képeket tartalmazhatnak.

#### JP2 Box ####
Ez a JP2 fájlformátum legfelső szintű építőeleme, amely típus- és hosszúságú mezőket tartalmaz a fejlécben, valamint egy adatszekciót. A dobozok legfigyelemreméltóbb típusa az összefüggő kódfolyam doboz. Ez a doboz az adatrészében a JPEG2000 kódfolyamot tárolja.

#### JPEG2000 CodeStream ####

A JPEG2000 CodeStream egy bájtok sorozata, amely a JPEG2000 tömörített kép dekódolásához szükséges. Abban az esetben, ha a fájlban nincs más, mint ez a kódfolyam, akkor ezt nyers kódfolyamfájlnak nevezzük. Általában a JPEG kódfolyam a JPEG2000 tömörítési algoritmus alkalmazása egy képen, bár nem ez az egyetlen módja.

#### Csempe alkatrészek ####

A JPEG2000 kódolású kép csomagoknak nevezett adategységek gyűjteménye. Ezeket a csomagokat a kódfolyamban tartják fenn a csempe-részeknek nevezett csomagcsoportokon belül. A kép kódolása előtt a kódoló a képet egy téglalap alakú blokkokból álló rácsra osztja, amelyeket csempéknek neveznek, ahol minden csempét külön kódolnak, a többi csempétől függetlenül.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 fájlformátum" >}}

## J2K tömörítés ##
A JPEG 2000 wavelet-tömörítési technológiát használ, ami gyorsítja azt a tényt, hogy viszonylag kevés pixel jelenik meg bármely nézetablakban vagy ablakban, amelyet a néző megjelenít. Ezt nyomatékosíthatja, hogy nagyon nagy méretű (gigabájtban) képek esetén csak néhány megabájt pixel jelenik meg a képernyőn. Ez segít gyorsan lekérni és megjeleníteni a képadatoknak csak azt a részét, amely a képernyő képpontjainak feltöltéséhez szükséges. Ehhez nagysebességű dekompressziós technológiára is szükség van, hogy felgyorsítsa a képlekérési mechanizmust a menet közben szükséges képek létrehozásához.

A J2K kihasználja a gyors kibontás előnyeit, és csak a pixeladatokhoz szükséges információkat kéri le, hogy a látható képek egy részét gyorsan megjelenítse a képernyőn. A J2K elsősorban adatok megtekintésére és nem szerkesztésére készült.

## J2K azonosító ##
A JPEG 2000 fájlok 6A 50 20 20 aláírási bájtokkal rendelkeznek.

### Mime típusok ###
A JPEG 2000 fájlokhoz regisztrált Mime típusok a következők:
* kép/jp2
* kép/jpx
* kép/jpm
* videó/mj2

## Fejlesztések a JPEG szabványhoz képest ##
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


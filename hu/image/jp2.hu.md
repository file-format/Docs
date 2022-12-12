{
  "date" : "2019-10-11",
  "keywords" :[ "jp2 fájl", "jp2 fájlformátum", "mi az a jp2 fájl", "fájl", "jp2 példa", "jp2 fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Képfájl formátum",
  "description":"További információ a JP2 fájlformátumról és az API-król, amelyek JP2 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Mi az a JP2 fájl? ##

A JPEG 2000 (**JP2**) egy képkódoló rendszer és a legmodernebb képtömörítési szabvány. Wavelet technológiát használ a veszteségmentes tartalom bármilyen minőségben történő kódolására. Ezen túlmenően, a kódolás hatékonyságát érintő jelentős szankciók nélkül, a JPEG 2000 képes ugyanazt a tartalmat hatékonyan elérni és számos más felbontásra és minőségre dekódolni. A JPEG 2000 kódfolyamai jelentősen skálázhatók, mivel olyan érdekes régiókkal rendelkeznek, amelyek lehetővé teszik a térbeli véletlenszerű hozzáférést.

A JPEG 2000 az egyik legjobban méretezhető szabvány. A kép különböző részei különböző minőségek használatával tárolhatók. Figyelemre méltó teljesítménynövekedés érhető el a kódfolyam különféle módokon történő megrendelésével. Mindazonáltal a JP2 bonyolult és számításigényes kódolókat/dekódolókat igényel, e rugalmasság eredményeként. A JPEG-hez képest a JPEG 2000 csak olyan csengetési műtermékeket hoz létre, amelyek a kép széléhez közeli gyűrűket eredményeznek, és elmosódnak, míg a JPEG 8 × 8-as vizuális műtermékblokkokat használ, amelyek egyaránt lehetnek csengő és blokkoló műtermékek. Akár 16384 különböző komponenssel rendelkezik, terapixelben kifejezett méretekkel, és akár 38 bit/minta pontossággal.

## Előzmények ##

2000-ben a Joint Photographic Experts Group bizottság megtervezte a JP2-t azzal a céllal, hogy ezzel az új, wavelet alapú módszerrel javítsák saját diszkrét koszinusz transzformáció alapú JPEG szabványukat. A JPEG bizottság célja az volt, hogy alapmódszereiket licenszdíjmentesen biztosítsák. A JP2 licencben 20 cég közötti versenyben ők nyertek. A JPEG 2000-et ISO szabványnak nyilvánították, bár a legtöbb webböngésző 2017 óta nem áll készen a JPEG 2000-re.

## A JPEG 2000 képkódoló rendszer részei ##

Az alábbiakban a JPEG 2000 szabványok teljes készletét alkotó főbb részek találhatók.


|Rész|Cím|Leírás|Szám
---|---|---|---|
|1. rész|Alapkódrendszer| Meghatározza a kódfolyam szintaxisát. A JPEG 2000 képek dekódolásának különböző szakaszai. Elmagyarázza az alapvető JP2 fájlformátumot, a metaadatokat és a megadandó IP-jogokat.|ISO/IEC 15444-1
|2. rész|Bővítmények|Kiterjesztéseket határoz meg a fájlformátumú kódfolyamhoz, és lehetővé teszi a HDR-minta bemutatóit, a színtér specifikációját, a kivágást, a geometriai átalakításokat; változatos animációk, metaadatok és többszörös kódfolyam.|ISO/IEC 15444-2
|3. rész|Motion JPEG 2000 (MJ2 vagy MJP2)|Fájlformátum bevezetése a mozgássorozatokhoz, a képeket független kódfolyamba kódolva.|ISO/IEC 15444-3
|4. rész|Megfelelőség|Kódolási és dekódolási tesztelési technikákat állapít meg, és ellenőrzi a fájlokat a csupasz kódú adatfolyamokhoz és a JP2-fájlokhoz egyaránt.|ISO/IEC 15444-4
|5. rész|Referenciaszoftver|Két forráskódcsomagból (Java, C) áll, amelyek Core kódolási rendszert valósítanak meg, és nyílt forráskódú licencek alatt állnak rendelkezésre.|ISO/IEC 15444-5
|6. rész|Összetett képfájl formátum|Meghatározza a JPM fájlformátumot, és lehetővé teszi a többoldalas dokumentumok képalkotását faxszerű alkalmazásokhoz. Támogatja a JBIG2 és JPEG használatát.|ISO/IEC 15444-6
|8. rész|JPEG 2000 Biztonságos (JPSEC)|Gondoskodik a tranzakciók, a tartalom és a technológiák biztonságáról, és biztonságos JPEG 2000 bitfolyamokat tesz lehetővé.|ISO/IEC 15444-8
|9. rész|JPIP|Eszközöket határoz meg hálózati környezetben a metaadatokhoz és képekhez való hozzáféréshez, és interaktív és hatékony protokollokat ír elő|ISO/IEC 15444-9
|10. rész|JP3D|Az 1. rész térfogati kiterjesztése és a Z dimenzió bevezetése. Kibővíti a csempék, kódblokkok, körzetek és a 3D érdeklődési körökhöz kapcsolódó kisegítő lehetőségek fogalmát.|ISO/IEC 15444-10
|Part 11|JPWL|Jól szervezett átvitellel foglalkozik egy hibás vezeték nélküli hálózaton keresztül. Ez a bővítmény kompatibilis a dekóderekkel |ISO/IEC 15444-11
|13. rész|Belépő szintű kódoló|A Core kódrendszer belépő szintű kódoló megvalósítását határozza meg.|ISO/IEC 15444-13
|14. rész|JPXML|A reprezentáció XML-ben, és elmagyarázza a markerszegmenseket és a képek belső adataihoz való hozzáférési módszereket.|ISO/IEC 15444-14
|Part 15|HTJ2K (Feldolgozatlan)|Meghatároz egy alternatív blokkkódoló algoritmust. Az algoritmus tízszeresére növeli az áteresztőképességet és veszteségmentes kódolást/dekódolást.|

## JP2 fájlformátum ##

A JPEG 2000 ugyanúgy határozza meg a fájlformátumot, mint a kódfolyamot, mint a JPEG-1. Bár a képmintákat kizárólag a JPEG 2000 írja le, a JPEG-1 azonban további információkat is tartalmaz a kép kódolásához elengedhetetlen színtérről és felbontásról. Ha egy kép JPEG 2000 fájlként van tárolva, a **.jp2** kiterjesztést használja a rendszer. Ezt a fájlformátumot tovább javítja a JPEG 2000 part-2 kiterjesztése, amely animációs mechanizmusokat és számos kódfolyam konfigurálását határozza meg egyetlen képben. A **.jpx** kiterjesztést használja, ha a képeket ezzel a kiterjesztett fájlformátummal menti. Mivel a kódfolyam-adatokat nem tekintjük elsősorban fájlba mentettnek, ezért erre a célra nincs szabványos kiterjesztése. Bár tesztelési célból, gyakran a **.jpc** vagy **.j2k** kiterjesztést kapja. A JPEG-1-gyel ellentétben a JPEG 2000 más módszert választ a metaadatok XML formátumban történő kódolására. Az 12234-1.4 szabvány (az ISO TC42 bizottság által) referenciaként szolgál az Exif-címkék és az XML-komponensek között. A JPEG 2000 tartalmazhat egy ISO szabványt, az XMP-t.

### Darabok ###
A JPEG 2000 fájlok egymást követő darabokból állnak. Minden csonk 8 bájtos fejléccel rendelkezik: 4 bájtos csonkméret (big-endian, magas bájt először) és 4 bájtos csonktípus – az előre meghatározott aláírások egyike: „jP” vagy „jP2”.

A második csonknak "ftyp" típusúnak kell lennie, és 8-as eltolásnál van egy altípusa. A JPEG 2000 altípusa határozza meg, amelynek a következő értékek valamelyikének kell lennie: "jp2 "(fájltípus \*.JP2), "jp20" (fájl típus \*.JPA), "jpm " (fájltípus \*.JPM), "jpx " (fájl típusa \*.JPX).

Iterálva a darabokat, amíg ismeretlen típust nem észlelünk, JPEG 2000 kép/videó fájlt készítünk.

### Színátalakítás ###

Kezdetben a képek RGB színtérből másik színtérbe történő átalakítása szükséges. Erre a célra két módszer létezik: irreverzibilis színtranszformáció (ICT) és megfordítható színtranszformáció (RCT). Az előbbi YC,,B,,C,,R,, színteret használ, és fix/lebegőpontos, később pedig módosított YUV színtér, és természetében megfordítható.// //Nem korlátozódik az RGB modellre, JPEG A 2000 nyelv többkomponensű átalakítást használ.

### Csempézés ###

Amikor a színátalakítás megtörtént, a kép téglalap alakú régiókká, úgynevezett csempékké alakul, amelyek külön átalakíthatók és kódolhatók. Az összes lapka mérete azonos lesz, vagy az egész kép egyetlen lapkának tekinthető. A Dekóder kihasználja a csempézés előnyeit, és kevesebb memóriát fogyaszt, vagy részben kódolhat néhány csempét. Bár ennek a technikának a hátránya a képminőség romlása.

### Wavelet transzformáció ###

A csempézés után a kép wavelet transzformációra kerül, amely lehet irreverzibilis vagy reverzibilis, és a konvolúciós vagy emelési séma segítségével valósítható meg.

### Tömörítési arány ###

A kép fizikai jellemzőitől függően 20%-os tömörítési nyereség érhető el. A JPEG 2000 térbeli redundancia-előrejelzése létfontosságú szerepet játszik a tömörítési folyamatban, és általában a nagy felbontású képek nyerik a legtöbb előnyt.

## A szabvány által kiszolgált alkalmazások ##

* Képkocka alapú HD videók rögzítése, szerkesztése és tárolása
* Orvosi képek és biometrikus adatok
* Műholdképek, távérzékelés és mozgásérzékelés
* Kliens/szerver kommunikáció, hálózati elosztás és tárolás.
* Digitális mozi, élő HDTV közvetítés, digitalizált audio-vizuális cucc

## Hivatkozások ##

* [A JPEG 2000 áttekintése](https://jpeg.org/jpeg2000)
* [JPEG 2000 képkódoló rendszer](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)


{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "file", "extension", "format", "Audio Coding", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az AAC fájlformátumról és az API-król, amelyek AAC fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"AAC - Advanced Audio Coding File",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## Mi az AAC fájl?

Az AAC (Advanced Audio Coding) olyan digitális hangkódolási szabványra utal, amely veszteséges hangtömörítésen alapuló hangfájlokat képvisel. A **[MP3](/hu/audio/mp3/)** fájlformátum utódjaként indították el, tekintettel arra, hogy az oldalsó problémákkal szembesültek az új ötletek megvalósítása az adattömörítési módszerek fejlesztésén alapuló kódolási folyamatban. Az AAC jobb hangminőséget ér el, mint az MP3 azonos bitsebességgel. Az MPEG-2 7. részében (ISO/IEC 13818-7), frissített formában pedig az MPEG-4 3. részében (ISO/IEC 14496-3) határozták meg.

Az AAC formátumot alapértelmezett médiaformátumként fogadta el a YouTube, iPhone, iPod, iPad, Apple iTunes és számos más platform. Számos alkalmazás és API áll rendelkezésre az AAC fájlformátumok más formátumokká konvertálásához, például MP3, WMA, M4A, **[WAV](/hu/audio/wav/)** és mások.

### Az AAC fájl rövid története

Az AAC fájlformátum az MP3 továbbfejlesztett változata néhány fejlesztéssel. Több vállalat közreműködésével, köztük a Fraunhofer Institute (Fraunhofer IIS – MP3 fejlesztők), a Nokia, a Dolby, az AT&T és a Sony, a formátumot a Moving Picture Experts Group (MPEG) nemzetközi szabvánnyá nyilvánította 1997 áprilisában. Később, 1999-ben, az MPEG-2 Part 7 frissítésre került, és bekerült az MPEG-4 szabványcsaládba. MPEG-4 Part 3 néven volt ismert, ISO/IEC 14496-3: 1999 vagy MPEG-4 Audio néven.

## Az AAC fájlformátum specifikációi

Az AAC fájlformátum specifikációi nagyobb rugalmasságot tesznek lehetővé a kodek tervezésében, mint az MP3 esetében, ami több párhuzamos kódolási stratégiát és hatékonyabb tömörítést eredményez. A formátumot számos hardverplatform választotta az MP3-hoz képest történő fejlesztése érdekében, ami több lehetőséget biztosít még kisebb bitsebességgel is. Az AAC fájlformátum specifikációi [MPEG-2 Part 7](https://www.iso.org/standard/43345.html) és [MPEG-4 Part 3](https://www.iso.org) /standard/53943.html) (nem ingyenesen letölthető). A formátum a következő médiatípusokat használja:

* audio/aac
* audio/aacp
* audio/3gpp
* audio/3gpp2
* audio/mp4
* audio/mp4a-latm
* audio/mpeg4-generic

## AAC vs MP3 – Fejlesztések ##

Az AAC és az MP3 közötti fő különbségek a fejlesztések tekintetében a következők:

* Az AAC a csatornák szélesebb körét (48-ig) és mintavételezési frekvenciákat (8 kHz-től 96 kHz-ig) támogatja
* Az AAC jobb kódolási frekvenciákkal rendelkezik 16 kHz felett
* Az AAC szélesebb korlátokkal rendelkezik a szűrőkészlet frekvencia-idő felbontásában, ami a tranziensek és az audiojel stacioner részeinek jobb kódolását eredményezte.
* Hatékonyabb és egyszerűbb szűrőbank: a hibrid szűrőbankot a szabványos MDCT (módosított diszkrét koszinusz transzformáció) váltotta fel.
* Támogatja a tömörítés fokozott hatékonyságát a Temporal Noise Shaping (TNS), az MDCT-idő előrejelzési együtthatói (hosszú távú előrejelzés), a parametrikus sztereó, az észlelési zajhelyettesítés, a spektrális sáv replikáció (SBR) használatával.
* rugalmasabb közös sztereó (különböző frekvenciatartományokban különböző módszerek használhatók);

## Referenciák ##

* [AAC – a Wikipedia által](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)


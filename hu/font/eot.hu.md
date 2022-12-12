{
  "date" : "2020-08-20",
  "keywords" :[ "eot fájl", "eot fájlformátum", "mi az eot fájl", "fájl", "eot példa", "eot fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - TrueType Font File Format",
  "description":"További információ az EOT fájlformátumról és az API-król az EOT-fájlok létrehozásához és megnyitásához.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Mi az EOT fájl?

Az .eot kiterjesztésű fájl egy dokumentumba ágyazott OpenType betűtípus. Ezeket többnyire webfájlokban, például weboldalakban használják. A Microsoft készítette, és a Microsoft Products támogatja, beleértve a PowerPoint prezentáció [.pps](/hu/presentation/pps) fájlt is. A fájl nem elsődleges használat, és egyfajta kísérő dokumentum a fő dokumentummal vagy weboldallal. Az OTF betűtípusokhoz hasonlóan az EOT is támogatja a Postscript és a TrueType körvonalakat a karakterjelekhez. Az EOT-fájlok kisebb méretűek, mert LZ-tömörítéssel tömörítik őket. Az EOT egy Microsoft-eszközt használ a meglévő TTF/OTF betűtípusok létrehozásához.

## Rövid története

Az EOT fontot 2007-ben adták be a W3C-nek a CSS3 részeként, de a távoli rendszerre való tartós telepítés követelménye miatt az elutasítás oka lett. 2008 márciusában újra benyújtották, de a W3C végül a [Web Font Format](/hu/font/woff/) (WOFF) lehetőséget választotta, amelyet akkor szabványosítottak.

## EOT fájlformátum

Az EOT fájlformátum részletei a [W3 benyújtási oldalon] (https://www.w3.org/Submission/EOT/#FileFormat) találhatók, és kidolgozza az e betűformátum által használt szerkezetet. Az EOT egyetlen EMBEDDEDFONT struktúrából áll, amely elegendő alapvető információt nyújt a hte betűtípus nevéről és a támogatott karakterekről. Ezen információk becsomagolása lehetővé teszi a felhasználói ügynökök számára, hogy elkerüljék a betűkészlet kicsomagolását, kicsomagolását vagy telepítését, ha az már megtalálható a gépen.

### EMBEDDEDFONT Struktúra
Az EMBEDDEDFONT struktúra három felülvizsgálaton esett át, és minden egyes revízióval további adatok kerültek a struktúra végére. Az EMBEDDEDFONT szerkezet utolsó változata az alábbiak szerint készült.

|Adattípus|Bejegyzés neve|Leírás|
---|---|---|
|unsigned long|EOTSize|A teljes szerkezethossz bájtban (beleértve a karakterlánc- és betűtípusadatokat)|
|unsigned long|FontDataSize|Az OpenType betűtípus hossza (FontData) bájtban|
|unsigned long|Verzió|Ennek a formátumnak a verziószáma - 0x00020002|
|aláíratlan hosszú|Zászlók|Zászlók feldolgozása|
|byte[10]|FontPANOSE|A font PANOSE értéke - Lásd: http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|Windows rendszerben ez a TEXTMETRIC.tmCharSetből származik. Ez az érték határozza meg a betűtípus karakterkészletét. A DEFAULT_CHARSET (0x01) azt jelzi, hogy nincs preferencia. - Lásd: http://msdn2.microsoft.com/en-us/library/ms534202.aspx|
|byte|Dőlt|Ha az ITALIC bitje be van állítva az OS/2.fsSelectionben, az érték 0x01 lesz – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|A betűtípus súlyértéke – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Típusjelzők, amelyek információt nyújtanak a beágyazási engedélyekről – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|Mágikus szám az EOT-fájlhoz – 0x504C. Adatsérülések ellenőrzésére szolgál.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (0-31 bit) – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (32-63 bit) – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (64-95 bitek) – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (96-127 bitek) – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (0-31 bitek) – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (32-63 bit) – Lásd: http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment – Lásd: http://www.microsoft.com/typography/otspec/head.htm|
|aláíratlan hosszú|Fenntartva1|Fenntartva - 0-nak kell lennie|
|aláíratlan hosszú|Fenntartva2|Fenntartva - 0-nak kell lennie|
|aláíratlan hosszú|Fenntartva3|Fenntartva - 0-nak kell lennie|
|aláíratlan hosszú|Fenntartva4|Fenntartva - 0-nak kell lennie|
|unsigned short|Padding1|Padding a hosszú igazítás fenntartásához. A kitöltés értékét mindig 0x0000-ra kell állítani.|
|unsigned short|FamilyNameSize|A FamilyName tömb által használt bájtok száma|
|byte|FamilyName[FamilyNameSize]|UTF-16 karakterek tömbje FamilyNameSize bájt hosszúságban. Ez az angol nyelvű betűtípuscsalád karakterlánc, amely a betűtípus névtáblázatában található (névazonosító = 1) - Lásd: http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|A kitöltés értékét mindig 0x0000-ra kell állítani.|
|unsigned short|StyleNameSize|A StyleName által használt bájtok száma|
|byte|StyleName[StyleNameSize]|UTF-16 karakterek tömbje StyleNameSize bájt hosszúságban. Ez az angol nyelvű betűtípus-alcsalád karakterlánc, amely a betűtípus névtáblázatában található (névazonosító = 2) - Lásd: http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|A kitöltés értékét mindig 0x0000-ra kell állítani.|
|unsigned short|VersionNameSize|A VersionName által használt bájtok száma|
|bytes|VersionName[VersionNameSize]|UTF-16 karakterek tömbje VersionNameSize bájt hosszúságban. Ez a betűtípus névtáblázatában található angol nyelvű verzió (névazonosító = 5) - Lásd: http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|A kitöltés értékét mindig 0x0000-ra kell állítani.|
|unsigned short|FullNameSize|A FullName által használt bájtok száma|
|byte|FullName[FullNameSize]|UTF-16 karakterek tömbje FullNameSize bájt hosszúságban. Ez az angol nyelvű teljes név karakterlánc, amely a betűtípus névtáblázatában található (névazonosító = 4) - Lásd: http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|A kitöltés értékét mindig 0x0000-ra kell állítani.|
|unsigned short|RootStringSize|A RootString tömb által használt bájtok száma|
|byte|RootString[RootStringSize]|RootStringSize bájt hosszúságú UTF-16 karakterek tömbje.|
|unsigned long|RootStringCheckSum|RootString CheckSum értéke. Lásd az alábbi algoritmust a RootStringChecksum feldolgozására.|
|unsigned long|EUDCCodePage|Az EUDC betűtípus-támogatásához szükséges kódlapérték.|
|unsigned short|Padding6|A kitöltés értékét mindig 0x0000-ra kell állítani.|
|unsigned short|SignatureSize|A Signature tömb által használt bájtok száma. Jelenleg lefoglalt, és 0x0000-ra kell állítani.|
|byte|Aláírás[SignatureSize]|Jelenleg lefoglalva. Ha a SignatureSize 0x0000, ennek a tömbnek nincs hossza.|
|unsigned long|EUDCFlags|Az EUDC betűtípus jelzőinek feldolgozása. A tipikus értékek a következők lehetnek: TTEMBED_XORENCRYPTDATA és TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|A Signature tömb által használt bájtok száma.|
|byte|EUDCFontData[EUDCFontSize]|Az EUDC betűtípusadatokhoz használt bájtok száma. Ha az EUDCFontSize 0x00000000, ennek a tömbnek nincs hossza.|
|byte|FontData[FontDataSize]|Az EOT-fájl betűtípusadatai. Az adatok tömöríthetők vagy XOR-titkosíthatók, ahogy azt a feldolgozási jelzők jelzik.|

## Hivatkozások

* [EOT fájlformátum](https://www.w3.org/Submission/EOT/)
* [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Fontbeágyazás](https://en.wikipedia.org/wiki/Font_embedding)


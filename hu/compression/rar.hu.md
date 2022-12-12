{
  "date" : "2019-10-11",
  "keywords" :[ "rar fájl", "rar fájl formátum", "mi az a rar fájl", "fájl", "rar példa", "rar fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Mi az a RAR fájlkiterjesztés és API-k, amelyek RAR fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a RAR fájl?

A .rar kiterjesztésű fájlok olyan archív fájlok, amelyeket az információk tömörített vagy normál formában történő tárolására hoznak létre. A RAR, amely a Roshal ARchive fájlformátum rövidítése, egy védett fájlformátum, amelyet Eugene Roshal hozott létre 1995-ben, aki orosz szoftvermérnök volt. A formátumot fájlok archiválására használják különböző módszerekkel, beleértve a különféle tömörítési technikákat. Számos alkalmazási szoftver áll rendelkezésre Windows, Linux és MacOS rendszerhez a RAR fájlok kivonásához. A RARLab WinRAR szoftvere a Shareware fájlarchiváló segédprogram (40 napig ingyenes) Microsoft Windows platformon; a szoftvert ugyanaz a szerző, Eugene Roshal portolta Linuxra (csak kivonatként).

## Verziók A RAR fájlformátum története

* v1.3 (eredeti, nem rendelkezik "Rar!" aláírással)
* v1.5
* v2.0 - WinRAR 2.0 és Rar verzióval jelent meg MS-DOS 2.0-hoz
* v2.9 – a WinRAR 3.00-as verziójában jelent meg
* v5.0 – a WinRAR 5.0 és újabb verziói támogatják

## A RAR formátum legfontosabb jellemzői

A RAR már régóta jelen van a területen, és az egyik kedvenc archiválási fájlformátum. A RAR formátum főbb jellemzői a következők:

**`Magas tömörítési arány:`** Kiváló a [ZIP]-hez képest (/hu/compression/zip/), összehasonlítható a 7z és a zipx formátummal.

**`Erős fájltitkosítás a tervezés során:`** A titkosított RAR4 archívumok AES-128 alapú titkosításra támaszkodnak, míg a titkosított RAR5 archívumok AES-256 titkosításra, továbbfejlesztett kulcsütemezéssel

**`Speciális hibajavítási és adat-helyreállítási lehetőségek:`** opcionális helyreállítási rekordok az archívum létrehozása során

**`Fájlméret:`** Minimum 20 bájt és maximum 2^63 bájt (az archívum teljes méretéből 8 exabájt)

**`Többkötetes RAR archívum:`** Lehetőség a nagy archívumok felosztására több kisebb fájlra a hálózaton keresztüli átvitel megkönnyítése érdekében. Ebben az esetben a fájlkiterjesztések 1-gyel nőnek a megosztott kötetek megjelenítéséhez

## RAR fájlformátum

A RAR formátum teljes specifikációja nem elérhető nyilvánosan, ezért a formátum részleteit nem lehet tömören megfogalmazni.

### Általános archív elrendezés

Az 5.0-s verzióban bevezetett RAR fájlformátum általános elrendezése a következő:

|Fájlformátum
---|
|Önkicsomagoló modul (opcionális)
|RAR 5.0 aláírás
|Archiválási titkosítási fejléc (opcionális)
|Fő archívum fejléce
|A megjegyzés szolgáltatás fejlécének archiválása (opcionális)
Fájl fejléc 1
|Szolgáltatásfejlécek (NTFS ACL, adatfolyamok stb.) az előző fájlhoz (opcionális)
|...
|Fájlfejléc N
|Szolgáltatásfejlécek (NTFS ACL, adatfolyamok stb.) az előző fájlhoz (opcionális)
|Helyreállítási rekord (opcionális)
|Az archívum vége fejléc

A RAR-fájlok fent említett egyes szakaszairól a [RAR 5.0 fájlformátum-specifikációk](https://www.rarlab.com/technote.htm#arcstruct) dokumentumban olvashat.

#### Önkicsomagoló RAR-archívumok

Ha maga a RAR fájl önkicsomagoló, az önkicsomagoló információ az archív aláírást megelőző fájl elején található. Mérete és tartalma nincs meghatározva.

#### RAR 5.0 aláírás

A RAR aláírás egy 8 bájtos fejléc, amely a következő varázsszámokból áll:

0x 52 61 72 21 1A 07 00

ahol

0x6152 - HEAD_CRC

0x72 – HEAD_TYPE

0x1A21 – HEAD_FLAGS

0x0007 - HEAD_SIZE

## Hivatkozások

* [RAR 5.0 archív formátum](https://www.rarlab.com/technote.htm)
* [RAR – a Wikipedia által](https://en.wikipedia.org/wiki/RAR_(file_format))


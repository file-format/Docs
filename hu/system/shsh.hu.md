{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH fájl – iPhone/iPod Touch SHSH Blob fájlformátum",
  "description":"További információ arról, hogy mi az SHSH-fájl.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Mi az SHSH fájl?

Az SHSH-fájl, más néven Signature HaSH, egy digitális aláírás, amelyet az Apple használ az iOS-eszközök, például iPhone, iPad és iPod firmware-frissítéseinek hitelesítésére és ellenőrzésére.

## Különbség az SHSH és az SHSH2 fájlformátumok között

Az SHSH2-fájlhoz hasonlóan az SHSH-fájl is egy egyedi azonosítót tartalmaz az eszközhöz, amelyet "ECID"-nek (Exclusive Chip ID) neveznek, valamint információkat tartalmaz az eszközre telepített firmware-verzióról. Az SHSH-fájlokat azonban az iOS régebbi verzióiban használták (az iOS 10 előtt), és azóta SHSH2-fájlok váltották fel őket.

## SHSH fájlformátum - További információ

Az SHSH-fájlokat a rendszer bináris fájlformátumban menti a lemezre. Ennek a fájlformátumnak a belső fájlszerkezetének részletei nem érhetők el nyilvánosan.

Az SHSH-fájlok fontosak azoknak a felhasználóknak, akik vissza akarják frissíteni eszközük firmware-jét egy olyan korábbi verzióra, amelyet már nem ír alá az Apple. Ha elmenti az SHSH-fájlokat egy adott firmware-verzióhoz, amikor azt még az Apple aláírja, a felhasználók később felhasználhatják őket arra, hogy megkerüljék az Apple aláírás-ellenőrzését, és telepítsék az adott firmware-verziót eszközükre. Ezt a folyamatot "jailbreaknek" is nevezik.

## Hivatkozások

* [SHSH Blob – a Wikipedia által](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)


{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extension", "file", "format", "system", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows kabinetfájl",
  "description":"További információ a CAB fájlformátumról és az API-król, amelyek CAB-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Mi az a CAB fájl? ##

A .cab kiterjesztésű fájl egy Windows kabinetfájlhoz tartozik, amely a rendszerfájlok kategóriájába tartozik. Ez egy olyan fájl, amely archív fájlformátumban van mentve a Microsoft Windows olyan verzióiban, amelyek támogatják a tömörített adatalgoritmusokat, például az [LZX](/hu/compression/lzx/), a Quantum és a [ZIP](/hu/compression/zip/ ). A fájl létfontosságú, ha egy felhasználó vagy fejlesztő szoftvertelepítési adatokat és fájlokat szeretne tartalmazni és megosztani. A veszteségmentes adattömörítés és az ezekben a fájlokban található digitális tanúsítványok révén ez a fájl tökéletes az ilyen fájlok tárolására és megosztására. Támogatja a különböző Microsoft-telepítőket, például az Eszköztelepítőt, a SetUp API-t és az AdvPakot.

## Rövid története ##

A CAB fájl egy adattömörítési fájltípus, amelyet a Microsoft fejlesztett ki. Eredetileg "Gyémánt" volt a neve, de aztán CAB fájlként vált ismertté, ami a "Cabinet" szó rövidítése.

## Műszaki specifikáció ##

Egy CAB-fájl általában legfeljebb 65535 mappát tartalmazhat, amelyek viszont egyenként legfeljebb 65536 fájlt tartalmazhatnak. A CAB fájltárolási mechanizmus idő- és helytakarékos, mivel minden mappát tömörített blokkként ment, ahelyett, hogy minden egyes fájlt külön-külön tömörítene és tárolna. Az üres mappák nem tárolhatók a CAB archív mappáiban. A CAB fájlt először a Microsoft fejlesztette ki, és különféle telepítőkben használják, például az InstallShieldben, kissé eltérő formátumban. A CAB-fájlok általában önkicsomagoló programokhoz kapcsolódnak. A Microsoft CAB fájlok könnyen felismerhetők egyedi jelölőjüknek köszönhetően, amely segít a formátum azonosításában. Az összes Microsoft CAB-fájl egyedi jelölője egy négyszavas előtag, az MSCF. Ezt a kódot látva a felhasználó könnyen megkülönböztetheti a Microsoft CAB fájlokat más fájloktól, és ennek megfelelően használhatja azt tömörítőben vagy verzióban. A fájlok tömöríthetők több szoftvertelepítési adattal, vagy a jelenlegi adatok kicsomagolhatók a megfelelő szoftver segítségével.


## CAB példa ##

A következő példa a fájlok és mappák közötti kapcsolatot szemlélteti CAB-fájlstruktúrában:

{{< figure src="../cab.png" alt="CAB fájl formátum" >}}

## Hivatkozási szám

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))

{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPK fájlformátum",
  "description":"További információ az NPK fájlformátumról és az NPK-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Mi az NPK fájl?

Az NPK-fájl egy szoftverfrissítési csomagfájl, amelyet a **MikroTik** útválasztók használnak az útválasztó operációs rendszerének frissítésére. Tömörített bináris archívumként érkezik, amelyet az útválasztóba töltenek be a szoftverfrissítések telepítéséhez. Az NPK-fájlokban található információk magukban foglalják a hálózati információkat, például az IP-címet és az IP-szolgáltatást, a csatlakozókra vonatkozó információkat (Ethernet interfészek és soros port), az e-mail beállításokat, a hídkonfigurációt és a helyi felhasználókezelést.

## NPK fájlformátum

Az NPK-fájlok tömörített bináris archívumként kerülnek tárolásra. Ez egy zárt fájlformátum, amelyet csak maguk a MikroTik használnak. Nem célja RouterOS-bővítmények létrehozása harmadik feleken keresztül. Az NPK-fájlokat maga a MikroTik karbantartja, és ezek frissített verziói letölthetők a [MikroTik](https://mikrotik.com/download) webhely letöltési szakaszaiból.

Amikor egy NPK-fájlt feltöltenek egy útválasztóra, az útválasztó operációs rendszere csak akkor lép életbe, ha újraindítják. Ezért az útválasztó operációs rendszerének frissítéséhez újra kell indítani.

## Hivatkozások

* [MikroTik – Router OS frissítése](https://mikrotik.com/download)
* [Hogyan hozzunk létre NPK-fájlokat](https://forum.mikrotik.com/viewtopic.php?t=87126)


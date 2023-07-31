{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CMS fájlformátum – kapcsolatkezelő szolgáltatási profilfájl",
  "description":"További információ a CMS-fájlokról és az API-król, amelyek CMS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Mi az a CMS fájl?

A CMS-fájl egy adatfájl, amely a Microsoft Windows Connection Manager által használt profilinformációkat tartalmazza. Lehetővé teszi a távoli felhasználók számára a hálózathoz való csatlakozást ezen profilinformációk segítségével. A CMS-fájlban tárolt információk a felhasználó operációs rendszerére és a távoli felhasználó és a hálózat közötti kapcsolat létrehozására használt engedélyekre vonatkozó adatokat tartalmaznak. A CMS-rendszergazdák a Connection Manager Administrator Kit (CMAK) segítségével állítják elő a CMS-fájlokat.

## CMS fájlformátum – További információ

A CMS-fájlok nem gyakran találhatók a felhasználói gépeken. Mivel ezeket kifejezetten arra használják, hogy távoli felhasználókat engedélyezzenek a hálózathoz, ezeket azokon a számítógépeken találhatja meg, amelyek a vállalati hálózathoz vagy valamilyen speciális célú irodához való csatlakozásra szolgálnak. A legtöbb esetben egy szervezeti hálózathoz, például a virtuális magánhálózathoz (VPN) való csatlakozáshoz használják, amely csak egy vállalat számára van fenntartva. Hálózati rendszergazdaként beállíthatja a hozzáférést egy ilyen hálózathoz a Connection Manager segítségével, hogy lehetővé tegye számára a vállalati hálózathoz való hozzáférést egy távoli helyről.

### Mi az az insdie CMS?

A CMS-profilfájl a Connection Manager segítségével jön létre, és más konfigurációs fájlokkal együtt csomagolódik, mielőtt a távoli felhasználó rendelkezésére bocsátaná. Ezek a további fájlok tartalmazhatnak egy CMP- és egy INF-fájlt, amelyek egy [EXE](/hu/executable/exe/) fájlba vannak csomagolva. Ez a teljes csomag a távoli felhasználó rendelkezésére áll a hálózathoz való csatlakozáshoz.

## Hivatkozások

* [A Windows Connection Manager megértése és konfigurálása](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)


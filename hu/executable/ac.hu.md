{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Ismerje meg az AC fájlformátumot és az API-kat, amelyek ACCDB fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "AC fájlformátum - Autoconf Script fájl",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-hu",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Mi az AC fájl?

Az AC fájl az Autoconf szkriptfájl. Az **Autoconf** M4 makrók bővíthető csomagja, amely shell-szkripteket állít elő a szoftverforráskód-csomagok automatikus konfigurálásához. Ezek a parancsfájlok kézi felhasználói beavatkozás nélkül képesek a csomagokat sokféle UNIX-szerű rendszerhez igazítani. Az Autoconf egy sablonfájlból létrehoz egy konfigurációs parancsfájlt egy csomaghoz, amely felsorolja a csomag által használható operációs rendszer-szolgáltatásokat M4 makróhívások formájában.

Producing configuration scripts using Autoconf requires GNU M4. Az Autoconf beállítása előtt telepítenie kell a GNU M4-et (legalább az 1.4.6-os verziót, bár az 1.4.13-as vagy újabb ajánlott), hogy az Autoconf konfiguráló szkriptje megtalálja azt. Az Autoconf által előállított konfigurációs szkriptek önállóak, így a felhasználóknak nincs szükségük Autoconf-ra (vagy GNU M4-re).

## AC fájl - Mivel nyitható meg?

Az AC az Automatic Configuration rövidítése. Ez egy GNU Autoconf által generált szkript, amely lehetővé teszi a szoftver forráskódjának adaptálását a különböző Posix-szerű rendszerekhez a csomagban található szükséges funkciók tesztelésével. A szkriptet AC fájlnak nevezik.

## Az Autotools fő összetevői

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Az Autotools olyan kapcsolódó csomagok gyűjteménye, amelyek együttes használata esetén a hordozható szoftverek létrehozásával járó nehézségek jelentős része megszűnik. Ezeket az eszközöket néhány viszonylag egyszerű, felfelé szállított bemeneti fájllal együtt használják a csomag összeállítási rendszerének létrehozására.

**Alapvető áttekintés az Autotools fő összetevőinek egymáshoz való illeszkedéséről.**

!{{HIPERLINK1}}

Egy egyszerű beállításban:

- Az `autoconf` program a `configure.in` vagy a `configure.ac` fájlból állít elő egy konfigurációs szkriptet.
- Az `automake` program egy Makefile.in fájlt készít a Makefile.am fájlból.
- A configure szkript fut egy vagy több Makefile fájl létrehozására a Makefile.in fájlokból.
- A `make` program a Makefile-t használja a program fordításához.

## Hivatkozások
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Az Autotools alapjai](https://devmanual.gentoo.org/general-concepts/autotools/index.html)




{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ismerje meg az Age of Empires 2 Expansion Replay MGX fájlformátumát és az MGX-fájlok létrehozására és megnyitására alkalmas API-kat.",
  "title" : "MII fájl – Wii Virtual Avatar fájlformátum",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-hu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Mi az a MII fájl?

A MII fájl egy virtuális avatar fájlformátum, amelyet virtuális avatarok tárolására használnak a Nintendo Wii játékkonzolon. Ezek a fájlok olyan információkat tartalmaznak, mint az avatar megjelenése, mozgása és animációi. Használhatók játékokban, közösségi hálózati alkalmazásokban és más szoftverekben a Wii-n. A MII-fájl egyéb jellemzőket is tartalmaz az avatárral kapcsolatban, például a nemet, a hajszínt, a bőrszínt, az arcvonásokat és a szemtípust.

A MII-fájlt a [My Avatar Editor](https://rc24.xyz/goodies/mii/) használatával nyithatja meg.

## MII fájl formátum

A MII fájlformátum részletes meghatározása itt: [Wii Brew](https://wiibrew.org/wiki/Mii_data). A MII-fájlban lévő karakterláncok Unicode formátumban (UTF-16) vannak tárolva, big-endian.

### MI blokk

A MII fájl adatait a Wiimote két blokkban tárolja. Minden blokk 750 bájt hosszú, 2 bájt CRC-vel, így összesen 752 bájt. Minden blokk egy 4 bájtos értékkel ('RNCD') kezdődik, amely a MII fájlformátum varázslatos számának tűnik.

## Hogyan készítsünk MII fájlokat?

A Nintendo Wii-hez többféleképpen hozhat létre avatarokat:

1. `A beépített Mii csatorna használata a Wii-n:` Ez a csatorna lehetővé teszi egyéni avatarok létrehozását különféle eszközök segítségével, beleértve az arcvonásokat, a test alakját és a ruházatot. Miután létrehoztad az avatarod, elmentheted Mii-fájlként, és felhasználhatod játékokban és más szoftverekben a Wii-n.

1. `A Mii Maker alkalmazás használata a Nintendo 3DS-en:` A Mii Maker alkalmazás lehetővé teszi egyéni avatarok létrehozását a Nintendo 3DS érintőképernyőjének és kamerájának segítségével. Az avatar létrehozása után elmentheti Mii-fájlként, és vezeték nélküli kapcsolaton keresztül átviheti Wii-re.

1. Harmadik féltől származó szoftverek használata: Egyes fejlesztők olyan szoftvereket hoztak létre, amelyek lehetővé teszik egyéni avatarok létrehozását a Wii számára. Ezt a szoftvert általában számítógépen való használatra tervezték, és további lépésekre lehet szükség az avatar Wii-re való átviteléhez.

1. `Előre elkészített avatarok használata: Egyes játékokhoz és egyéb Wii-szoftverekhez előre elkészített avatarok tartoznak, amelyeket használhat.

Minden esetben Nintendo-fiókkal kell rendelkeznie az avatar létrehozásához és a Wii-re való mentéséhez.

## Hivatkozások

* [My Avatar Editor](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)



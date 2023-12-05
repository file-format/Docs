{
"dátum": "2023-05-02",
  "keywords": [
"obi fájl",
"mi az obi fájl",
"mi az obi fájl formátuma",
"fájl",
"obi fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "OBI-fájlformátum - Outlook RSS-előfizetési fájl",
  "description":"További információ az OBI-formátumról és az OBI-fájlok létrehozására és megnyitására alkalmas API-król.",
"linktitle": "OBI",
  "menu": {
    "docs": {
      "identifier": "settings-obi",
      "parent": "settings"
}
},
"lastmod": "2023-05-02"
}

## Mi az OBI fájl?

Az OBI-fájl egy Outlook RSS-előfizetési fájl, amely lehetővé teszi a felhasználók számára, hogy előfizessenek egy RSS-hírcsatornára a Microsoft Outlook alkalmazásban. Az RSS a Really Simple Syndication rövidítése, amely egy webes hírcsatorna-formátum, amelyet gyakran frissített tartalom, például blogbejegyzések, hírcímek vagy podcastok közzétételére használnak.

Az Outlook RSS-hírcsatornájára való feliratkozáshoz a felhasználók rákattinthatnak az RSS-hírcsatorna hivatkozására egy webhelyen, vagy kimásolhatják az RSS-hírcsatorna URL-címét, és beilleszthetik az Outlook „Új RSS-hírcsatorna hozzáadása” párbeszédpanelébe. Az Outlook ezután rendszeresen ellenőrzi az RSS-hírcsatornát új tartalom után, és megjeleníti azt a felhasználó RSS-hírcsatorna mappájában.

Az Outlook RSS-előfizetéses fájlok kiterjesztése „.rss”. Ezek a fájlok tartalmazzák az RSS-hírcsatorna URL-címét, és felhasználhatók RSS-hírcsatorna-előfizetések megosztására másokkal, vagy RSS-hírcsatorna-előfizetések biztonsági mentésére és visszaállítására.

## OBI fájlformátum - További információ

Az OBI-fájlok OPML-fájlként (Outline Processor Markup Language) ismertek, és a Microsoft Outlook alkalmazásban előfizetett RSS-hírcsatorna URL-címeinek listáját tartalmazzák.

Amikor a felhasználó RSS-hírcsatornáit OBI-fájlba exportálja, az tartalmazza az összes RSS-hírcsatorna listáját, amelyre előfizetett, beleértve az egyes hírcsatornák címét, a hírfolyam URL-címét és minden egyéb releváns információt. Ez lehetővé teszi a felhasználók számára, hogy RSS-hírcsatorna-előfizetéseiket könnyen átvigyék egy másik RSS-olvasóba, vagy biztonsági másolatot készítsenek előfizetéseikről.

Az OBI-fájlok RSS-hírcsatorna-előfizetések importálására is használhatók a Microsoft Outlookba vagy más RSS-olvasóba. Az OBI-fájl Outlookba való importálásához a felhasználók a "Fájl" > "Megnyitás és exportálás" > "Importálás/exportálás" > "Importálás másik programból vagy fájlból" > "Következő" > "RSS-hírcsatornák importálása OPML-fájlból" lehetőségre kattinthatnak. majd tallózással keresse meg az OBI fájl helyét a számítógépén.

## Mi az OBI fájl formátuma?

Az Outlook RSS-előfizetési fájl, más néven OBI-fájl, XML-t (eXtensible Markup Language) használ a fájl szerkezetének és tartalmának meghatározásához.

Az OBI-fájlok egymásba ágyazott elemek sorozatából állnak, amelyek mindegyike saját attribútum- és értékkészlettel rendelkezik. Az OBI-fájl fő eleme a "vázlat" elem, amely információkat tartalmaz az RSS-hírfolyamról, beleértve a hírfolyam címét, a hírfolyam URL-címét és minden egyéb releváns információt.

Minden "vázlat" elem tartalmazhat gyermekelemeket is, amelyek almappákat vagy alkategóriákat képviselnek az RSS feedlistán belül. Az OBI-fájl felépítése lehetővé teszi az RSS-hírcsatorna-előfizetések egyszerű szervezését és kezelését, és felhasználható az előfizetések átvitelére a különböző RSS-olvasók között, illetve az előfizetések biztonsági mentésére és visszaállítására.

## Hivatkozások
* [Mik azok az RSS-hírcsatornák?](https://support.microsoft.com/en-us/office/what-are-rss-feeds-e8aaebc3-a0a7-40cd-9e10-88f9c1e74b97)


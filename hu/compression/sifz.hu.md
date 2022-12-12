{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SIFZ fájlformátum - Synfig Studio tömörített projektfájl",
  "description":"További információ a SIFZ fájlformátumról és az API-król, amelyek SIFZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## Mi az a SIFZ fájl?

A SIFZ-fájl egy gzip-ben tömörített SIF-fájl, amelyet a **Synfig Studio** nyílt forráskódú 2D animációkat készítő alkalmazás hozott létre. Több grafikus elemet tartalmaz, amelyek pótolják az animációt. Az általános animációs tartalom formákkal, ecset- vagy ceruzavonásokkal és szöveggel megtöltött vászon kombinációjával épül fel. Mindezek a saját pozíciójuk szerint vannak elrendezve, a sugár, az érintő, a szög, a csúcs és a szélesség fogantyúi szerint. A SIFZ-fájlok a [Synfig Studio] segítségével nyithatók meg (https://www.synfig.org/).

## SIFZ fájlformátum

A SIFZ fájlok tömörített [ZIP](/hu/compression/zip/) fájlok, amelyek a gzip tömörítési módszerrel vannak csomagolva. A Synfig filmminőségű animációk készítésére szolgál vektoros és bittérképes grafikával. A régi képkockánkénti animáció-készítési módszertől eltérően ez lehetővé teszi, hogy jobb minőségű 2D animációkat készítsen kevesebb erőforrással.

A tömörített SIFZ fájlok kisebbek, mint a tömörítetlen SIF fájlok. Ez megkönnyíti az alacsony sávszélességű internetkapcsolatokon keresztüli átvitelt is.

## Hivatkozások

* [Synfig nyílt forráskódú – Github](https://github.com/synfig/synfig/)
* [Synfig Documentation](https://synfig.readthedocs.io/en/latest/index.html)


{
  "date" : "2021-10-20",
  "keywords" :[ "sfar fájl", "sfar fájlformátum", "mi az sfar fájl", "fájl", "sfar példa", "Mass Effect 3 DLC fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tudjon meg többet a Mass Effect 3 SFAR fájlformátumáról és az API-król, amelyek SFAR fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"SFAR – Mass Effect 3 DLC fájl",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Mi az SFAR fájl?

A .sfar kiterjesztésű fájl egy játékadatfájl, amelyet a Mass Effect 3 használ a DLC (letölthető tartalom) tömörített, védett archívumban való tárolására. A Mass Effect 3 egy játék, amelyet az Electronic Arts, egy vezető játékfejlesztő cég készített. Az SFAR-fájlban tárolt DLC-tartalom a játék további tartalommal és funkciókkal való bővítésére szolgál.

## SFAR fájlformátum – További információ

Az SFAR-fájlokat tömörített archív fájlokként tárolják/mentik bináris fájlformátumban. Ezek LZX és LZMA tömörítési algoritmusokat is használnak a tartalom tömörítésére. Az SFAR fájlok az ME3 Explorerhez mellékelt DLC-szerkesztővel nyithatók meg. Az SFAR mellett a DLC Editor más játékfájlokat is ki tud bontani, mint például a [PCC](/hu/game/pcc/).

## SFAR fájlformátum specifikációi

Az SFAR fájl a következő négy fő részre oszlik.

### SFAR fejléc

Az SFF fejléc információkat tartalmaz a fájlt alkotó különféle darabokról.

### SFAR fájltábla

Az SFAR fájltábla tartalmazza a fájlbejegyzések listáját, ahol minden bejegyzés 30 bájt hosszú.

### Blokkméret táblázat

A Block-Size több bejegyzést tartalmaz, ahol minden bejegyzés 2 byes hosszúságú. Ez az érték adja meg a Fájltáblázat bejegyzésének megfelelő blokkméretet.

### Blokkok

Az SFAR-fájl blokkdarabjai az SFAR-fájlon belüli adatokat tartalmazzák.

## Hivatkozások

* [DLC SFAR fájlformátum – kutatás](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)


{
  "date" : "2021-09-08",
  "keywords" :[ "pcc fájl", "pcc fájl formátum", "mi az a pcc fájl", "fájl", "pcc példa", "pcc fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a Mass Effect PCC fájlformátumról és az API-król, amelyek PCC fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"PCC – Mass Effect Package File",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Mi az a PCC fájl?

A .pcc fájl egy [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) fájl, amely játékadatokat tartalmaz a játék tartalmának, például modellek, textúrák és szobák. A Mass Effect 2 és 3 az első lövöldözős játékok, amelyek az Unreal Engine 3 játékmotoron alapulnak. A játékot eredetileg a [Bioware](https://www.bioware.com/about/) fejlesztette ki, aki a játékerőforrások többségét saját PCC-fájlformátumában tartotta. A Bioware-t az Electronic Arts, a világ egyik vezető interaktív szórakoztató szórakoztatóipari kiadója vásárolta meg.

## PCC fájlformátum - További információ

A PCC-fájlok tömörített és/vagy tömörítetlen struktúrákat tartalmaznak, amelyek hozzájárulnak a teljes fájlszervezéshez.

### Tömörített PCC szerkezet

A tömörített PCC-fájl táblázatokból és adatokból áll, amelyek darabokra vannak szegmentálva. Minden egyes darab változó számú tömörített blokkot tartalmaz.

* "Chunks Header" - 16 bájtos közös fejléc, amely információkat tartalmaz a darabokról.
* "Chunk Header" - 16 bájtos fejléc, amely információkat tartalmaz a blokkűrlapban található nyers tömörített adatokról.

### Tömörítetlen PCC-struktúra

A tömörítetlen PCC fájlok a következő öt részre oszthatók.

* `Header` - alapvető információkat tartalmaz a PCC fájl szerkezetéről.
* `Name Table` - a csomagban található nevet tartalmazza, beleértve az import osztályokat, az exportálást és az export tulajdonságokat.
* `Import Table` - tartalmazza a PCC által importált összes osztályt és objektumot.
* `Export Table` - tartalmazza a csomagban tárolt összes objektumot. Az egyes exportok mérete eltérő lehet.

## Hivatkozások

* [Me3Explorer – PCC fájlformátum](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)


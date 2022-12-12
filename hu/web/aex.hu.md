{
  "date" : "2019-10-11",
  "keywords" :[ "aex", "aex fájl", "fájl formátum", "fájl típusa", "mi az aex fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AEX – Alpha Five Compiled Global Functions File",
  "description" :"Tanulja meg, hogy mi az AEX fájl és API-k, amelyek AEX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AEX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-07"
}

## Mi az AEX fájl?

Az AEX-fájl (.aex kiterjesztéssel) egy lefordított [Xbasic](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml) fájl, amely globális függvények lefordított programkódját tartalmazza. Használható webes alkalmazásokban, ha szerveroldali [.a5w](/hu/web/a5w/) oldalakról hívja meg őket. Az AEX fájlok betöltése és eltávolítása az a5w_load_aex és a5w_unload_aex függvények A5W fájlokból való meghívásával történt. Az új megvalósításban azonban ezek a fájlok az a5_application.5i fájlba való felvétellel töltődnek be a memóriába. Az Xbasic programozási nyelvet az Alpha Anywhere szoftver használja mobil és webes alkalmazások fejlesztésére.

## AEX fájlformátum - További információ

Az AEX fájlokat a rendszer bináris fájlformátumban menti lemezre, és Xbasic-ben írt függvénykódokat tartalmaz. Az Xbasic script parancsutasítások határozzák meg a végrehajtás szerkezetét és folyamatát, beleértve az ismételt művelet végrehajtását vagy leállítását, vagy a feltételek alapján két vagy több lépés közötti választást. Az [Xbasic Language Reference](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml) című dokumentumban részletes információkat találhat róla.

## Hivatkozások

* [Alpha Five](https://www.alphasoftware.com/)
* [Alpha Five Documentation](https://documentation.alphasoftware.com/documentation/pages/index.html)
* [Xbasic útmutató](https://documentation.alphasoftware.com/pages/Guides/Xbasic/index.xml)


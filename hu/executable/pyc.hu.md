{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a PYC fájlformátumról és az API-król, amelyek PYC fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"PYC fájlformátum - Python összeállított fájl",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Mi az a PYC fájl?

A PYC fájl egy lefordított kimeneti fájl, amelyet Python programozási nyelven írt forráskódból állítanak elő. Amikor a PY fájlt Python interpreter segítségével futtatja, a program bájtkóddá konvertálja a végrehajtáshoz. Ugyanakkor a lefordított bájtkód .pyc fájlként is elmentésre kerül, hogy a gyorsítótárból később újra felhasználható legyen, ha lehetséges.

## A PYC fájlformátum felépítése

A PYC fájlok bájtkódban vannak, és a fájlformátum-specifikációik nem érhetők el nyilvánosan. Egyes források vizsgálata azonban azt mutatja, hogy a [egy PYC-fájl szerkezete](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) a következőkből áll:

* `Négybájtos mágikus szám`r - Egyszerűen két bájt, amely a rendezőkód minden változásával változik, majd két bájt 0d0a.
* `Négybájtos módosítási időbélyeg` – A .pyc-et létrehozó forrásfájl Unix módosítási időbélyege, hogy újra lehessen fordítani, ha a forrás megváltozik.
* "Egy rendezett kódobjektum" - a kódobjektum marshal.dump kimenete, amely a forrásfájl fordításának eredménye.

## Hivatkozások

* [A .pyc fájlok szerkezete](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)


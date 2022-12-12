{
  "date" : "2021-07-29",
  "keywords" :[ "md5 fájl", "md5 fájlformátum", "mi az md5 fájl", "fájl", "md5 példa", "md5 fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - MD5 ellenőrzőösszeg fájl",
  "description":"További információ az MD5 fájlokról és az API-król, amelyek MD5 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Mi az MD5 fájl?

Az MD5 fájl egy ellenőrző összeg fájl, amelyet a fájl integritásának ellenőrzésére használnak. Hasonló a társított fájl ujjlenyomatához, és egyedileg generálódik egy olyan algoritmus segítségével, amely a fájl bitjeinek számát használja. A fájl ellenőrzésére szolgál olyan szoftverrel, mint például az [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Az MD5 fájlok használatának egyik előnye annak ellenőrzése, hogy a letöltött fájlok nem sérültek-e.

## MD5 fájlformátum – További információ

Az MD5 fájlokat általában az eredeti fájlnévvel, de .md5 kiterjesztéssel menti a rendszer. Ha például a társított fájlnév „abc_987_123456.grb”, a megfelelő MD5-fájl neve „abc_987_123456.grb.md5” lesz. Az MD5 fájlok segítenek azonosítani, hogy a fogadott vagy letöltött fájlokat nem sérti meg vagy nem érinti rosszindulatú tartalom. Röviden, az MD5 fájlok garantálják a fájl teljességét.


## Hogyan lehet ellenőrizni az MD5 ellenőrző összeget?

Egyetlen fájl ellenőrizhető/ellenőrizhető az MD5 esetében az [md5sum](https://en.wikipedia.org/wiki/Md5sum) eszközzel az alábbiak szerint.

```
md5sum -c abc_987_123456.grb.md5
```

## Hivatkozások

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)


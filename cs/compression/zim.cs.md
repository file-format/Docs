{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru ZIM - soubor archivu OpenZIM",
  "description":"Další informace o formátu souboru ZIM a rozhraních API, která mohou vytvářet a otevírat soubory ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Co je soubor ZIM? ##

Soubory s příponou .zim jsou archivy vytvořené pro ukládání obsahu Wiki offline. Je považován za nejvhodnější otevřený formát souboru pro ukládání Wikipedie na USB. Ukládá obsah stránek v kompaktním formátu. Jeho název pochází z „Zeno IMproved“, což byl dřívější formát souboru Zeno. ZIM je spravován projektem [openZIM ](https://openzim.org/), který je sponzorován Wikimedia CH a podporován Wikimedia Foundation. Soubory ZIM lze otevřít pomocí aplikací, jako je Kiwix a ZIMReader. Projekt OpenZIM hostil implementaci formátu souboru ZIM na [Github](https://github.com/openzim) za přispění komunity OpenSource.

## Specifikace formátu souboru ZIM

Formát souboru ZIM byl vyvinut nad [formát souboru Zeno](https://openzim.org/wiki/Zeno_file_format) a není zpětně kompatibilní. Specifikace formátu souboru ZIM jsou [dostupné online](https://openzim.org/wiki/ZIM_file_format) od openZIM pro vývojáře. OpenZIM poskytl C++ open source implementaci, [LibZim](https://openzim.org/wiki/Zimlib), pro čtení a zápis ZIM souborů.

Formát souboru ZIM používá kompresi LZMA2, aby byl obsah kompaktní.

{{< figure src="../ZIM_File_Format.jpeg" alt="Formát souboru ZIM" >}}


### Záhlaví ZIM

Soubor ZIM začíná záhlavím s offsetem 0. Všechny složky jsou založeny na little-endian a všechna celá čísla jsou celá čísla bez znaménka, tj. uint_16, uint_32, uint_64.

|Název pole |Typ| Offset| Délka| Popis|
---|---|---|---|---|
|magicNumber| celé číslo| 0| 4| Magické číslo pro rozpoznání formátu souboru musí být 72173914 (0x44D495A)|
|hlavníVerze| celé číslo| 4| 2| Hlavní verze formátu souboru ZIM (5 nebo 6)|
|minorVerze| celé číslo| 6| 2| Menší verze formátu souboru ZIM|
|uuid| celé číslo| 8| 16| jedinečné ID tohoto souboru zim|
|počet článků| celé číslo| 24| 4| celkový počet článků|
|clusterCount| celé číslo| 28| 4| celkový počet shluků|
|urlPtrPos| celé číslo| 32| 8| pozice seznamu ukazatelů na adresář seřazené podle URL|
|titlePtrPos| celé číslo| 40| 8| pozice seznamu ukazatelů adresáře seřazeného podle Title|
|clusterPtrPos| celé číslo| 48| 8| pozice seznamu ukazatelů clusteru|
|mimeListPos| celé číslo| 56| 8| pozice seznamu MIME typů (také velikost záhlaví)|
|hlavní stránka| celé číslo| 64| 4| hlavní stránka nebo 0xffffffff, pokud není hlavní stránka|
|layoutPage| celé číslo| 68| 4| rozvržení stránky nebo 0xffffffffff, pokud není žádná stránka rozvržení|
|kontrolní součetPos| celé číslo| 72| 8| ukazatel na md5checksum tohoto souboru bez samotného kontrolního součtu. Toto ukazuje vždy 16 bajtů před koncem souboru.|

## Reference ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)


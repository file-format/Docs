{
  "date" : "2021-02-15",
  "keywords" :[ "soubor vp6", "formát souboru vp6", "co je soubor vp6", "soubor", "příklad vp6", "přípona souboru vp6", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - TrueMotion Video File",
  "description":"Další informace o formátu souboru VP6 a rozhraních API, která mohou vytvářet a otevírat soubory VP6.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Co je soubor VP6?

VP6 je video formát se ztrátovou kompresí, který byl představen technologií On2 v květnu 2003. Je součástí řady video kodeků vyvinutých společností TrueMotion včetně V3, V4 a V5. Formát byl krátce použit v oblasti vysílání, jako jsou zprávy BBC a software QuickLink. VP6 byl následován kodekem VP7 v lednu 2005 s lepší kompatibilitou komprese.

## Formát souboru VP6

Kompletní specifikace souborů V6 nejsou veřejně dostupné. On2 specifikace původně zveřejnil, ale brzy se staly nedostupnými pro běžné uživatele. Neoficiální dokumentace formátu souboru VP6 je dostupná na [multimediální wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6), na kterou lze odkazovat vývojáře.

### Makrobloky (MB)

Podobně jako u MPEG-2, MPEG-4 části 2 a 10 se každý snímek videa souboru VP6 skládá z pole 16x16 makrobloků (MB). Každý MB může být v jednom z následujících režimů:

* Vnitřní MB
* Inter MB, null MV, předchozí referenční snímek
* Inter MB, diferenciál MV, předchozí referenční snímek
* Inter MB, čtyři MV, předchozí referenční snímek
* Inter MB, MV 1, předchozí referenční snímek
* Inter MB, MV 2, předchozí referenční snímek
* Inter MB, null MV, označený odkaz na snímek
* Inter MB, diferenciální MV, označený referenční rámeček
* Inter MB, MV 1, označený odkaz na rámeček
* Inter MB, MV 2, označený odkaz na rámeček

### Záhlaví rámečku

Záhlaví rámce VP6 je znázorněno níže, které následuje po pakování bitů big-endian.

|Syntaxe|Počet bitů|Typ|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 znamená intra frame|
|qp |6 |Nepodepsáno |Platný rozsah kvantizačního parametru 0..63|
|značka| 1| Konstantní| 0=VP61/62, 1=VP60|
|if (režim_snímku == 0) { | 0 | |rovná se INTRA_FRAME|
|verze |5| Konstantní| 6=VP60/61, 7=VP60(Electronic Arts), 8=VP62|
|verze2 |2| Konstanta |0=VP60, 3=VP61/62|
|prokládat |1| Boolean |pravda (1) znamená, že bude použito prokládání|
|if (značka==1 nebo verze2==0) {||||
|offset |16 |Nesignováno| offset sekundární vyrovnávací paměti (byty vzhledem k začátku vyrovnávací paměti)|
|}||||
|dim_y |8| Nesignováno| Výška makrobloku videa|
|dim_x |8| Nesignováno| Šířka makrobloku videa|
|render_y |8 |Nepodepsáno |Výška zobrazení videa|
|render_x |8 |Nepodepsáno |Zobrazená šířka videa|
|}jinak{||||
|if (značka==1 nebo verze2==0) {||||
|offset |16 |Nesigned |Offset sekundární vyrovnávací paměti (byty související se začátkem vyrovnávací paměti)|
|}||||
|}||||

## Reference

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)


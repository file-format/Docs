{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru OSR a rozhraních API, která mohou vytvářet a otevírat soubory OSR.",
  "title" :"OSR File - osu! Replay File Format",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Co je soubor OSR?

Soubor OSR je soubor pro přehrávání hry vytvořený souborem [osu! hra](https://osu.ppy.sh/home). Osu! je rytmická hra, kde uživatelé spojují kliknutí myší s hudbou. Do souboru OSR se zaznamenává skladba přehrávaná uživatelem, hity a shody, čas a datum přehrané skladby a celkové pořadí. Tento soubor OSR lze poté sdílet s ostatními pro účely přehrávání. Soubor OSR vyžaduje, aby byl soubor beatmap přítomen ve složce "Songs".

**MIME Typ souboru OSR Formát:** x-osu-replay

## Formát souboru OSR

Soubory OSR se ukládají jako binární soubory s datovými poli s pevnou i proměnnou délkou.

|Typ dat| Formát|
---|---|
|Byte |Herní režim přehrávání (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Integer |Verze hry, kdy byla vytvořena replay (např. 20131216)|
|Řetězec |osu! beatmap MD5 hash|
|Řetězec| Jméno hráče|
|Řetězec| osu! replay MD5 hash (zahrnuje určité vlastnosti přehrávání)|
|Krátké| Počet 300s|
|Krátké| Počet 100 ve standardu, 150 v Taiko, 100 v CTB, 100 v mánii|
|Krátké| Počet 50s ve standardu, drobné ovoce v CTB, 50s v mánii|
|Krátké| Počet Geki ve standardu, Max 300s v mánii|
|Krátké| Počet Katus ve standardu, 200s v mánii|
|Krátké| Počet chyb|
|Celé číslo| Celkové skóre zobrazené ve zprávě o skóre|
|Krátké| Největší kombinace zobrazená ve skóre reportu|
|Byte| Perfektní/úplné kombo (1 = žádné vynechání a žádné přerušení posuvníku a žádné předčasně dokončené posuvníky)|
|Celé číslo| Použité mody. Seznam hodnot modů naleznete níže.|
|Řetězec| Sloupcový graf života: čárkami oddělené páry u/v, kde u je čas v milisekundách do skladby a v je hodnota s plovoucí desetinnou čárkou od 0 do 1, která představuje množství života, které máte v daném čase (0 = sloupec života je prázdný, 1= životnost je plná)|
|Dlouhé| Časové razítko (tikání Windows)|
|Celé číslo| Délka komprimovaných dat přehrávání v bajtech|
|Byte |Pole komprimovaná data přehrávání|
|Dlouhé| Online skóre ID|
|Dvojité| Další informace o modu. Přítomno pouze v případě, že je povolena Target Practice.|

## Reference

* [OSU! Rytmická hra](https://osu.ppy.sh/home)
* [Formát souboru OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


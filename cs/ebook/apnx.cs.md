{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon Page Number Index", "rozšíření", "soubor", "formát", "eKniha", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů Amazon APNX a rozhraních API, která mohou vytvářet a otevírat soubory APNX.",
  "title" :"APNX - Amazon Page Number Index",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Co je soubor APNX? ##

Soubor Amazon Page Number Index, který používá příponu .apnx, je typ souboru eBook; používá Amazon Kindle. Tyto soubory jsou ve skutečnosti známé jako stránkovací soubory používané zařízeními Kindle. Soubory APNX se tedy obvykle vytvářejí k označení stránek elektronických knih Kindle. Funkce stránkování byla spuštěna na zařízeních Amazon Kindle od jejich firmwaru 3.1. Hledá v souboru APNX indexy stránek a poté je mapuje s čísly stránek v původní tiskové knize. Tyto soubory se ukládají do zařízení Kindle spolu se soubory Amazon eBooks. Soubory APNX nelze otevřít ani upravit.

## Specifikace formátu souboru APNX ##

### Rozvržení

|bytes| obsah| komentáře|
---|---|---|
|4 |00010001 | Identifikátor formátu. Hodnota 65537 little-endian.|
|4 |začátek příštího | Posun po ukončení umístění prvního záhlaví. Spustí novou sekvenci záhlaví info|
|4 |délka| Délka prvního záhlaví|
|N |první záhlaví | Řetězec obsahující hlavičku obsahu. Začíná další sekvence|
|2 |neznámý | Vždy 1|
|2 |délka | Délka druhého záhlaví|
|2 |počet stránek | Celkový počet bajtů po druhém záhlaví, které představují stránky. Tento součet zahrnuje bajty, které pageMap ignoruje.|
|2 |neznámý | Vždy 32|
|N |druhé záhlaví | Řetězec obsahující hlavičku mapování stránky|
|4*N |vycpávka | První číslo uvedené v záhlaví mapování stránky označuje počet 0 bajtů.|
|4*N |seznam stránek ||

### Záhlaví obsahu

Záhlaví obsahu se skládá z řetězce uzavřeného v {}, který obsahuje páry klíč, hodnota:

|obsah| komentáře|
---|---|
|contentGuid| Průvodce.|
|asin | Identifikátor Amazon pro verzi knihy Kindle.|
|cdeType | MOBI cdeType. U e-knih by měl být vždy EBOK.|
|fileRevisionId | Revize tohoto souboru.|

#### Příklad
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Záhlaví mapování stránky
Záhlaví mapování stránky se skládá z řetězce uzavřeného v {}, který obsahuje páry klíč, hodnota.

|obsah | komentáře|
---|---|
|asin | ISBN 10 pro papírovou knihu, které stránky odpovídají|
|Mapa stránky| Trojhodnotová n-tice. Vypadá takto: "(N,N,N)\
1) Počet bajtů po záhlaví, které začíná sekvenci číslování stránek\
2) neznámé\
3) neznámý\|
#### Příklad
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Seznam stránek

Seznam stránek je posloupnost posunů v nezpracovaném HTML. Každý
hodnota je začátek nové stránky. Každý záznam je 4bajtový big endian
int.



## Reference

* [Formát souboru Amazon APNX](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX – od MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)


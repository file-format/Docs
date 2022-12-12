{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Formát souboru", "Otevřít", "Číst", "Vytvořit", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů HPGL a rozhraních API, která mohou vytvářet a otevírat soubory HPGL.",
  "title" :"Formát souborů HPGL - učte se od odborníků na formát souborů!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Co je soubor HPGL?

Soubor HPGFL (Hewlett-Packard Graphics Language) obsahuje sadu instrukcí pro ovládání plotru vyvinutou společností HP. Plotry HP používají tento soubor ke kreslení a tisku vektorového a rastrového obsahu na papír.

### Příkaz HPGL

Příkaz HPGL se skládá z následujících.
* Příkazová část abecedy se dvěma znaky
* Sekce parametrů
* Sekce Terminátor

V případě více parametrů musí být každý parametr v souboru oddělen oddělovačem.

### Příklad příkazu HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Souřadnicový systém

Souřadnicové systémy se skládají z 2-rozměrných indikátorů měření pro lokalizaci jakéhokoli konkrétního místa. HPGL pro tento účel používá jak souřadnicový systém Plotter, tak uživatelský souřadnicový systém.

#### Souřadnicový systém plotru

Tento souřadnicový systém se používá k vykreslování výkresů na základě pohybu plotru. Typická jednotka XY minimálního pohybu plotru je 0,025 mm. Možný rozsah změn výkresu s druhy plotrů.

#### Uživatelský souřadnicový systém

Uživatelem zadaný souřadnicový systém lze nastavit pomocí měřítka a počátku. Tyto jsou převedeny na souřadnice plotru pomocí příkazu IP a příkazu SC. Souřadnice systému plotru jsou standardně použity, pokud se tento převod neprovádí.

## Formát souboru HPGL
Soubory HPGL jsou ve formátu ASCII (textový soubor) a začínají několika instalačními příkazy. Tím se nastaví určité parametry plotru pro vykreslování. Typický soubor HPGL vypadá následovně.

|Příkaz|Význam
---|---|
|IN;|inicializovat, spustit vykreslovací úlohu|
|IP;|nastaví body měřítka (P1 a P2) do jejich výchozích pozic|
|SP1;|vyberte pero 1|
|PU0,0;|zvedněte pero nahoru a přesuňte se na výchozí bod pro další akci|
|PD100,0,100,100,0,100,0,0;|položte pero dolů a přesuňte se na následující místa (nakreslete rámeček kolem stránky)|
|PU50,50;|Per Up a přesun na souřadnice X,Y 50,50|
|CI25;|nakreslete kružnici o poloměru 25|
|SS;|vyberte standardní znakovou sadu|
|DT*,1;|nastavit oddělovač textu na hvězdičku a netisknout je (1, což znamená "pravda")|
|PU20,80;|zvedněte pero a přesuňte se na 20,80|
|LBHello World*;|nakreslit štítek|

## Reference
* [HPGL by Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [Referenční příručka HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)


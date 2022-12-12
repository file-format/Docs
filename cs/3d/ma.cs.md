{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma soubor", "formát souboru ma", "formát souboru", "3d", "stažení souboru ma", "soubor .ma", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů MA a rozhraních API, která mohou otevírat a vytvářet soubory MA.",
  "title" :"Formát souboru MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Co je soubor MA?

Soubor s příponou .ma je soubor 3D projektu vytvořený pomocí aplikace Autodesk Maya. Obsahuje velký seznam textových příkazů pro specifikaci informací o souboru. Soubor **.ma** lze otevřít a upravit v libovolném textovém editoru, aby se vyřešily případné problémy s příkazy v případě poškození souboru. Tyto soubory obsahují informace pro definování informací o 3D scéně, jako je geometrie, osvětlení, animace a vykreslování.

## Formát souboru MA

Soubory MA se ukládají na disk v textovém formátu ASCII, na rozdíl od souborů MB, které se ukládají na disk v binárním formátu. Podrobný odkaz na formát souboru MA je k dispozici v [Autodesk Maya Documentation] (https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) a lze jej použít pro vývojářskou referenci.

### Záhlaví souboru MA

Záhlaví souboru MA začíná sekcí komentářů, která poskytuje informace o vytvoření souboru a datum změny. Čtečky souborů Maya tento blok ignorují, protože se používá pouze pro informační účely. Záhlaví však musí začínat prvními šesti znaky jako „//Maya“.

Záhlaví souboru ASCII vypadá následovně.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Odkazy na soubory

Část s odkazy na soubory souboru .ma obsahuje informace o všech ostatních souborech Maya, na které se v tomto souboru odkazuje. Každý odkazovaný soubor lze číst pomocí jediného příkazu souboru, který je obsažen ve stejném souboru. Syntaxe příkazu file při použití pro odkazování je:

```
file -r -rpr prefixString fileName;
```
nebo

```
file -r -ns nameSpace fileName
```
Zde je příklad řetězce.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Tento příklad ukazuje, že objekt sun obsažený v souboru `solar` by byl v tomto souboru přístupný pod názvem "solar_sun".

### Požadavky

Sekce požadavků souboru .ma se skládá ze série požadovaných příkazů a sděluje Mayovi informace, jako je verze a informace o zásuvných modulech, které jsou nutné ke čtení souborů. Příklad sekce požadavků je následující.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Další část specifikuje požadavky. Skládá se z řady požadovaných příkazů. Tato část souboru říká Maye, jaký software je potřeba ke správnému načtení souboru. Konkrétně, jakou verzi Maya a jaké plug-iny.

## Stáhnout soubor MA
Je trochu těžké najít a stáhnout MA soubor 3D modelu. Vzorový soubor MA si proto můžete stáhnout zde:

- [Ukázka.ma](../vzor.ma)


## Reference

* [Organizace souborů Maya ASCII – Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)


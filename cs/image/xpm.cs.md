{
  "date" : "2019-10-11",
  "keywords" :[ "soubor xpm", "formát souboru xpm", "co je soubor xpm", "soubor", "příklad xpm", "přípona souboru xpm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap File Format",
  "description":"Další informace o formátu souboru XPM a rozhraních API, která mohou vytvářet a otevírat soubory XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor XPM?

Soubor s příponou .xpm je formát souboru obrázku, který byl používán systémem X Windows. Podporuje průhledné pixely a obvykle se zaměřuje na vytváření pixmap ikon. Podporuje monochromatická, gra-scale a barevná data pixmap. Ty byly navrženy tak, aby je bylo možné upravovat ručně a lze je zahrnout do kódu [C](/cs/programming/c/). Pro tento účel jsou soubory XPM ve formátu prostého textového souboru a řídí se syntaxí programovacího jazyka C. Soubory XPM lze otevřít pomocí různých aplikací pro prohlížení obrázků, jako je např
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView a Canvas X.

## Formát souboru XPM

Formát souboru XPM používá syntaxi C, aby mohly být integrovány do programů C a C++. Skládá se z následujících šesti různých částí.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Sekce jsou ve skutečnosti polem řetězců následovně.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Níže jsou uvedeny podrobnosti o každé sekci.

`<Values> ` - Tato sekce je řetězec, který obsahuje čtyři nebo šest celých čísel, která jsou v základu 10 a odpovídají:

* šířka a výška pixmapy
* počet barev
* počet znaků na pixel
* volitelné souřadnice aktivního bodu a značka XPMEXT

`<Colors> ` - Tato sekce obsahuje tolik řetězců, kolik je barev. Každý řetězec je následující:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Tato sekce se skládá z<height> struny a<width> \*<chars_per_pixel> znaky. Každý<chars_per_pixel> řetězec délky by měl být jednou z dříve definovaných skupin v<Colors> sekce.

`<Extension> ` - Sekce rozšíření musí být označena, pokud není prázdná, v<Values> sekce. Může se skládat z několika<Extension> pododdíly, které mohou být následujících dvou typů:

* jeden samostatný řetězec složený následovně: XPMEXT<extension-name><extension-data>
* nebo blok složený z několika řetězců:XPMEXT<extension-name><related extension-data composed of several strings>

## Reference

* [XPM – Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM Manual] (http://www.xfree86.org/current/xpm.pdf)


{
  "date" : "2020-01-10",
  "keywords" :[ "soubor otg", "formát souboru otg", "co je soubor otg", "soubor", "příklad otg", "přípona souboru otg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - Formát souboru šablony výkresu OpenDocument",
  "description":"Další informace o formátu souboru OTG a rozhraních API, která mohou vytvářet a otevírat soubory OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Co je soubor OTG?

Soubor OTG je šablona výkresu, která je vytvořena pomocí standardu OpenDocument, který se řídí specifikací OASIS Office Applications [1.0](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Představuje výchozí organizaci prvků výkresu pro vektorový obrázek, který lze použít k dalšímu vylepšení obsahu souboru. Soubory OTF jsou jako jakékoli jiné soubory založené na formátu OpenDocument, které jsou založeny na formátu XML a představují obsah dokumentu. Soubory OTF lze zobrazit otevřením v libovolném textovém nebo standardním editoru XML.

## Specifikace formátu souboru OTG ##

Formát souboru OTG je založen na formátu OpenDocument XML, který má dobře zavedené schéma. Struktura každé součásti formátu OpenDocument je reprezentována prvkem, který má přidružené atributy a je společný pro všechny typy dokumentů, jako je textový dokument, tabulkový procesor nebo soubor výkresu. OTG, což je šablona výkresu, široce využívá specifikace grafického obsahu, které zahrnují:

* Vylepšené funkce stránky pro grafické aplikace
* Kreslení tvarů
* Rámy
* 3D tvary
* Vlastní tvar
* Tvary prezentace
* Prezentační animace
* Animace prezentace SMIL
* Prezentační akce
* Přítomná textová pole
* Obsah prezentačního dokumentu

### Vylepšené funkce stránky pro grafické aplikace ###
#### Mistr podkladů ####

Element Handout Master je šablona pro automatické generování stránek s podklady pro aplikace, které podporují tisk takových stránek.
Atributy, které mohou být spojeny s `<style:handout-master>` prvek jsou:

|Rozvržení|Atribut|Popis
---|---|---|
|Rozvržení stránky prezentace|prezentace:název-rozložení-prezentace|Odkazy na `<style:presentation-page-layout>`  atribut
|Rozvržení stránky|`style:page-layout-name` | Určuje rozvržení stránky, které obsahuje velikosti, ohraničení a orientaci vzorové stránky podkladů.
|Styl stránky|`draw:style-name`|Přiřadí další atributy formátování hlavní stránce podkladu přiřazením stylu stránky výkresu.|
|Prohlášení v záhlaví| `presentation:use-header-name`| Určuje název deklarace pole záhlaví, která se používá pro všechna pole záhlaví, která jsou zobrazena na vzorové stránce podkladů.
|Prohlášení v zápatí| presentation:use-footer-name|Uvádí název deklarace pole zápatí, která se používá pro všechna pole zápatí, která jsou zobrazena na vzorové stránce podkladů.
|Deklarace data a času|use-date-time-name|Uvádí název deklarace pole datum-čas, která se používá pro všechna pole data a času, která jsou zobrazena na hlavní stránce podkladů.

### Kreslení tvarů ###
Formát OpenDocument podporuje několik tvarů výkresu, které lze použít pro jakýkoli typ dokumentu.

|Tvar|Přidružené atributy| Prvky
---|---|---|
Obdélník - `<draw:rect>` |Pozice, Velikost, Styl, Vrstva, Z-Index, ID, ID titulku, Ukotvení textu, pozadí tabulky, koncová pozice kreslení, Zaoblené rohy|Název, Dlouhý popis, Posluchači událostí, Lepicí body, Text
Řádek `<draw:line>` |Styl, Vrstva, Z-Index, ID, ID titulku a transformace, Ukotvení textu, pozadí tabulky, koncová pozice kreslení, Počáteční bod, Koncový bod|Název, Dlouhý popis, Posluchači událostí, Lepicí body, Text
Polyline `<draw:polyline>` | Pozice, Velikost, Pole zobrazení, Styl, Vrstva, Z-Index, ID, ID titulku a transformace, Kotva textu, pozadí tabulky, koncová pozice kreslení, Body| Název, dlouhý popis, posluchači událostí, lepicí body, text
Mnohoúhelník "draw:polygon `|Pozice, Velikost, Pole zobrazení, Styl, Vrstva, Z-Index, ID, ID a transformace titulku, Ukotvení textu, pozadí tabulky, koncová pozice kreslení, Body|Název, Dlouhý popis, Posluchači událostí, Lepicí body, Text
|Pravidelný mnohoúhelník `<draw:regular-polygon> `|Pozice, Velikost, Styl, Vrstva, Z-Index, ID, ID a transformace titulku, Ukotvení textu, pozadí tabulky, koncová pozice kreslení, Konkávní, Rohy, Ostrost|Název, Dlouhý popis, Posluchače událostí, Lepicí body, Text
|Cesta `<draw:path> `|Pozice, Velikost, Pole zobrazení, Styl, Vrstva, Z-Index, ID, ID titulku a transformace, Kotva textu, pozadí tabulky, koncová pozice kreslení, Data cesty| Název, dlouhý popis, posluchači událostí, lepicí body, text

### Rámečky ###
Rámeček v dokumentu výkresu je obdélníkový kontejner, který obsahuje textová pole, obrázky nebo objekty. Rámečky podporují další funkce, jako jsou obrysy, obrazové mapy a hypertextové odkazy. Rámeček může obsahovat objekt i obrázek, což umožňuje vícenásobné ztvárnění objektu. Aplikace vykreslují příslušný prvek na základě nejlepší podpory.

Rámy mohou obsahovat:
* Textová pole
* Objekty reprezentované buď ve formátu OpenDocument nebo v binárním formátu specifickém pro objekt
* Snímky
* Applety
* Zásuvné moduly
* Plovoucí rámy

Rámeček je obsažen v dokumentu, jak je znázorněno níže.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Reference ##
* [Formát otevřených dokumentů OASIS pro aplikace Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formát OpenDocument – Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)


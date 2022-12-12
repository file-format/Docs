{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "soubor", "formát souboru", "Jazyk popisu stránky", "Skalární" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru SVG a rozhraních API, která mohou vytvářet a otevírat soubory SVG.",
  "title" :"Co je soubor SVG?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Co je soubor SVG? ##

Soubor SVG je soubor skalární vektorové grafiky, který k popisu vzhledu obrázku používá textový formát založený na XML. Slovo Scalable odkazuje na skutečnost, že SVG lze škálovat na různé velikosti bez ztráty kvality. Textový popis těchto souborů je činí nezávislými na rozlišení. Je to jeden z nejpoužívanějších formátů pro tvorbu webových stránek a tiskové grafiky za účelem dosažení škálovatelnosti. Formát lze použít pouze pro dvourozměrnou grafiku. Soubory SVG lze prohlížet/otvírat téměř ve všech moderních prohlížečích včetně Chrome, Internet Explorer, Firefox a Safari.

## Stručná historie ##

Specifikace SVG jsou k dispozici jako otevřený standard konsorciem World Wide Web Consortium (W3C) od roku 1999. Předtím byly W3C do roku 1998 předkládány podobné specifikace formátu souborů v šesti různých formátech. V roce 2011 byla provedena aktualizace specifikací a jejich verze byla 1.1 . V roce 2016 bylo SVG 2 publikováno jako novější verze obsahující funkce navíc k těm v SVG 1.1.

## Specifikace formátu souboru ##

SVG Document Object Model (DOM) pokládá základy pro všechny specifikace a rozhraní, která odpovídají konkrétním částem specifikací. Prohlížeče SVG musí implementovat rozhraní SVG DOM, jak je definováno ve specifikacích W3C. Jeho DOM zpřístupňuje několik rozhraní pro různé datové typy a prvky.

### Tvary SVG ###

SVG má některé předdefinované prvky tvaru, které mohou vývojáři použít:

* Obdélník<rect>
* Kruh<circle>
*Elipsa<ellipse>
* Linka<line>
* Polyline<polyline>
* Mnohoúhelník<polygon>
* Cesta<path>

Na základě těchto tvarů a specifikací jsou funkční oblasti SVG následující.

**Cesty** – Cesty se používají k reprezentaci jednoduchých i složených obrysů tvarů. Kódování se používá k definování povahy operace. Například M se používá pro Přesunout do, L se používá pro Line To, Z se používá k uzavření cesty a tak dále.

**Základní tvary** – Lze kreslit přímkové cesty a cesty tvořené řadou spojených přímých segmentů (křivek) a také uzavřené mnohoúhelníky, kružnice a elipsy. Standardními prvky jsou také obdélníky a obdélníky se zaoblenými rohy.

**Text** – Reprezentace textu je vyjádřena jako znaková data XML, kde lze na text použít mnoho vizuálních efektů. Specifikace umožňují pracovat s obousměrným textem, svislým textem a znaky podél zakřivené cesty.

**Malba** - Tvary lze vyplnit a/nebo ohraničit barvou, přechodem nebo vzorem, což umožňuje, aby byly neprůhledné nebo aby měly jakýkoli stupeň průhlednosti. Prvky na konci čar, jako jsou šipky nebo symboly objevující se ve vrcholech mnohoúhelníku, jsou reprezentovány značkami.

**Barva** – Specifikace SVG umožňují aplikovat barvy na všechny viditelné prvky SVG, buď přímo, nebo prostřednictvím výplně, tahu a dalších vlastností. Pro specifikaci lze použít různá barevná kódování, jako je černá nebo modrá, hexadecimální reprezentace, desítkové nebo jako procenta formy RGB.

**Přechody a vzory** – Tvary v souboru SVG lze vyplnit nebo ohraničit plnými barvami, přechody nebo opakujícími se vzory.

**Efekty filtru** – Ve skutečnosti jde o sérii grafických operací, které se aplikují na danou zdrojovou vektorovou grafiku, aby vytvořily upravený výsledek.

**Interaktivita** – Uživatelé mohou pracovat se soubory SVG změnou zaměření, kliknutím myši, posouváním nebo přibližováním obrázku. Interaktivita umožňuje obrázkům SVG komunikovat s uživateli mnoha různými způsoby, jak bylo uvedeno výše.

**Propojení** – Je možné, aby obrázky SVG měly hypertextové odkazy na jiné dokumenty. Toho je dosaženo pomocí XML Linking Language nebo XLink. To umožňuje vytvářet specifické stavy pohledu, které se používají k přiblížení/oddálení konkrétní oblasti nebo k omezení pohledu na konkrétní prvek.

**Skriptování** – Podobně jako u HTML jsou všechny aspekty dokumentu SVG přístupné pro manipulaci pomocí skriptů. Objekty SVG DOM poskytují návod, jak toho dosáhnout pomocí prvku a atributu SVG. Skripty jsou uzavřeny v prvcích tagu `script` a mohou se podle potřeby spouštět v reakci na události ukazatele, klávesnice nebo dokumentu.

**Animace** – Prvky DOM<animate> ,<animateMotion> a<animateColor> umožňuje zahrnout animaci obsahu SVG. Toho samozřejmě nelze dosáhnout bez použití skriptů a vestavěných časovačů. Tyto animace mohou být nepřetržité a mohou být uvedeny ve smyčce i opakování a zároveň reagovat na události uživatele.

**Písma** – Text v SVG může odkazovat na externí soubory písem, jako jsou systémová písma. Při absenci takových písem nebude text ve formátu SVG vykreslen na výstup. To lze překonat začleněním požadovaných glyfů do takového souboru jako fontu, který je poté vykreslen pomocí<text> živel.

## Příklady ##
Následující řádky ukazují, jak je kruh reprezentován pomocí skriptu SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Následující řádky kódu ukazují, jak používat<text> blok pro vykreslení textu do SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Reference ##

* [Specifikace W3C SVG](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG – Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)


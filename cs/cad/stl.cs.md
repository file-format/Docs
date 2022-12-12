{
  "date" : "2020-03-16",
  "keywords" :[ "Soubor STL", "Formát", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů STL a rozhraních API, která mohou vytvářet a otevírat soubory STL.",
  "title" :"Formát souboru STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor STL?

STL, zkratka pro stereolitrografii, je zaměnitelný formát souboru, který představuje 3-rozměrnou povrchovou geometrii. Souborový formát nachází uplatnění v několika oblastech, jako je rychlé prototypování, 3D tisk a počítačově podporovaná výroba. Představuje plochu jako řadu malých trojúhelníků, známých jako fasety, kde každá faseta je popsána kolmým směrem a třemi body představujícími vrcholy trojúhelníku. Výsledná data používají aplikace k určení průřezu 3D tvaru, který má výrobce postavit. Ve formátu souboru STL nejsou k dispozici žádné informace pro reprezentaci barvy, textury nebo jiných běžných [CAD](/cs/cad/) atributů modelu.

## Stručná historie ##

Vývoj formátu souborů STL se datuje od roku 1987. Byl vyvinut společností 3D Systems pro jeho použití v komerčních 3D tiskárnách. Revidovaná verze formátu souboru STL, známá jako STL 2.0, byla navržena v roce 2009 s aktualizacemi formátu souboru.

## Specifikace formátu souboru ##

Soubor STL představuje geometrii povrchu pomocí faset. Plochy definují povrch 3D objektu a jsou jednoznačně identifikovány jednotkovou normálou, což je čára kolmá k trojúhelníku o délce 1,0, a třemi vrcholy. Pro každou fasetu je uloženo celkem 12 čísel jako Normální a každý vrchol je specifikován třemi souřadnicemi. Soubor StL neobsahuje žádné informace o měřítku; souřadnice jsou v libovolných jednotkách.

Specifikace formátu souboru STL lze zkoumat z následujících dvou hledisek.

### Orientace faset ###

Orientace fasety je určena směrem normály jednotky a pořadím, ve kterém jsou uvedeny vrcholy. Orientace faset je určena dvěma způsoby takto:

* Směr normály je ven
* Vrcholy jsou uvedeny zvenčí ve směru proti směru hodinových ručiček, přičemž se řídí pravidlem pravé ruky.

### Pravidlo Vertex to Vertex ###

Podle tohoto pravidla sdílí každý trojúhelník dva vrcholy s každým ze sousedních trojúhelníků. Vrchol jednoho trojúhelníku tedy nemůže ležet na straně jiného trojúhelníku.

## Formáty souborů ##

STL je k dispozici v ASCII i v binárních reprezentacích pro kompaktní formát souborů.

### Formát STL ASCII ###

Verze ASCII formátu souboru STL je zapsána v prostém ASCII. Vzhledem k velké velikosti však není formát souboru vybrán jako preferovaný formát pro použití. Syntaxe souboru ASCII STL je následující:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Slova s tučným písmem představují klíčová slova, která by měla být vždy malá. Symboly psané kurzívou jsou proměnné, které mají být nahrazeny uživatelem zadanými hodnotami. Číselná data v řádcích **normální fasety** a **vrchol** jsou s plovoucí jednoduchou přesností, například 1,23456E+789. **normální** souřadnice může mít úvodní znaménko mínus; **vertex** souřadnice nemusí.

### Binární formát STL ###

Binární formát používá IEEE celé číslo a číselnou reprezentaci s plovoucí desetinnou čárkou. Formát souboru je reprezentován následovně:

|Pole|Informace|
---|---|
|Záhlaví|80 znaků|
|Počet trojúhelníků|4bajtové malé endian celé číslo bez znaménka|
|Data pro každý trojúhelník|12 32bitových čísel s plovoucí desetinnou čárkou|

Propracovanější pohled na formát souboru je uveden níže.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Reference ##

* [Formát STL](http://www.fabbers.com/tech/STL_Format)
* [STL – podle Wikipedie](https://en.wikipedia.org/wiki/STL_(formát_souboru))


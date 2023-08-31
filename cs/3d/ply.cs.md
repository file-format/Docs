{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "soubor", "přípona", "formát", "formát 3D souboru" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru PLY a rozhraních API, která mohou vytvářet a otevírat soubory PLY.",
  "title" :"PLY - Polygon 3D File Format",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PLY?

PLY, Polygon File Format, představuje 3D formát souboru, který ukládá grafické objekty popsané jako kolekce polygonů. Účelem tohoto formátu souboru bylo vytvořit jednoduchý a snadný typ souboru, který je dostatečně obecný, aby byl užitečný pro širokou škálu modelů. Formát souboru PLY je dodáván jako ASCII i binární formát pro kompaktní úložiště a pro rychlé ukládání a načítání. Formát souboru používají různé aplikace, které poskytují podporu pro čtení 3D souborů.

Objekty ve formátu PLY jsou popsány kolekcí vrcholů, ploch a dalších prvků spolu s vlastnostmi, jako je barva a normální směr, které lze k těmto prvkům připojit. Mezi další vlastnosti, které lze také uložit s objektem, patří:

* Normály povrchu
* souřadnice textury
* průhlednost
* spolehlivost údajů o rozsahu
* vlastnosti pro přední a zadní stranu mnohoúhelníku

Objekt reprezentovaný formátem PLY může být výsledkem různých zdrojů, jako jsou ručně digitalizované objekty, polygonové objekty z modelovacích aplikací, data vzdálenosti, trojúhelníky z pochodových krychlí, data terénu a modely radiozity.

## Stručná historie

Formát PLY byl vyvinut v 90. letech 20. století Gregem Turkem a dalšími ve Stanfordské grafické laboratoři, a proto je také známý jako formát Stanford Triangle Format. Formát souboru má od té doby verzi 1.0 a nebyly provedeny žádné další úpravy.

## Formát souboru PLY

Jednoduchý objekt PLY se skládá z kolekce prvků pro reprezentaci objektu. Skládá se ze seznamu (x,y,z) trojic vrcholů a seznamu ploch, které jsou vlastně indexy do seznamu vrcholů. Vrcholy a plochy jsou dva příklady prvků a většina souboru PLY se skládá z těchto dvou prvků. Nové vlastnosti mohou být také vytvořeny a připojeny k prvkům objektu, ale ty by měly být přidány takovým způsobem, aby se staré programy nezlomily, když narazí na tyto nové vlastnosti. Takové vlastnosti mohou být zahozeny i aplikacemi pro čtení. Navíc lze pomocí tohoto prvku vytvářet nové prvky a definovat vlastnosti.

### Struktura souboru

Struktura souboru formátu PLY je následující:

|Pole
---|
|Záhlaví souboru
|Seznam vrcholů
|Seznam tváří
|Seznam dalších prvků

#### Příklad struktury

Následující příklad níže použijeme v naší následné diskusi pro různé části formátu souboru PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Záhlaví souboru

Hlavička formátu souboru PLY se skládá z textu ASCII pro ASCII i binární formát. Začátek a konec sekce záhlaví je identifikován klíčovými slovy vrstva a konec záhlaví. Na začátku hlavičky je kouzelné slovo ply, které se používá pro rozpoznání formátu souboru PLY čtenáři. Na dalším řádku je uvedeno číslo verze tohoto souboru. Komentáře ve formátu souboru PLY začínají klíčovým slovem komentář na začátku každého řádku komentáře.

#### Klíčové slovo prvku

Klíčové slovo element pak říká, co je uvnitř souboru. Za ní následují vlastnosti pro tento konkrétní typ prvku, kde každá vlastnost má svůj typ vlastnosti a pořadí, jak je uvedeno níže:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

V tomto konkrétním příkladu má konkrétní vertexový prvek 3 vlastnosti typu float se zadaným pořadím.

#### Typy datových typů

Vlastnost může mít dva typy datových typů.

`Skalární`: Skalární datové typy jsou uvedeny níže:

|#Jméno|#Typ|#Počet bajtů
|znak|postava|1
|uchar|nepodepsaný znak|1
|krátké|krátké celé číslo|2
|ushort|krátké celé číslo bez znaménka|2
|int|Celé číslo|4
|uint|celé číslo bez znaménka|4
|plovák|plovák s jednoduchou přesností|4
|dvojitý|plovák s dvojitou přesností|8

`Seznam`: Existuje speciální forma definic vlastností, která používá datový typ seznamu. Příklad je ze souboru krychle výše:

`seznam vlastností uchar int vertex_index`

To znamená, že vlastnost "vertex_index" obsahuje nejprve znak bez znaménka, který říká, kolik indexů vlastnost obsahuje, následovaný seznamem obsahujícím tolik celých čísel. Každé celé číslo v tomto seznamu s proměnnou délkou je indexem k vrcholu.

## Reference ##

* [Formát souboru PLY](http://paulbourke.net/dataformats/ply/)
* [PLY – z Wikipedie](https://en.wikipedia.org/wiki/PLY_(file_format))


{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","soubor", "formát", "typ souboru", "přípona","co je soubor ASE?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru ASE a rozhraních API, která mohou otevírat a vytvářet soubory ASE.",
  "title" :"ASE - Autodesk ASCII Scene Export File",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Co je soubor ASE?

Soubor s příponou .ase je formát souboru Autodesk ASCII Scene Export, který představuje ASCII reprezentaci scény a obsahuje 2D nebo 3D informace při exportu dat scény pomocí Autodesku. Autodesk nabízí možnosti pro zahrnutí komponent scény při exportu dat scény. Můžete zahrnout definici sítě spolu s informacemi o vrcholu a ploše, popis materiálu, transformační data animace pro objekty, úplnou definici sítě pro každých n snímků, data animace pro kamery a světla a nastavení spojů IK.

## Formát souboru ASE – Další informace

Soubory ASE jsou textové soubory uložené ve formátu ASCII, které lze otevřít v libovolném textovém editoru. Soubor ASE může obsahovat následující typy informací poskytovaných společností Autodesk.

### Možnosti výstupu

* `Definice sítě` - Exportuje definici každé sítě, včetně informací o vrcholech a plochách pro geometrické objekty. Zapnutím této možnosti navíc povolíte položky ve skupinovém poli Možnosti sítě, popsané níže.
* `Materiály` - Obsahuje popis materiálu. Pokud není k objektu přiřazen materiál, exportuje se jeho barva drátěného modelu. Jsou zahrnuty všechny úrovně materiálového stromu, takže to může produkovat velké množství textu.
* „Klíče animace transformace“ – Zahrnuje data animace transformace pro objekty. Pokud je objekt cílovou kamerou nebo reflektorem, bude to zahrnovat data animace cíle.
* `Animated Mesh` - Exportuje kompletní definici sítě pro každých n snímků. Frekvence je specifikována ovladačem výstupu ovladače, který je popsán níže. Každý blok obsahuje stejné informace zadané ve skupinovém poli Možnosti sítě, popsané níže. Zapnutím tohoto nastavení můžete vytvořit velký soubor, a to i pro malé scény.
* `Nastavení animované kamery/světla` - Exportuje data animací pro kamery a světla, jako je barva, intenzita, pokles, zkreslení mapy a tak dále. Výstup bloku každých n snímků, jak je určeno číselníkem výstupu ovladače.
* `Inverzní kinematické spoje` - Exportuje nastavení spoje IK ve větvi Hierarchy.

### Typy objektů

Položky zde umožňují určit, jakou kategorii objektu chcete zahrnout do výstupu. Můžete zahrnout geometrické objekty, tvary, kamery, světla a pomocné objekty.

* Geometrické
* Tvary
* Fotoaparáty
* Světla
* Pomocníci

### Možnosti sítě

* `Normály sítě` - Exportuje normály obličeje a vrcholu. Jako první je uvedena normála obličeje, následovaná normálami tří vrcholů podpírajících obličej. Zapnutím této možnosti získáte mnohem větší soubor.
* `Mapping Coordinates` - Exportuje seznam mapovacích vrcholů a ploch podle struktur TVert a TVFace popsaných v 3ds Max Software Development Kit. Pokud objekt používá mapování obličejů, exportuje se seznam map obličejů obsahující souřadnice UVW pro každý obličej.
* `Barvy vrcholů` - Exportuje barvy vrcholů.

### Výstup ovladače

* `Použít klíče` – Exportuje hodnoty klíčů. Pokud ovladač nepoužívá klávesy, použije se metoda Force Sample. V případě transformačních regulátorů možnost Použít klíče funguje pouze tehdy, jsou-li všechny transformační regulátory buď Lineární/TCB nebo Bezier. Pokud jedna z transformačních stop používá jiný typ ovladače, pak se pro všechny transformační stopy použije metoda Force Sample.
* `Force Samples` - Vzorkuje hodnoty kontroleru na základě frekvence specifikované v Frames per Sample Controller.

## Reference

* [Autodesk – Export do ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)


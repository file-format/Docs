{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PDF/VT",
  "description":"Další informace o formátu souborů PDF/VT a rozhraních API, která mohou vytvářet a otevírat soubory PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Co je PDF/VT? #

PDF/VT, publikovaný jako [ISO 16612-2](https://www.iso.org/standard/46428.html) v srpnu 2010 jako standard, je navržen tak, aby umožňoval variabilní tisk dokumentů (VDP) v různých prostředí. Norma činí z variabilních informací a transakčního tisku základ normy. Tisk proměnných dat se používá tam, kde se část informací pro každého příjemce obsahu liší. Transakční tisk zahrnuje faktury, výpisy a další dokumenty, které kombinují fakturační informace s marketingovými informacemi. Výsledkem je kombinace vylepšeného zpracování obrázků, textu a dalších typů obsahu. PDF/VT umožňuje spolehlivou a dynamickou správu stránek pro tisková data HVTO (High Volume Transactional Output) pomocí konceptu metadat části dokumentu (DPM). Soubory PDF/VT lze otevřít v prohlížeči Adobe Acrobat bez nutnosti přidávat další komponenty.

## Hierarchie částí dokumentu ##

Hierarchie částí dokumentu (DPart) je jako stromová struktura uzlů částí dokumentu, která je založena na všech stránkách v dokumentu. Prvky tohoto stromu se nazývají uzly DPart. Každý vnitřní uzel obsahuje další uzly DPart a každý koncový uzel určuje jednu nebo více stránek pro příjemce. Hierarchie DPart v podstatě určuje pořadí a vztah dokumentů nebo částí dokumentů v souboru PDF/VT. Stromová struktura uzlů DPart snadno představuje vnitřní obsah dokumentu PDF/VT, protože může obsahovat dílčí dokumenty pro mnoho příjemců a každá část dokumentu odpovídá stránkám pro jednoho příjemce. V souborech PDF/VT je vyžadována hierarchie DPart.

## Metadata části dokumentu (DPM) ##

Metadata části dokumentu (DPM) jsou přidružena ke každému uzlu v hierarchii částí dokumentu a lze je použít ke sdělování informací o dílčím dokumentu konkrétního příjemce a jeho částech. Zejména DPM může obsahovat informace o vlastnostech nebo informace o příjemcích v zakódované podobě.

## Úrovně shody ##

PDF/VT se uděluje na následujících třech úrovních shody. Všechny jsou založeny na [PDF](/cs/pdf/) 1.6.

* `PDF/VT-1` - Je založen na PDF/X-4 a obsahuje všechny zdroje potřebné pro vykreslení dokumentu PDF.
* `PDF/VT-2` – Navrženo pro výměnu více souborů, dokumenty PDF/VT-2 mohou odkazovat na externí výstupní záměry, externí obsah nebo obojí. Dokument PDF/VT a všechny na něj odkazované soubory PDF a externí výstupní záměry se souhrnně nazývají sada souborů PDF/VT-2. Acrobat 9 a podporu této funkce.
* `PDF/VT-2s` - Podporuje živé vysílání PDF/VT-2. To umožňuje zpracování segmentovaných částí dat.

## Reference ##

* [PDF/VT – z Wikipedie](https://en.wikipedia.org/wiki/PDF/VT)
* [grafická technologie ISO 16612-2](https://www.iso.org/standard/46428.html)


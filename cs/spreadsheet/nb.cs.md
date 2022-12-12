{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "soubor", "přípona", "formát souboru", "Mathematica", "Tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Zjistěte, co je soubor NB API, který může vytvářet a otevírat soubory NB.",
  "title" :"NB - Formát souboru Mathematica Notebook",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Co je soubor NB?

Soubor s příponou .nb je formát souboru Wolfram notebooku, který ukládá instrukce pro matematické instrukce v textovém souboru. Může obsahovat mnoho různých typů dat, jako jsou živé výpočty, libovolná dynamická rozhraní, vstup s plnou sazbou, vstup obrázků, automatická anotace kódu, kompletní programové rozhraní na vysoké úrovni a tisíce pečlivě uspořádaných funkcí a možností. Textové instrukce jsou vstupem a výstupem Mathematica, který se generuje a aktualizuje při vkládání vstupních příkazů do souboru.

## Formát souborů Wolfram Notebook NB – Další informace

Soubory Wolfram Notebook NB jsou uloženy v prostém textovém formátu, což je formát souboru čitelný pro člověka. Obsah poznámkového bloku je uspořádán do sekcí jako prostý text, kde každá je reprezentována skupinami buněk, podobně jako tabulka. Rozsah těchto skupin je definován závorkou na konci každé buňky. Styl přiřazený buňce určuje její roli v poznámkovém bloku, jak je podrobně popsáno níže.

### Notebooky jako jazyk Wolfram

Pokud je zamýšleno uložit Notebook sestávající z matematických instrukcí pro provedení Wolfram Language Kernal, buňkám v dokumentu je automaticky přiřazen textový styl `Vstup`. To říká jádru, aby je považovalo za instrukce, které se provádějí, když uživatel vydá kombinaci kláves `Shift+Return`. Notebook Mathematica je znázorněn na následujícím příkladu.

{{< figure src="../Wolfram Notebook.jpeg" alt="Formát souborů pro notebook Wolfram" >}}

### Notebooky jako dokumenty

Poznámkové bloky Mathematica mohou být ve formátu dokumentu, aby vám poskytly pohled na to, co vidíte, co je to, co získáte (WYSIWYG). Tyto dokumenty jsou stejné jako dokumenty zobrazené na obrazovce nebo na tištěném papíře a jsou interaktivní. Za tímto účelem je buňce přiřazen `Textový styl`, který zobrazí obsah bez provádění příkazů jádra.

## Exportujte sešity Mathematica

Notebooky Mathematica lze exportovat do mnoha různých formátů souborů, jako je PDF, grafika, GIS, komprimovaný a tabulkový procesor.

## Reference

* [Základy notebooku Mathematica](https://reference.wolfram.com/language/guide/NotebookBasics.html)


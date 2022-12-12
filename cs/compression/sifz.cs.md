{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SIFZ File Format - Synfig Studio Compressed Project File",
  "description":"Další informace o formátu souboru SIFZ a rozhraních API, která mohou vytvářet a otevírat soubory SIFZ.",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## Co je soubor SIFZ?

Soubor SIFZ je komprimovaný soubor SIF gzip vytvořený open source aplikací pro vytváření 2D animací **Synfig Studio**. Obsahuje několik grafických prvků, které tvoří animaci. Celkový obsah animace je vytvořen pomocí kombinace plátna, které je vyplněno tvary, tahy štětcem nebo tužkou a textem. Všechny tyto jsou uspořádány ve svých vlastních polohách, úchopech poloměru, tečny, úhlu, vrcholu a šířky. Soubory SIFZ lze otevřít pomocí [Synfig Studio] (https://www.synfig.org/).

## Formát souboru SIFZ

Soubory SIFZ jsou komprimované soubory [ZIP](/cs/compression/zip/), které jsou zabaleny pomocí metody komprese gzip. Synfig se používá k vytváření animací ve filmové kvalitě pomocí vektorové a bitmapové předlohy. Na rozdíl od staré metody vytváření animací snímek po snímku vám umožňuje vytvářet 2D animace vyšší kvality s menším počtem zdrojů.

Komprimované soubory SIFZ jsou menší než nekomprimované soubory SIF. To také usnadňuje přenos přes internet s nízkou šířkou pásma.

## Reference

* [Synfig Open Source – Github](https://github.com/synfig/synfig/)
* [Dokumentace Synfig](https://synfig.readthedocs.io/en/latest/index.html)


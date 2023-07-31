{
  "date" : "2019-10-11",
  "keywords" :[ "soubor vstm", "formát souboru vstm", "co je soubor vstm", "soubor", "příklad vstm", "přípona souboru vstm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Microsoft Visio Template File Format",
  "description":"Další informace o formátu souborů VSTM a rozhraních API, která mohou vytvářet a otevírat soubory VSTM.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VSTM?

Soubory s příponou VSTM jsou soubory šablon vytvořené pomocí aplikace Microsoft Visio, které podporují makra. Na rozdíl od souborů VSDX mohou soubory vytvořené ze šablon VSTM spouštět makra, která jsou vyvinuta v kódu Visual Basic for Applications (VBA). Soubor šablony lze vytvořit za účelem poskytnutí základního nastavení dokumentu, který lze použít ke generování dalších dokumentů s těmito nastaveními. Soubory Visio se používají k vytváření výkresů, které obsahují vizuální objekty, vývojové diagramy, diagram UML, tok informací, organizační diagramy, softwarové diagramy, rozložení sítě, databázové modely, mapování objektů a další podobné informace. Soubory generované pomocí aplikace Visio lze také exportovat do různých formátů souborů, jako jsou PNG, BMP, PDF a další.

## Formát souboru ##

Soubory VSTM jsou založeny na Open Packaging Conventions a XML a vývojáři mohou těžit z tohoto formátu tím, že se naučí, jak s těmito soubory programově pracovat. Formát dědí mnoho stejných struktur XML jako jeho části z formátu souboru Visio XML Drawing (.vdx). Interoperabilita se soubory aplikace Visio je výrazně zvýšena, protože software třetích stran může pracovat se soubory aplikace Visio na úrovni formátu souboru.

Každý soubor aplikace Visio se nazývá balíček, který obsahuje další soubory nebo části. Část balíčku může být soubor XML, obrázek nebo dokonce řešení VBA. Části v balíčku lze rozdělit na části „dokument“ a „vztah“.

### Dokument ###

Části dokumentu obsahují skutečný obsah a metadata souboru Visio, jako je název souboru, první stránka a všechny obrazce, které obsahuje, a dokonce i datová připojení pro obrazce. Obrázky a textové soubory v balíčku jsou považovány za části dokumentu.

### Vztahy ###

Vztahové části souboru Visio jsou uloženy ve složce "_rels" a popisují, jak s nimi souvisí části v balíčku. Poskytuje také strukturu souboru. Samostatný dokument XML používá k určení vzájemného vztahu entit vztah nadřazený/podřízený prvek. Platný formát souboru Visio 2013 obsahuje správnou sadu částí a balíček obsahuje vztahy mezi částmi.

Části vztahů jsou dokumenty XML, které popisují vztahy mezi různými částmi dokumentu v balíčku. Definují přidružení mezi dvěma položkami: zadaným zdrojem (definovaným názvem a umístěním souboru vztahu) a zadanou cílovou částí dokumentu. Části vztahů se například používají k popisu toho, které předlohy tvarů jsou přidruženy k souboru, jak stránky souvisí se souborem a mezi sebou navzájem nebo jak se obrázky a objekty vztahují ke konkrétní stránce.

## Reference ##

* [Úvod do formátu souboru Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


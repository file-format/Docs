{
  "date" : "2019-10-11",
  "keywords" :[ "soubor vsdm", "formát souboru vsdm", "co je soubor vsdm", "soubor", "příklad vsdm", "přípona souboru vsdm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Microsoft Visio Drawing File Format",
  "description":"Další informace o formátu souborů VSDM a rozhraních API, která mohou vytvářet a otevírat soubory VSDM.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VSDM?

Soubory s příponou .vsdm jsou výkresové soubory vytvořené pomocí aplikace Microsoft Visio, která podporuje makra. Soubory VSDM jsou výkresy OPC/XML, které jsou podobné VSDX, ale také poskytují možnost spouštět makra při otevření souboru. Makra jsou uživatelem definované akce/kroky, které jsou vyvinuty ve Visual Basic for Applications (VBA) a lze je použít k provádění opakujících se úloh. Souborový formát VSDM byl představen se spuštěním aplikace Microsoft Visio 2013. Soubory Visio se používají k vytváření výkresů, které obsahují vizuální objekty, vývojové diagramy, diagram UML, tok informací, organizační diagramy, softwarové diagramy, rozložení sítě, databázové modely, mapování objektů a další podobné informace. Soubory vygenerované pomocí aplikace Visio lze také exportovat do různých formátů souborů, jako je [PNG](/cs/image/png/), [BMP](/cs/image/bmp/), [PDF](/cs/pdf/) a další.

## Formát souboru VSDM

Soubory VSDM jsou založeny na Open Packaging Conventions a XML a vývojáři mohou těžit z tohoto formátu tím, že se naučí, jak s těmito soubory programově pracovat. Formát dědí mnoho stejných struktur XML jako jeho části z formátu souboru Visio XML Drawing (.vdx). Interoperabilita se soubory aplikace Visio je výrazně zvýšena, protože software třetích stran může pracovat se soubory aplikace Visio na úrovni formátu souboru.

Každý soubor aplikace Visio se nazývá balíček, který obsahuje další soubory nebo části. Část balíčku může být soubor XML, obrázek nebo dokonce řešení VBA. Části v balíčku lze rozdělit na části „dokument“ a „vztah“.

### Dokument ###

Části dokumentu obsahují skutečný obsah a metadata souboru Visio, jako je název souboru, první stránka a všechny obrazce, které obsahuje, a dokonce i datová připojení pro obrazce. Obrázky a textové soubory v balíčku jsou považovány za části dokumentu.

### Vztahy ###

Vztahové části souboru Visio jsou uloženy ve složce "\_rels" a popisují, jak s nimi souvisí části v balíčku. Poskytuje také strukturu souboru. Samostatný dokument XML používá k určení vzájemného vztahu entit vztah nadřazený/podřízený prvek. Platný formát souboru Visio 2013 obsahuje správnou sadu částí a balíček obsahuje vztahy mezi částmi.

Části vztahů jsou dokumenty XML, které popisují vztahy mezi různými částmi dokumentu v balíčku. Definují přidružení mezi dvěma položkami: zadaným zdrojem (definovaným názvem a umístěním souboru vztahu) a zadanou cílovou částí dokumentu. Části vztahů se například používají k popisu toho, které předlohy tvarů jsou přidruženy k souboru, jak stránky souvisí se souborem a mezi sebou navzájem nebo jak se obrázky a objekty vztahují ke konkrétní stránce.

## Reference ##

* [Úvod do formátu souboru Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


{
  "date" : "2019-10-11",
  "keywords" :[ "soubor vstx", "formát souboru vstx", "co je soubor vstx", "soubor", "příklad vstx", "přípona souboru vstx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - Microsoft Visio File Format",
  "description":"Další informace o formátu souborů VSTX a rozhraních API, která mohou vytvářet a otevírat soubory VSTX.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VSTX?

Soubory s příponami .vstx jsou soubory šablon výkresů vytvořené pomocí aplikace Microsoft Visio 2013 a vyšší. Tyto soubory VSTX poskytují výchozí bod pro vytváření výkresů Visio, uložených jako soubory [.VSDX](/cs/image/vsdx/) s výchozím rozložením a nastavením. Obecně se soubory Visio používají k vytváření výkresů, které obsahují vizuální objekty, vývojové diagramy, diagram UML, tok informací, organizační diagramy, softwarové diagramy, rozložení sítě, databázové modely, mapování objektů a další podobné informace. Soubory generované pomocí aplikace Visio lze také exportovat do různých formátů souborů, jako je [PNG](/cs/Image/PNG/), [BMP](/cs/Image/BMP/), [PDF](/cs/pdf/) a další. Mezi programy, které otevírají soubory VSTX, patří Microsoft Visio pro Windows a Mac, které umožňují otevřít tyto soubory pro prohlížení a úpravy. Umožňuje také převádět formáty souborů aplikace Visio do řady dalších formátů.

# Formát souboru VSTX #

„X“ v příponě souboru odkazuje na formát souboru OpenOffice, který společnost Microsoft zavedla jako formát archivního souboru [ZIP](/cs/compression/zip/) jako náhradu za dříve podporované binární formáty souborů. Soubory VSTX jsou tedy založeny na formátu souboru XML specifikací OpenOffice na rozdíl od formátu souboru [.VST](/cs/image/vst/), který je v binárním formátu.

Soubory VSDX jsou založeny na konvencích Open Packaging Conventions a XML a vývojáři mohou z tohoto formátu těžit tím, že se naučí, jak s těmito soubory programově pracovat. Formát dědí mnoho stejných struktur XML jako jeho části z formátu souboru Visio XML Drawing (.vdx). Interoperabilita se soubory aplikace Visio je výrazně zvýšena, protože software třetích stran může pracovat se soubory aplikace Visio na úrovni formátu souboru.

Některé další typy souborů, které tvoří formát souboru Visio 2013, zahrnují:

* .vsdm (kresba s podporou maker aplikace Visio)
* .vssx (vzorník Visio)
* .vssm (vzorník s podporou maker Visio)
* .vstx (šablona Visio)
* .vstm (šablona s podporou maker aplikace Visio)

Formát souboru Visio 2013 pod kapotou používá strukturované prostředky k ukládání dat aplikace spolu se souvisejícími zdroji v archivu, jako je [ZIP](/cs/compression/zip/). Soubor ZIP lze extrahovat pomocí libovolného standardního extrakčního nástroje, pokud obsahuje i jiné typy souborů. Můžete jednoduše nahradit příponu souboru .VSTX příponou .ZIP v průzkumu Windows, abyste viděli obsah uvnitř souboru VSTX.

Každý soubor aplikace Visio se nazývá balíček, který obsahuje další soubory nebo části. Část balíčku může být soubor XML, obrázek nebo dokonce řešení VBA. Části v balíčku lze rozdělit na části „dokument“ a „vztah“.

### Dokument ###

Části dokumentu obsahují skutečný obsah a metadata souboru Visio, jako je název souboru, první stránka a všechny obrazce, které obsahuje, a dokonce i datová připojení pro obrazce. Obrázky a textové soubory v balíčku jsou považovány za části dokumentu.

### Vztahy ###

Vztahové části souboru Visio jsou uloženy ve složce "_rels" a popisují, jak s nimi souvisí části v balíčku. Poskytuje také strukturu souboru. Samostatný dokument XML používá k určení vzájemného vztahu entit vztah nadřazený/podřízený prvek. Platný formát souboru Visio 2013 obsahuje správnou sadu částí a balíček obsahuje vztahy mezi částmi.

Části vztahů jsou dokumenty XML, které popisují vztahy mezi různými částmi dokumentu v balíčku. Definují přidružení mezi dvěma položkami: zadaným zdrojem (definovaným názvem a umístěním souboru vztahu) a zadanou cílovou částí dokumentu. Části vztahů se například používají k popisu toho, které předlohy tvarů jsou přidruženy k souboru, jak stránky souvisí se souborem a mezi sebou navzájem nebo jak se obrázky a objekty vztahují ke konkrétní stránce.

## Reference ##

* [Úvod do formátu souboru Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


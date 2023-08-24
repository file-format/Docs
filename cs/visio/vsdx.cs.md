{
  "date" : "2019-10-11",
  "keywords" :[ "soubor vsdx", "formát souboru vsdx", "co je soubor vsdx", "soubor", "příklad vsdx", "přípona souboru vsdx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Další informace o formátu souborů VSDX a rozhraních API, která mohou vytvářet a otevírat soubory VSDX.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VSDX?

Soubory s příponou .vsdx představují formát souborů Microsoft Visio zavedený od Microsoft Office 2013 a novější. Byl vyvinut, aby nahradil formát binárního souboru [.VSD](/cs/visio/vsd/), který je podporován dřívějšími verzemi aplikace Microsoft Visio. Je také podporován ve službách Visio na serveru Microsoft SharePoint Server 2013 a pro publikování na serveru SharePoint nevyžaduje zprostředkující formát souboru. Soubory Visio se používají k vytváření výkresů, které obsahují vizuální objekty, vývojové diagramy, diagram UML, tok informací, organizační diagramy, softwarové diagramy, rozložení sítě, databázové modely, mapování objektů a další podobné informace. Soubory vygenerované pomocí aplikace Visio lze také exportovat do různých formátů souborů, jako je [PNG](/cs/image/png/), [BMP](/cs/image/bmp/), [PDF](/cs/pdf/) a další.

## Formát souboru ##

Soubory VSDX jsou založeny na konvencích Open Packaging Conventions a XML a vývojáři mohou z tohoto formátu těžit tím, že se naučí, jak s těmito soubory programově pracovat. Formát dědí mnoho stejných struktur XML jako jeho části z formátu souboru Visio XML Drawing (.vdx). Interoperabilita se soubory aplikace Visio je výrazně zvýšena, protože software třetích stran může pracovat se soubory aplikace Visio na úrovni formátu souboru.

Některé další typy souborů, které tvoří formát souboru Visio 2013, zahrnují:

* .vsdm (kresba s podporou maker aplikace Visio)
* .vssx (vzorník Visio)
* .vssm (vzorník s podporou maker Visio)
* .vstx (šablona Visio)
* .vstm (šablona s podporou maker aplikace Visio)

Formát souboru Visio 2013 pod kapotou používá strukturované prostředky k ukládání dat aplikace spolu se souvisejícími zdroji v archivu, jako je [ZIP](/cs/compression/zip/). Soubor ZIP lze extrahovat pomocí libovolného standardního extrakčního nástroje, pokud obsahuje i jiné typy souborů. Chcete-li zobrazit obsah uvnitř souboru VSDX, můžete jednoduše nahradit příponu souboru .vsdx příponou .zip.

Každý soubor aplikace Visio se nazývá balíček, který obsahuje další soubory nebo části. Část balíčku může být soubor XML, obrázek nebo dokonce řešení VBA. Části v balíčku lze rozdělit na části „dokument“ a „vztah“.

### Dokument ###

Části dokumentu obsahují skutečný obsah a metadata souboru Visio, jako je název souboru, první stránka a všechny obrazce, které obsahuje, a dokonce i datová připojení pro obrazce. Obrázky a textové soubory v balíčku jsou považovány za části dokumentu.

### Vztahy ###

Vztahové části souboru Visio jsou uloženy ve složce "\_rels" a popisují, jak s nimi souvisí části v balíčku. Poskytuje také strukturu souboru. Samostatný dokument XML používá k určení vzájemného vztahu entit vztah nadřazený/podřízený prvek. Platný formát souboru Visio 2013 obsahuje správnou sadu částí a balíček obsahuje vztahy mezi částmi.

Části vztahů jsou dokumenty XML, které popisují vztahy mezi různými částmi dokumentu v balíčku. Definují přidružení mezi dvěma položkami: zadaným zdrojem (definovaným názvem a umístěním souboru vztahu) a zadanou cílovou částí dokumentu. Části vztahů se například používají k popisu toho, které předlohy tvarů jsou přidruženy k souboru, jak stránky souvisí se souborem a mezi sebou navzájem nebo jak se obrázky a objekty vztahují ke konkrétní stránce.

## Reference ##

* [Úvod do formátu souboru Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


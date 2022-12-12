{
  "date" : "2019-10-11",
  "keywords" :[ "soubor vssx", "formát souboru vssx", "co je soubor vssx", "soubor", "příklad vssx", "přípona souboru vssx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSX - Visio Stencil File Format",
  "description":"Další informace o formátu souborů VSSX a rozhraních API, která mohou vytvářet a otevírat soubory VSSX.",
  "linktitle" : "VSSX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VSSX?

Soubory s příponou .vssx jsou šablony výkresů vytvořené pomocí [Microsoft Visio](https://products.office.com/en/visio/flowchart-software) 2013 a vyšší. Formát souboru VSSX lze otevřít pomocí aplikace Visio 2013 a vyšší. Soubory Visio jsou známé pro reprezentaci různých prvků výkresu, jako jsou kolekce tvarů, konektory, vývojové diagramy, rozložení sítě, diagramy UML, softwarové diagramy, databázové modely, mapování objektů a další podobné informace. Microsoft Visio také poskytuje možnost převádět soubory Visio do různých formátů souborů, jako je [PNG](/cs/image/png/), [BMP](/cs/image/bmp/), [PDF](/cs/pdf/) a další. Je k dispozici pro Windows i Mac OS.

## Formát souboru VSSX

Formát souboru VSSX je založen na formátu OpenOffice přijatém společností Microsoft od roku 2007. Je založen na archivu [ZIP](/cs/compression/zip/), který představuje celkový formát souboru založený na specifikacích formátu souboru XML. Ekvivalent binárního formátu souboru VSSX byl VSS, který byl podporován až do Visio 2007. Obsah formátu souboru VSSX můžete zobrazit nahrazením jeho přípony .ZIP a otevřít jej v libovolném formátu archivačního souboru, jako je WinZIP.

Soubory VSDX jsou založeny na konvencích Open Packaging Conventions a XML a vývojáři mohou z tohoto formátu těžit tím, že se naučí, jak s těmito soubory programově pracovat. Formát dědí mnoho stejných struktur XML jako jeho části z formátu souboru Visio XML Drawing (.vdx). Interoperabilita se soubory aplikace Visio je výrazně zvýšena, protože software třetích stran může pracovat se soubory aplikace Visio na úrovni formátu souboru.

Některé další typy souborů, které tvoří formát souboru Visio 2013, zahrnují:

* .vsdm (kresba s podporou maker aplikace Visio)
* .vssx (vzorník Visio)
* .vssm (vzorník s podporou maker Visio)
* .vstx (šablona Visio)
* .vstm (šablona s podporou maker aplikace Visio)

Každý soubor aplikace Visio se nazývá balíček, který obsahuje další soubory nebo části. Část balíčku může být soubor XML, obrázek nebo dokonce řešení VBA. Části v balíčku lze rozdělit na části „dokument“ a „vztah“.

## Reference ##

* [Úvod do formátu souboru Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
* [Mapa schémat – Visio XML](https://docs.microsoft.com/en-us/office/client-developer/visio/schema-mapvisio-xml)


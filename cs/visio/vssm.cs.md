{
  "date" : "2019-10-11",
  "keywords" :[ "soubor vssm", "formát souboru vssm", "co je soubor vssm", "soubor", "příklad vssm", "přípona souboru vssm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSM - Microsoft Visio Macro Enabled File Format",
  "description":"Další informace o formátu souborů VSSM a rozhraních API, která mohou vytvářet a otevírat soubory VSSM.",
  "linktitle" : "VSSM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VSSM?

Soubory s příponou .vssm jsou soubory šablony Microsoft Visio, které podporují makra. Soubor VSSM při otevření umožňuje spouštět makra pro dosažení požadovaného formátování a umístění tvarů v diagramu. Microsoft Visio je obecně kreslicí software, který umožňuje vytvářet soubory, které mohou obsahovat a reprezentovat uživatelem definované informace v různých tvarech. Mezi nejběžnější z nich patří mimo jiné diagramy UML, vývojové diagramy, vizuální objekty, tok informací, organizační diagramy, softwarové diagramy, uspořádání sítě, databázové modely, mapování objektů a další podobné informace. Soubory generované pomocí aplikace Visio lze také převést do různých formátů souborů, jako je [PNG](/cs/Image/PNG/), [BMP](/cs/Image/BMP/), [PDF](/cs/pdf/) a další.

## Formát souboru VSSM

Formát souboru VSSM byl zaveden s Microsoft Visio 2013, který je založen na specifikacích OpenOffice XML. Některé další typy souborů, které tvoří formát souboru Visio 2013, zahrnují:

* .vsdm (kresba s podporou maker aplikace Visio)
* .vssx (vzorník Visio)
* .vssm (vzorník s podporou maker Visio)
* .vstx (šablona Visio)
* .vstm (šablona s podporou maker aplikace Visio)

Formát souboru Visio 2013 pod kapotou používá strukturované prostředky k ukládání dat aplikace spolu se souvisejícími zdroji v archivu, jako je [ZIP](/cs/Compression/ZIP/). Soubor ZIP lze extrahovat pomocí libovolného standardního extrakčního nástroje, pokud obsahuje i jiné typy souborů.

Každý soubor aplikace Visio se nazývá balíček, který obsahuje další soubory nebo části. Část balíčku může být soubor XML, obrázek nebo dokonce řešení VBA. Části v balíčku lze rozdělit na části „dokument“ a „vztah“.

## Reference ##

* [Úvod do formátu souboru Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


{
  "date" : "2019-10-11",
  "keywords" : [ "vssx file", "vssx file format", "what is a vssx file", "file", "vssx example", "vssx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSSX - Visio Stencil File Format",
  "description":"Lær om VSSX filformat og API'er, der kan oprette og åbne VSSX filer.",
  "linktitle" : "VSSX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssx-da",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Hvad er en VSSX fil?

Filer med filtypenavnet .vssx er tegnestencils oprettet med [Microsoft Visio](https://products.office.com/en/visio/flowchart-software) 2013 og nyere. VSSX-filformatet kan åbnes med Visio 2013 og nyere. Visio-filer er kendt for repræsentation af en række tegningselementer, såsom samling af former, forbindelser, flowcharts, netværkslayout, UML-diagrammer, softwarediagrammer, databasemodeller, objektkortlægning og anden lignende information. Microsoft Visio giver også mulighed for at konvertere Visio-filer til forskellige filformater såsom [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) og andre. Den er tilgængelig til både Windows og Mac OS.

## VSSX filformat

The VSSX file format is based on the OpenOffice format adopted by Microsoft since 2007. Det er baseret på [ZIP](/compression/zip/)-arkivet, der repræsenterer det overordnede filformat baseret på XML-filformatspecifikationer. Det binære filformat, der svarer til VSSX, var VSS, der blev understøttet indtil Visio 2007. Du kan se indholdet af VSSX-filformatet ved at erstatte dets filtypenavn med .ZIP og åbne i ethvert arkiveringsfilformat, såsom WinZIP.

VSDX-filer er baseret på Open Packaging Conventions og XML, og udviklere kan drage fordel af dette format ved at lære, hvordan man arbejder med disse filer programmatisk. Formatet arver mange af de samme XML-strukturer som dets dele fra Visio XML Drawing-filformatet (.vdx). Interoperabilitet med Visio-filer er stærkt øget, da tredjepartssoftware kan manipulere Visio-filer på et filformatniveau.

Visse andre filtyper, der omfatter Visio 2013-filformatet, omfatter:

* .vsdm (Visio makroaktiveret tegning)

* .vssx (Visio stencil)

* .vssm (Visio makro-aktiveret stencil)

* .vstx (Visio-skabelon)

* .vstm (Visio makro-aktiveret skabelon)


Hver Visio-fil betegnes som pakke, der indeholder andre filer eller dele. En pakkedel kan være en XML-fil, et billede eller endda en VBA-løsning. Delene i pakken kan opdeles i dokument- og relations-dele.

## Referencer ##

* [Introduktion til Visio-filformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

* [Skemakort - Visio XML](https://learn.microsoft.com/en-us/office/client-developer/visio/schema-mapvisio-xml)



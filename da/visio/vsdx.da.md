{
  "date" : "2019-10-11",
  "keywords" : [ "vsdx file", "vsdx file format", "what is a vsdx file", "file", "vsdx example", "vsdx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDX",
  "description":"Lær om VSDX-filformat og API'er, der kan oprette og åbne VSDX-filer.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx-da",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Hvad er en VSDX fil?

Filer med filtypenavnet .vsdx repræsenterer Microsoft Visio-filformat introduceret fra Microsoft Office 2013 og fremefter. Det blev udviklet til at erstatte det binære filformat, [.VSD](/visio/vsd/), som understøttes af tidligere versioner af Microsoft Visio. Det understøttes også på Visio Services i Microsoft SharePoint Server 2013 og kræver ikke et mellemliggende filformat til udgivelse til SharePoint Server. Visio-filer bruges til at lave tegninger, der indeholder visuelle objekter, flowdiagrammer, UML-diagram, informationsflow, organisationsdiagrammer, softwarediagrammer, netværkslayout, databasemodeller, objektkortlægning og anden lignende information. Filer genereret ved hjælp af Visio kan også eksporteres til forskellige filformater såsom [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) og andre.

## Filformat ##

VSDX-filer er baseret på Open Packaging Conventions og XML, og udviklere kan drage fordel af dette format ved at lære, hvordan man arbejder med disse filer programmatisk. Formatet arver mange af de samme XML-strukturer som dets dele fra Visio XML Drawing-filformatet (.vdx). Interoperabilitet med Visio-filer er stærkt øget, da tredjepartssoftware kan manipulere Visio-filer på et filformatniveau.

Visse andre filtyper, der omfatter Visio 2013-filformatet, omfatter:

* .vsdm (Visio makroaktiveret tegning)

* .vssx (Visio stencil)

* .vssm (Visio makro-aktiveret stencil)

* .vstx (Visio-skabelon)

* .vstm (Visio makro-aktiveret skabelon)


Under hætten bruger Visio 2013-filformatet et struktureret middel til at gemme applikationsdata sammen med relaterede ressourcer i et arkiv såsom [ZIP](/compression/zip/). ZIP-filen kan udpakkes ved hjælp af et hvilket som helst standardudtræksværktøj, hvor det også indeholder andre typer filer. Du kan bare erstatte .vsdx-filtypen med .zip i Windows Explorer for at se indholdet inde i VSDX-filen.

Hver Visio-fil betegnes som pakke, der indeholder andre filer eller dele. En pakkedel kan være en XML-fil, et billede eller endda en VBA-løsning. Delene i pakken kan opdeles i dokument- og relations-dele.

### Dokument ###

Dokumentdelene indeholder det faktiske indhold og metadata af Visio-filen, som navnet på filen, den første side og alle de figurer, den indeholder, og endda dataforbindelserne for figurerne. Billeder og tekstfiler i pakken betragtes som dokumentdele.

### Relationer ###

Relationsdelene af en Visio-fil gemmes i mappen \_rels og beskriver, hvordan delene i pakken er relateret til hver. Det giver også strukturen af filen. Et selvstændigt XML-dokument bruger elementernes overordnede/underordnede forhold til at bestemme forholdet mellem enheder til hinanden. Et gyldigt Visio 2013-filformat indeholder det korrekte sæt af dele, og pakken indeholder relationerne mellem delene.

Relationsdele er XML-dokumenter, der beskriver relationerne mellem forskellige dokumentdele i pakken. De definerer en tilknytning mellem to elementer: en specificeret kilde (defineret af navnet og placeringen af relationsfilen) og en specificeret måldokumentdel. For eksempel bruges relationsdele til at beskrive, hvilke formmastere, der er knyttet til filen, hvordan sider relaterer sig til filen og til hinanden, eller hvordan billeder og objekter relaterer til en bestemt side.

## Referencer ##

* [Introduktion til Visio-filformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)



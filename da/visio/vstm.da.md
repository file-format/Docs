{
  "date" : "2019-10-11",
  "keywords" : [ "vstm file", "vstm file format", "what is a vstm file", "file", "vstm example", "vstm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSTM - Microsoft Visio skabelonfilformat",
  "description":"Lær om VSTM filformat og API'er, der kan oprette og åbne VSTM filer.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm-da",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Hvad er VSTM fil?

Filer med VSTM-udvidelse er skabelonfiler oprettet med Microsoft Visio, der understøtter makroer. I modsætning til VSDX-filer kan filer, der er oprettet fra VSTM-skabeloner, køre makroer, der er udviklet i Visual Basic for Applications (VBA)-kode. En skabelonfil kan oprettes for at give grundlæggende indstillinger for dokumentet, som kan bruges til at generere yderligere dokumenter med disse indstillinger. Visio-filer bruges til at lave tegninger, der indeholder visuelle objekter, flowdiagrammer, UML-diagram, informationsflow, organisationsdiagrammer, softwarediagrammer, netværkslayout, databasemodeller, objektkortlægning og anden lignende information. Filer genereret ved hjælp af Visio kan også eksporteres til forskellige filformater såsom PNG, BMP, PDF og andre.

## Filformat ##

VSTM-filer er baseret på Open Packaging Conventions og XML, og udviklere kan drage fordel af dette format ved at lære at arbejde med disse filer programmatisk. Formatet arver mange af de samme XML-strukturer som dets dele fra Visio XML Drawing-filformatet (.vdx). Interoperabilitet med Visio-filer er stærkt øget, da tredjepartssoftware kan manipulere Visio-filer på et filformatniveau.

Hver Visio-fil betegnes som pakke, der indeholder andre filer eller dele. En pakkedel kan være en XML-fil, et billede eller endda en VBA-løsning. Delene i pakken kan opdeles i dokument- og relations-dele.

### Dokument ###

Dokumentdelene indeholder det faktiske indhold og metadata af Visio-filen, som navnet på filen, den første side og alle de figurer, den indeholder, og endda dataforbindelserne for figurerne. Billeder og tekstfiler i pakken betragtes som dokumentdele.

### Relationer ###

Relationsdelene af en Visio-fil gemmes i mappen _rels og beskriver, hvordan delene i pakken er relateret til hver. Det giver også strukturen af filen. Et selvstændigt XML-dokument bruger elementernes overordnede/underordnede forhold til at bestemme forholdet mellem enheder til hinanden. Et gyldigt Visio 2013-filformat indeholder det korrekte sæt af dele, og pakken indeholder relationerne mellem delene.

Relationsdele er XML-dokumenter, der beskriver relationerne mellem forskellige dokumentdele i pakken. De definerer en tilknytning mellem to elementer: en specificeret kilde (defineret af navnet og placeringen af relationsfilen) og en specificeret måldokumentdel. For eksempel bruges relationsdele til at beskrive, hvilke shape-mastere der er knyttet til filen, hvordan sider relaterer til filen og til hinanden, eller hvordan billeder og objekter relaterer til en bestemt side.

## Referencer ##

* [Introduktion til Visio-filformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)



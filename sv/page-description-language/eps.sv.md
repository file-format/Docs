{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "fil", "tillägg", "filformat", "Sidlayout", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om EPS-filformat och API:er som kan skapa och öppna EPS-filer.",
  "title" :"EPS-filformat - Encapsulated PostScript-fil",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en EPS-fil?

En .eps-fil är en bildfil som sparas på skiva i Encapsulated Postscript-filformat. Den kan innehålla valfri kombination av text, grafik och bilder. EPS-filer kan också innehålla en bitmappsförhandsvisningsbild inkapslad inuti för visning av program som kan öppna sådana filer.

## Kort historia av EPS-filformat

En snabb titt på EPS-filformat ur historiskt perspektiv avslöjar följande information:

* Den första versionen av EPS släpptes av Adobe någon gång mellan 1985 och 1988
* Version 2.0 av EPS-specifikationen publicerades i januari 1989
* Specifikationen för version 3.0 av EPS publicerades som ett separat dokument 1992; detta är den senaste publicerade versionen.

EPS, i kombination med tilläggsmekanismen för Open Structuring Conventions som beskrivs i klausul 9 i Adobes specifikation för PostScript Language Document Structurering Conventions, utgjorde grunden för tidiga versioner av filformatet Adobe Illustrator Artwork.

## EPS filformat

EPS är ett proprietärt men offentligt dokumenterat format och EPS-filformatspecifikationer är tillgängliga offentligt för utvecklarens referens. EPS är ett [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) som överensstämmer med filformatet och följer alla regler som fastställts av DSC. DSC är ett speciellt filformat för PostScript-dokument från Adobe. Alla program som påstår sig kunna läsa EPS-filer bör vara DSC-kompatibla.

En EPS-fil består av två huvudsektioner som förklaras nedan.

### Förhandsgranskningsbild ###

En typisk EPS-fil innehåller en förhandsgranskningsbild i ett format som är avsett för bekväm användning i ett arbetsflöde som involverar flera system eller applikationer. Avsikten med en förhandsvisning är att ha en bild i ett format som de flesta grafikapplikationer kan rendera; en förhandsvisning är vanligtvis av lägre upplösning, i pixeldimensioner och/eller i bitdjup. Förhandsgranskningsfilen kan vara i ett av ett antal format. Specifikationen för EPS_3 listar tre "enhetsspecifika" förhandsvisningsformat:

* för Apple Macintosh, en PICT-bild som används av QuickDraw-programmet
* för DOS-datorer, en TIFF-bitmapp
* Windows Metafil.

PICT och Windows Metafile kan innehålla både bitmappsdata och vektorgrafik. Dessutom definierar specifikationen en mycket enkel enhetsoberoende representation för en inbäddad bitmappad förhandsvisningsbild. Denna representation är känd som Encapsulated PostScript Interchange Format (EPSI).

En EPSI-förhandsvisning är en bitmapp representerad som ASCII-hexadecimal, inlindad mellan några PostScript-kommentarer för identifiering och avsedd att vara enkel och lätt att transportera. För att särskilja EPS-filer med de olika förhandsgranskningsformaten rekommenderades olika DOS-filtillägg och Macintosh-filtyper i EPS-specifikationen.

### PostScript-kod

EPS-filformatet måste åtminstone innehålla följande:

* en rubrikkommentar, %!PS-Adobe-3.0 EPSF-3.0
* och en kommentar om begränsningsrutan, %%BoundingBox: llx lly urx ury, som beskriver gränserna för illustrationen. Dessa fyra argument motsvarar de nedre vänstra (llx, lly) och övre högra hörnen (urx, ury) i begränsningsrutan.

En EPS-fil kan inte använda någon av följande operatorer:

* bandenhet,
* cleardictstack
* kopiera sida
* radera sida
* exitserver
* ramenhet
* grestoreall
* initclip
* initgrafik
* initmatris
* sluta med
* renderband
*setglobal
* setpagedevice
*set delad
*startjobb.

## Konvertering av EPS till andra filformat

EPS-filer kan konverteras till standardbildformat som [JPG](/sv/image/jpeg/), [PNG](/sv/image/png/), [TIFF](/sv/image/tiff/) och [PDF](/sv/pdf /) med olika applikationer t.ex. Adobe Illustrator, Photoshop och PaintShop Pro.

På grund av en [säkerhetssårbarhet](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) i EPS-filer, Office 2016, Office 2013, Office 2010 och Office 365 har stängt av möjligheten att infoga EPS-filer i Office-dokument.

## Referenser

* [Encapsulated PostScript - av Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)


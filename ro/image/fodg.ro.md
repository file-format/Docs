{
  "date" : "2019-10-11",
  "keywords" :[ "fișier fodg", "format fișier fodg", "ce este un fișier fodg", "fișier", "exemplu fodg", "extensie fișier fodg", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - Format de fișier de desen OpenDocument",
  "description":"Aflați despre formatul de fișier FODG și despre API-urile care pot crea și deschide fișiere FODG.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier FODG?

Un fișier cu extensia .fodg este un format de fișier Apache OpenOffice Drawing pentru stocarea elementelor de desen. Acesta se bazează pe specificațiile de format de fișier prezentate de Advancement of Structural Information Standards (OASIS). Un alt format de fișier similar pentru grafica OpenOffice este [ODG](/ro/image/odg/) care stochează elemente de desen ca imagine vectorială. Fișierele FODG pot fi deschise atât cu OpenOffice, cât și cu LibreOffice. Alte formate de fișiere acceptate de OpenOffice, de exemplu, includ [ODT](/ro/word-processing/odt/), ODF, [ODP](/ro/presentation/odp/) și [ODS](/ro/spreadsheet/ods/).

## Format de fișier FODG

FODG se bazează pe formatul de fișier XML al OpenDocument, care este conform cu OASIS OpenDocument Format ISO/IEC 26300. Are Internet Media Type application/vnd.oasis.opendocument.graphics și, de asemenea, este conform cu org.oasis-open.opendocument public.composite-content . Structura XML este comună pentru toate tipurile de documente, cum ar fi foile de calcul, desenele și documentele text. Documentele OpenOffice profită de separarea preocupărilor prin separarea conținutului, stilurilor, metadatelor și setărilor aplicației în patru fișiere XML separate.

`<office:document-content>` - Conținutul documentului și stilurile automate utilizate în conținut.
`<office:document-styles>` - Stiluri utilizate în conținutul documentului și stiluri automate utilizate în stilurile în sine.
`<office:document-meta>` - Meta informațiile documentului, cum ar fi autorul sau ora ultimei acțiuni de salvare.
`<office:document-settings>` - Setări specifice aplicației, cum ar fi dimensiunea ferestrei sau informațiile despre imprimantă.

## Referințe ##
* [Specificații viitoare pentru standardizarea v 1.3 ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


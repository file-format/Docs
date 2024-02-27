{
  "date": "2019-10-11",
  "keywords": [
"odg fil",
"odg filformat",
"hvad er en odg-fil",
"fil",
"odg eksempel",
"odg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODG filformat",
  "description": "Lær om ODG-filformat og API'er, der kan oprette og åbne ODG-filer.",
  "linktitle": "ODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-od-dag"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en ODG fil?

ODG-filformatet bruges af Apache OpenOffice's Draw-applikation til at gemme tegningselementer som et vektorbillede. Det følger de XML-baserede filformatspecifikationer skitseret af Advancement of Structural Information Standards (OASIS). ODG repræsenterer tegninger som vektorbilleder ved hjælp af punkter, linjer og kurver. Udover OpenOffice giver LibreOffice og andre applikationer også støtte til at arbejde med ODG-filformat. Andre formater, der understøttes af OpenOffice, omfatter f.eks. [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) og [ODS](/spreadsheet/ods/).


## ODG filformatspecifikationer

ODG-filformat er baseret på OpenDocument-format, der er struktureret XML-dokumentformat med veldefineret skema.
Hver strukturel komponent i et OpenDocument-format er repræsenteret af et element, der har tilknyttede attributter. Den XML-baserede struktur er fælles for alle dokumenttyper såsom tekstdokument, regneark eller en tegnefil. Et dokument kan indeholde forskellige stilarter. En OpenDocument-filstruktur består af følgende elementer.
  * Dokumentrod
  * Dokument MetaData
  * Body Element og Dokumenttyper
  * Applikationsindstillinger
  * Scripts
  * Skrifttypeerklæringer
  * Stilarter
  * Sidestile og layout

##  Dokumentrødder ##

Et dokumentrodelement indeholder hele dokumentet og er det primære element i en fil i OpenDocument-format. De samme typer dokumentrodelementer kan anvendes til alle typer dokumenter, såsom tekst, dokumenter, regneark og tegnedokumenter.

### Rodelementer ###
Et enkelt XML-dokument er repræsenteret af sit eget rodelement. De fem forskellige understøttede rodelementer er som følger.

`<office:document> ` - Fuldfør Office-dokument i et enkelt XML-dokument.
`<office:document-content> ` - Dokumentindhold og automatiske stilarter, der bruges i indholdet.
`<office:document-styles> ` - Typografier brugt i dokumentindholdet og automatiske typografier brugt i selve typografierne.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` - Programspecifikke indstillinger, såsom vinduesstørrelse eller printeroplysninger.

### ODG Document MetaData ###
The OpenDocument contains all metadata elements in the \<office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### Brødelement og dokumenttyper ###
Dokumentets brødtekst angiver typen af indhold, der er indeholdt i dokumentet ved hjælp af dokumenttypeelementet. Disse dokumenttyper er:
  * tekstdokumenter
  * tegne dokumenter
  * præsentationsdokumenter
  * regnearksdokumenter
  * diagramdokumenter
  * billeddokumenter

### Applikationsindstillinger ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * Dokumentindstillinger f.eks. standardprinter
  * Vis Indstillinger f.eks. zoomniveau

### Scripts ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### Skrifttypeerklæringer ###

En skrifttypeerklæring indeholder oplysninger om de skrifttyper, der bruges af forfatteren til et dokument. Disse oplysninger hjælper med at finde disse skrifttyper på andre systemer.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Stilarter ###
Følgende stilarter understøttes af OpenDocument-formatet.

Fælles stilarter - XML-repræsentationerne af sådanne stilarter omtales som stilarter
`Automatiske typografier` - Indeholder formateringsegenskaber, der i brugergrænsefladevisningen af et dokument er tildelt til et objekt såsom et afsnit.
`Mater Styles` - en almindelig typografi, der indeholder formateringsoplysninger og yderligere indhold, der vises sammen med dokumentindholdet, når typografien anvendes. Et eksempel på en masterstil er mastersider.

## Referencer ##
  * [OASIS Open Document Format for Office-applikationer](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


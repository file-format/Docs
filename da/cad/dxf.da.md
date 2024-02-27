{
  "date": "2020-03-16",
  "keywords": [
"DXF fil",
"Filformat",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om DXF-filformat og API'er, der kan oprette og åbne DXF-filer.",
  "title": "DXF filformat",
  "linktitle": "DXF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dx-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en DXF fil?

DXF, Drawing Interchange Format eller Drawing Exchange Format, er en mærket datarepræsentation af AutoCAD-tegnefil. Hvert element i filen har et præfiks heltal kaldet en gruppekode. Denne gruppekode repræsenterer faktisk det element, der følger, og angiver betydningen af et dataelement for en given objekttype. DXF gør det muligt at repræsentere næsten al brugerspecificeret information i en tegnefil.

DXF-filformat blev udviklet af Autodesk som CAD-datafilformat til datainteroperabilitet mellem AutoCAD og andre applikationer. Således kan data importeres fra andre formater til DXF til AutoCAD i henhold til DXF-filformatets interoperabilitetsspecifikationer.

## Kort historie ##


The history of DXF file format dates back to 1982 when it was introduced as part of AutoCAD 1.0. Oprindelige versioner af AutoCAD understøtter kun ASCII-filformatet DXF. Med udgivelsen 10 af AutoCAD (og derover) i 1988 blev understøttelse af både ASCII og binære DXF-filformater introduceret i AutoCAD. I de tidligere stadier delte Autodesk ikke nogen filformatspecifikationer, og på grund af dette var korrekt import af DXF-filer ikke let. Men Autodesk udgiver nu DXF-specifikationerne og er tilgængelige for offentligheden.

## Filformatspecifikationer ##

DXF-filformatet bruger gruppekoden og værdiparrene til at arrangere indholdet i sektioner. Hver sektion er sammensat af poster, hvor hver post består af en gruppekode og dataelement. Hver gruppekode og værdi er på deres egen linje i DXF-filen. Hver sektion starter med en gruppekode 0 efterfulgt af strengen SECTION. Dette efterfølges af en gruppekode 2 og en streng, der angiver navnet på sektionen (f.eks. SECTION1). Hver sektion er sammensat af gruppekoder og værdier, der definerer dens elementer. Et afsnit slutter med et 0 efterfulgt af strengen ENDSEC.

DXF-filformat betragter objekter, der er forskellige fra enheder. Objekter har ingen grafisk repræsentation her, men entiteter har det. Således omtales indgange i DXF som grafiske objekter, mens objekter omtales som ikke-grafiske objekter. BLOCK- og ENTITIES-sektionerne i DXF-filen indeholder Entities, og brugen af gruppekoder i disse to sektioner er identisk. Slutningen af en enhed er angivet med den næste 0-gruppe, som begynder den næste enhed eller angiver slutningen af afsnittet.

### Filstruktur ###

Sektioner i en DXF-fil er arrangeret i følgende rækkefølge:

|Section|Basic description
---|---|
|Header|Dette afsnit indeholder generel information om tegningen. Det er ligesom indstillingsfunktionen i din telefon, som indeholder de forskellige variabler, der er forbundet med tegningen og dens tilknyttede værdier. For eksempel vil Header-sektionen definere, hvilken AutoCAD-version DXF-filen bruger ($ACADVER-variablen) eller den enhed, der bruges til at måle vinkler i filen ($AUNITS-variablen)
|Klasser|Sektionen KLASSER indeholder oplysningerne for applikationsdefinerede klasser, hvis forekomster vises i sektionerne BLOKKE, ENTITIES og OBJECTS i databasen.
|Tabeller|Dette afsnit indeholder definitioner for flere forskellige tabeller, som hver indeholder en række forskellige symbolindgange. For eksempel definerer tabellen [line type](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) (LTYPE) mønstret af tankestreger, prikker, tekst og symboler i DXF-filen, og hvordan de skaleres. Her er en komplet liste over tabeller fundet i dette afsnit:<ul><li> Application ID (APPID) tabel</li><li> Block Record (BLOCK_RECORD) tabel</li><li> Dimension Style (DIMSTYPE) tabel</li><li> Lag (LAYER) tabel</li><li> Linjetype (LTYPE) tabel</li><li> Tekststil (STYLE) tabel</li><li> Brugerkoordinatsystem (UCS) tabel</li><li> Se (VIS) tabel</li><li> Viewport-konfigurationstabel (VPORT).</li></ul>
|Blokker|Dette afsnit indeholder de grafiske objekter og tegningsenheder, der udgør hver blokreference i tegningen.
|Entiteter|Dette afsnit indeholder de faktiske objektdata og grafiske enheder i tegningen. Dette kan omfatte rådata - for eksempel er en cirkelentitet defineret af dens tykkelse, midtpunktet, dens radius og ekstruderingsretning.
|Objekter|Her finder du de ikke-grafiske dele af tegningen. For eksempel er AutoCAD-ordbøger gemt her.

## Referencer ##

* [DXF File Specifications](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF af Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)



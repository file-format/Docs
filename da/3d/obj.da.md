{
  "date": "2019-10-11",
  "keywords": [
"obj fil",
"obj filformat",
"hvad er en obj fil",
"fil",
"obj eksempel",
"obj filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBJ filformat",
  "description": "Lær om OBJ-filformat og API'er, der kan åbne og oprette OBJ-filer.",
  "linktitle": "OBJ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ob-daj"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en OBJ-fil?

**OBJ**-filer bruges af Wavefronts Advanced Visualizer-applikation til at definere og gemme de geometriske objekter. Frem- og tilbagetransmission af geometriske data er muliggjort gennem OBJ-filer. Både polygonal geometri som punkter, linjer, teksturspidser, flader og friformsgeometri (kurver og overflader) understøttes af OBJ-format. Dette format understøtter ikke animation eller information relateret til lys og placering af scener.

En OBJ-fil er normalt et slutprodukt af 3D-modelleringsprocessen genereret af en CAD (Computer Aided Design). Standardrækkefølgen til at gemme hjørner er mod uret, hvilket undgår eksplicit erklæring af ansigtsnormaler. Selvom OBJ-filer erklærer skalaoplysninger i en kommentarlinje, er der endnu ingen enheder blevet erklæret for OBJ-koordinater.

## Historien om 3D OBJ-format

Wavefront Technologies created OBJ file format for its Advanced Visualizer application to store geometric objects and 3D data. Its version 2.11 is superseded by a newly documented version 3. Filformatet er åbent og er blevet implementeret af andre leverandører til deres 3D-grafikapplikation. Wavefront Technologies holdt dette filformat open source og neutralt.

## OBJ filformat

I 3D-objekter er kodning af overfladegeometrien et udfordrende job, som OBJ-filformatet klarede meget godt. Dette format er ret alsidigt, da det giver en række muligheder for at indkode overfladegeometri. Følgende er tre tilladte formater med deres egne fordele og mangler:

### Tessellation med polygonale ansigter

OBJ-filformatet letter brugeren at tesselere en 3D-modeloverflade ved hjælp af simple eller komplekse geometriske former. Til overfladegeometrikodning af en model gemmer en fil hjørnerne og normalen til hver polygon. Selvom tessellering øger modellens grovhed, er det alligevel nødvendigt at finde den korrekte balance mellem størrelsen på en fil og dens udskriftskvalitet.

### Friformskurve

OBJ-filformatet tillader de brugerdefinerede friformede overfladekurver at specificere overfladegeometrien af en model. Da friformskurver er mere komplekse end polygonale flader, da buede linjer med få matematiske parametre bedst kan defineres af friformskurver. Derfor, med færre data sammenlignet med polygonale tesselleringer, bruges friformskurver til at generere en højkvalitetskodning af enhver 3D-model uden at udvide filstørrelsen.

### Fritformede overflader

OBJ-filformatet specificerer også fliselægningen af overfladegeometri med friformede overfladepletter. Denne form for freeform-overfladelapper (NURBS) er meget velegnet til overflader uden stive radiale dimensioner, som f.eks. en lastbils karosseri, helikopterens vinger eller en båds skrog. Brug af friformede overflader er meget fordelagtige, da de er mere præcise for at holde filstørrelser mindre med højere præcision. Disse overflader er en væsentlig del af rumfarts- og bilindustrien, hvor den lave præcision er utilgivelig.

Følgende nøgleord er arrangeret efter datatype for at definere overfladegeometri.


|Elementer|Udsagn om friformskurve/overfladelegeme|Friformskurve/overfladeattributter
---|---|---|
|p|Punkt|parm|Parameterværdier|deg|Grader
|l|Line|trim|Ydre trimningsløkke|bmat|Basismatrix
|f|Face|hul|Indre trimmeløkke|trin|Trinstørrelse
|kurv|Kurve|scrv|Specialkurve|cstype|Kurve- eller overfladetype
|curv2|2D curve|sp|Special point|**Forbindelse og gruppering af overflader**
|surf|Surface|end|End statement|con|connect
|**Vis/gengiv attributter**|g|Gruppenavn
|fasning|skråinterpolation|shadow_obj|Skyggestøbning|s|udjævningsgruppe
|lod|Detaljeniveau|trace_obj|Ray tracing|mg|Fletningsgruppe
|d_interp|Opløs interpolation|ctech|Kurvetilnærmelsesteknik|o|Objektnavn
|c_interp|Farveinterpolation|stech|Overfladetilnærmelsesteknik|
|usemtl|Materialenavn|mtllib|Materialebibliotek|
|**Geometriske hjørner**|
|v|Geometriske hjørner|vn|Højdenormaler|
|vt|Tekstur-hjørnepunkter|vp|Parameterrum-hjørner|

### Farve og tekstur

OBJ-filen tillader farve- og teksturinformation at gemme i et tilknyttet filformat kaldet Material Template Library (MTL). Multifarvede geometriske modeller gengives ved at bruge disse to filer sammen. MTL-filer er ASCII-baserede og letter computergengivelse ved at beskrive lysreflekterende egenskaber af en overflade ved hjælp af modellen for Phong-reflektion. Standarden er blevet vedtaget af et stort antal softwareleverandører, som benytter sig af udveksling af materialer. MTL-formatet er lidt forældet for ikke at have understøttelse i de nyeste teknologier såsom spejlende og parallaksekort.

## Referencer

* [Wavefront .obj-fil](https://en.wikipedia.org/wiki/Wavefront_.obj_file)



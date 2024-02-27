{
  "date": "2021-01-22",
  "keywords": [
"ASE",
"fil",
"format",
"filtype",
"udvidelse",
"hvad er en ASE fil?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om ASE-filformat og API'er, der kan åbne og oprette ASE-filer.",
  "title": "ASE - Autodesk ASCII Scene Export File",
  "linktitle": "ASE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-as-dae"
}
},
  "lastmod": "2021-01-22"
}

## Hvad er en ASE fil?

A file with a .ase extension is an Autodesk ASCII Scene Export file format that is an ASCII representation of a scene, containing 2D or 3D information while exporting scene data using Autodesk. Autodesk provides options to include scene components while exporting scene data. You can include Mesh definition along with vertex and face information, Material description, transform animation data for the objects, complete mesh definition of every n frames, animation data for cameras and lights and IK joint settings.

## ASE-filformat - flere oplysninger

ASE-filer er tekstfiler, der er gemt i ASCII-format, som kan åbnes i enhver teksteditor. En ASE-fil kan indeholde følgende typer oplysninger leveret af Autodesk.

### Outputindstillinger

 * Mesh Definition - Eksporterer definitionen af hver maske, inklusive top- og ansigtsoplysninger for geometriske objekter. Derudover aktiveres elementerne i gruppeboksen Mesh Options, beskrevet nedenfor, ved at slå dette til.
 * `Materials` - Includes the material description. If a material is not assigned to an object, its wireframe color is exported. All levels of a material tree are included, so this can produce a lot of text.
 * `Transform Animation Keys` - Indeholder transformationsanimationsdata for objekterne. Hvis objektet er et målkamera eller spotlight, vil dette inkludere målanimationsdata.
 * `Animeret mesh` - Eksporterer en komplet mesh-definition af hver n frames. Frekvensen er specificeret af Controller Output spinneren, beskrevet nedenfor. Hver blok indeholder de samme oplysninger, der er angivet i gruppeboksen Mesh Options, beskrevet nedenfor. Aktivering af dette kan resultere i en enorm fil, selv for små scener.
 * `Animerede kamera/lysindstillinger` - Eksporterer animationsdata for kameraer og lys, såsom farve, intensitet, fald, kortbias og så videre. Udsender en blok for hver n frames, som specificeret af Controller Output-spinneren.
 * `Inverse kinematiske samlinger` - Eksporterer IK-ledsindstillingerne i hierarkigrenen.

### Objekttyper

Elementerne her lader dig angive, hvilken kategori af objekter, du ønsker inkluderet i outputtet. Du kan inkludere geometriske objekter, former, kameraer, lys og hjælpeobjekter.

 * Geometrisk
 * Former
 * Kameraer
 * Lys
 * Hjælpere

### Mesh-indstillinger

 * Mesh Normals - Eksporterer ansigts- og topnormalerne. Ansigtets normal er angivet først, efterfulgt af normalerne af de tre spidser, der understøtter ansigtet. Aktivering af dette resulterer i en meget større fil.
 * `Mapping Coordinates` - Eksporterer en liste over kortlægningspunkter og ansigter i henhold til TVert- og TVFace-strukturerne beskrevet i 3ds Max Software Development Kit. Hvis et objekt bruger ansigtsmapping, eksporteres en ansigtskortliste indeholdende UVW-koordinater for hvert ansigt.
 * `Vertex Colors` - Eksporterer toppunktsfarver.

### Controller-output

 * `Brug nøgler` - Eksporterer nøgleværdier. Hvis controlleren ikke bruger nøgler, bruges Force Sample-metoden. I tilfælde af transformationscontrollere virker indstillingen Brug nøgler kun, hvis alle transformationscontrollere enten er lineære/TCB eller Bezier. Hvis et af transformationssporene bruger en anden type controller, bruges Force Sample-metoden for alle transformationsspor.
 * `Force Samples` - Samples controllerværdier baseret på den frekvens, der er angivet i Frames pr. Sample Controller.

## Referencer

 * [Autodesk - Eksporterer til ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)


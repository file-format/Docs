{
  "date": "2019-11-25",
  "keywords": [
"jpm fil",
"jpm filformat",
"hvad er en jpm-fil",
"fil",
"jpm eksempel",
"jpm filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPM - JPEG 2000 sammensat filformat",
  "description": "Lær om JPM filformat og API'er, der kan oprette og åbne JPM filer.",
  "linktitle": "JPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-dam"
}
},
  "lastmod": "2021-02-08"
}

## Hvad er JPM fil?

JPM refererer til JPEG 2000 billedkodningssystem del 6, som bruges til dokumentafbildning. Den er baseret på Mixed Raster Content Standard (ISO/IEC 16485) og indeholder lagdelte stillbilleder, der bruger JPEG 2000 og andre kodninger. Ud over dets egne specifikationer, arver JPM-filformatet funktioner fra dets overordnede, dvs. filformatet [jp2](/image/jp2/).

## JPM filformat

JPM-filformatet er defineret af [ISO/IEC 15444-6:2003](https://www.iso.org/standard/61124.html) -- JPEG 2000 billedkodningssystemet -- Del 6: Sammensat billedfilformat. Et sammensat billede kan indeholde scannede billeder, syntetiske billeder eller begge dele, hvilket kræver en blanding af kontinuerlig tone og to-niveau komprimeringsmetoder. JPM-filformatet definerer en kompositionsmodel, der beskriver metoden til at kombinere flere billeder for at generere et sammensat billede ved hjælp af multi-layer Mixed Raster Content (MRC)-billeddannelsesmodellen, defineret i ITU-T T.44 | ISO/IEC 16485.

### JPM-specifikationer
JPM-filformatstandarden angiver, at det er en binær beholder til at repræsentere et sammensat billede, hvorved flere billeder kan kombineres til et enkelt billede. Det sætter mekanismen til at gruppere flere billeder i et hierarki af layoutobjekter, sider og sidesamlinger for at gemme JPEG 2000 og andre komprimerede billeddataformater. Formatet inkluderer mekanismen til at inkorporere metadata (ofte omtalt som strukturelle metadata i digitale biblioteksprojekter).

## Referencer

 * [ITU-T Rec. T.805](https://www.itu.int/rec/T-REC-T.805/da)
 * [ISO/IEC 15444-6:2013](https://www.iso.org/standard/61124.html)
 * [Wikipedia:JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000)


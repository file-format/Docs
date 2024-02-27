{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BIF-fil - Ventana Whole Slide Image Format",
  "description":"Lær om BIF-filformat og API'er, der kan oprette og åbne BIF-filer.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-da",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Hvad er en BIF fil?

En BIF-fil er en rasterbilledfil, der indeholder objektglasbilledet. Det består af flere TIFF-billeder, der kombineres af diasvisningsapplikationer til et enkelt sammensat billede. BIF-filer er oprettet af Ventana Medical systems digital diasscanner og er fuldt ud kompatible med BigTIFF-varianten af [TIFF](/image/tiff/) v 6.0-definitionen.

## BIF filformat

En BIF-fil gemmes som en binær billedfil og består af så mange som 200.000 x 200.000 pixels. Dette kan føre til store filstørrelser, hvilket bryder størrelsesgrænsen på 4 GB, som er pålagt af 32-bit filpegepinde defineret af TIF-standarden. Med 64-bit filpointere overvindes denne filstørrelsesbarriere dog af BigTIFF-varianten af TIFF-standarden.

### Hvem bruger BIF-fil?

BIF-filer bruges af digitale diasscannere til at scanne og oprette digitale kopier af diasprøver. Hvis du er patolog, kan du åbne disse BIF-filer i applikationer til diasvisning. Med et højt niveau af detaljer og høj opløsningsdata kan du zoome ind og ud på et diasbillede for at se prøveudsnit i mere eller mindre detaljer. Metadatafilen [XML](/web/xml/), der findes i disse filer, definerer, hvordan billederne skal kombineres, og det billede, der skal bruges som filens thumbnail.

## Hvordan åbner jeg filen BIF?

Du kan åbne BIF filer med:

 * OpenSlide (på tværs af platforme)
 * ImageJ (på tværs af platforme)
 * NetScope Viewer (Windows)

## Referencer ##

 * [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)


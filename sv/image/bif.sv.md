{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BIF-fil - Ventana Whole Slide Image Format",
  "description":"Läs mer om BIF-filformat och API:er som kan skapa och öppna BIF-filer.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Vad är en BIF fil?

En BIF-fil är en rasterbildsfil som innehåller objektglasbilden. Den består av flera TIFF-bilder som kombineras av bildvisningsprogram till en enda sammansatt bild. BIF-filer skapas av Ventana Medical systems digitala diabildskanner och är helt kompatibla med BigTIFF-varianten av [TIFF](/sv/image/tiff/) v 6.0-definitionen.

## BIF filformat

En BIF-fil sparas som en binär bildfil och består av så många som 200 000 x 200 000 pixlar. Detta kan leda till stora filstorlekar, vilket bryter mot storleksgränsen på 4 GB som anges av 32-bitars filpekare som definieras av TIF-standarden. Med 64-bitars filpekare övervinns dock denna filstorleksbarriär av BigTIFF-varianten av TIFF-standarden.

### Vem använder BIF-fil?

BIF-filer används av digitala objektglasskannrar för att skanna och skapa digitala kopior av objektglasprover. Om du är patolog kan du öppna dessa BIF-filer i applikationer för bildvisning. Med stor detaljnivå och högupplösta data kan du zooma in och ut på en diabild för att se provavsnitt i mer eller mindre detaljer. Metadatafilen [XML](/sv/web/xml/) som finns i dessa filer definierar hur bilderna ska kombineras och vilken bild som ska användas som filens miniatyrbild.

## Hur öppnar man filen BIF?

Du kan öppna BIF filer med:

* OpenSlide (plattformsoberoende)
* ImageJ (plattformsoberoende)
* NetScope Viewer (Windows)

## Referenser ##

* [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)


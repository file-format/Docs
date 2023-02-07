{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo BIF - Formato de imagen de diapositiva completa de Ventana",
  "description":"Obtenga más información sobre el formato de archivo BIF y las API que pueden crear y abrir archivos BIF",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## ¿Qué es un archivo BIF?

Un archivo BIF es un archivo de imagen de trama que contiene la imagen del espécimen del portaobjetos. Consiste en múltiples imágenes TIFF que se combinan mediante aplicaciones de visualización de diapositivas en una sola imagen compuesta. Los archivos BIF son creados por el escáner de portaobjetos digital de los sistemas de Ventana Medical y son totalmente compatibles con la variante BigTIFF de la definición [TIFF](/es/image/tiff/) v 6.0.

## Formato de archivo BIF

Un archivo BIF se guarda como un archivo de imagen binario y consta de hasta 200 000 x 200 000 píxeles. Esto puede dar lugar a archivos de gran tamaño, rompiendo el límite de tamaño de 4 GB impuesto por los punteros de archivo de 32 bits definidos por el estándar TIF. Sin embargo, con punteros de archivo de 64 bits, esta barrera del tamaño de archivo se supera con la variante BigTIFF del estándar TIFF.

### ¿Quién usa el archivo BIF?

Los escáneres de portaobjetos digitales utilizan archivos BIF para escanear y crear copias digitales de muestras de portaobjetos. Si es patólogo, puede abrir estos archivos BIF en aplicaciones de visualización de diapositivas. Con un gran nivel de detalles y datos de alta resolución, puede acercar y alejar una imagen de diapositiva para ver secciones de muestras con más o menos detalles. El archivo de metadatos [XML](/es/web/xml/) presente en estos archivos define cómo se deben combinar las imágenes y la imagen que se debe usar como miniatura del archivo.

## ¿Cómo abrir un archivo BIF?

Puede abrir archivos BIF con:

* OpenSlide (multiplataforma)
* ImageJ (multiplataforma)
* Visor de NetScope (Windows)

## Referencias ##

* [Documento técnico BIF de patología digital de Roche](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)


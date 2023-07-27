{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo MP - Archivo LaTeX MetaPost",
  "description":"Obtenga información sobre el formato de archivo MP y las API que pueden crear y abrir archivos MP",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## ¿Qué es un archivo MP?

Un archivo MP es un archivo de imagen vectorial generado por el lenguaje de programación MetaPost para crear imágenes. Las imágenes vectoriales creadas con el formato de archivo MP se guardan como archivos [EPS](/es/page-description-language/eps/) (PostScript encapsulado). Además, MetaPost se distribuye con los marcos TeX y Metafont y se pueden generar archivos MP desde los archivos TEX y LTX utilizados por estas aplicaciones. Los archivos MP contienen instrucciones de dibujo y dibujos algorítmicos matemáticos para representar el archivo EPS de salida. El motor PDFTex puede usar el EPS creado para generar archivos [PDF](/es/pdf/) directamente.

## Formato de archivo MP

Los archivos MP se guardan en el disco como archivos binarios y generan salida EPS cuando se exportan al formato de archivo de imagen vectorial de salida. Los dibujos creados con MetaPost se incluyen en forma formateada dentro de documentos técnicos y publicaciones de revistas creadas con LaTex.

### Ejemplo de archivo MetaPost MP

El siguiente es un ejemplo, al que se hace referencia en [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), que contiene una flecha y la letra "A" justo encima de la mitad de la flecha.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Referencias ##

* [MetaPost de Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Metapost de muestra de látex de Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)


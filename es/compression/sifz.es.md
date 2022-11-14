{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo SIFZ: archivo de proyecto comprimido de Synfig Studio",
  "description":"Obtenga información sobre el formato de archivo SIFZ y las API que pueden crear y abrir archivos SIFZ",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## ¿Qué es un archivo SIFZ?

Un archivo SIFZ es un archivo SIF comprimido con gzip creado por la aplicación de creación de animaciones 2D de código abierto **Synfig Studio**. Contiene múltiples elementos gráficos que compensan la animación. El contenido general de la animación se crea mediante una combinación de un lienzo que se rellena con formas, trazos de pincel o lápiz y texto. Todos estos están dispuestos en sus propias posiciones, radio, tangente, ángulo, vértice y asas de ancho. Los archivos SIFZ se pueden abrir con [Synfig Studio](https://www.synfig.org/).

## Formato de archivo SIFZ

Los archivos SIFZ son archivos comprimidos [ZIP](/es/compression/zip/) que se empaquetan con el método de compresión gzip. Synfig se utiliza para crear animaciones con calidad de película utilizando ilustraciones vectoriales y de mapa de bits. A diferencia del antiguo método de creación de animaciones fotograma a fotograma, te permite producir animaciones 2D de mayor calidad con menos recursos.

Los archivos SIFZ, al estar comprimidos, son más pequeños que los archivos SIF sin comprimir. Esto también facilita la transferencia a través de conexiones a Internet de bajo ancho de banda.

## Referencias

* [Código abierto Synfig - Github](https://github.com/synfig/synfig/)
* [Documentación Synfig](https://synfig.readthedocs.io/en/latest/index.html)


{
  "date" : "2019-10-11",
  "keywords" :[ "archivo gbr", "formato de archivo gbr", "qué es un archivo gbr", "archivo", "ejemplo gbr", "extensión de archivo gbr","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo GBR - Formato de archivo Gerber para PCB",
  "description":"Obtenga información sobre el formato de archivo GBR y las API que pueden crear y abrir archivos GBR",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo GBR?

Un archivo con extensión .gbr es un formato de archivo de imagen Gerber para el intercambio de transferencia de datos de diseño de placa de circuito impreso (PCB). Fue desarrollado por Ucamco. Los datos de diseño de PCB son el componente principal requerido por la industria de fabricación para su manipulación. Un archivo GRB contiene datos de PCB, como capas de cobre, máscara de soldadura, leyenda y datos de perforación y ruta. Se puede utilizar para transferir datos como las características de fabricación de PCB, incluido el grosor o el acabado, en un formato estandarizado. Todos los sistemas de diseño de PCB generan archivos Gerber que pueden ser manejados por los sistemas de fabricación de PCB. Los archivos GBR ahora se han convertido en el estándar de facto para la transferencia de datos de diseño de placa de circuito impreso (PCB). Ucamco ha proporcionado un [visor en línea gratuito](https://gerber-viewer.ucamco.com/) para abrir y ver formatos de archivo GBR.

## Formato de archivo GBR

GBR es un formato legible por humanos UTF-8 que consta de solo 27 comandos. Debido a esta breve lista de comandos y su tamaño compacto, GBR es fácil de depurar. Gerber en esencia es un formato vectorial abierto para imágenes binarias 2D. La metainformación se transfiere con las imágenes a través de Atributos. Un solo archivo GRB especifica una sola imagen y no requiere que se interpreten archivos adjuntos o parámetros externos. Una imagen necesita un solo archivo. Utiliza caracteres ASCII de 7 bits para todos los comandos y nombres definidos en la especificación que se pueden imprimir. Esto cubre completamente la generación completa de imágenes.

### Ejemplo de archivo GBR

A continuación se muestra un archivo Gerber de ejemplo que crea un círculo de 1,5 mm de diámetro centrado en el origen. Hay un comando por línea.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Referencias

* [Formato Gerber](https://www.ucamco.com/en/gerber)


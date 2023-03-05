{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo DDS: archivo de imagen de superficie de DirectDraw",
  "description":"Obtenga información sobre el formato de archivo DDS y las API que pueden crear y abrir archivos DDS",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## ¿Qué es un archivo DDS?

Un archivo DDS es un archivo de imagen ráster que utiliza el formato de contenedor DirectDraw Surface (DDS). Almacena texturas sin comprimir y comprimidas (DXTn) e implementa diferentes tipos para almacenar diferentes tipos de datos. También admite varios tipos diferentes de datos, como texturas de una sola capa, texturas con mipmaps, mapas de cubos, mapas de volumen y matrices de texturas. Esto permite que los archivos DDS almacenen modelos de unidades de textura de videojuegos además de fotos digitales y fondos de escritorio de Windows. El formato de archivo DDS fue desarrollado por Microsoft para usarse con DirectX SDK.

## Formato de archivo DDS

Los archivos DDS se guardan como archivos binarios y se pueden usar con DirectX SDK. Utiliza el poder de DirectX para desarrollar aplicaciones de renderizado en tiempo real, como juegos 3D.

Diseño de archivo ### DDS

Microsoft ha documentado en detalle el [diseño del archivo DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout). Un archivo DDS binario contiene la siguiente información.

* Un DWORD (número mágico) que contiene el valor del código de cuatro caracteres 'DDS' (0x20534444).
* Una descripción de los datos en el archivo.

DDS_HEADER describe los datos y DDS_PIXELFORMAT describe el formato de píxel. Ambos reemplazan las estructuras obsoletas DDSURFACEDESC2, DDSCAPS2 y DDPIXELFORMAT DirectDraw 7.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

La [guía de programación del formato de archivo DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) elabora más detalles técnicos de este formato de archivo.

## Referencias

* [DDS - Por Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Manual de referencia técnica del formato de archivo PCX de ZSoft](http://qzx.com/pc-gpe/pcx.txt)


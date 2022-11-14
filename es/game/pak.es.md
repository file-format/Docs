{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "formato de archivo", "qué es un archivo pak", "archivo", "ejemplo de paquete", "Archivo de paquete de videojuegos","extensión"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el archivo .pak y las API que pueden crear y abrir archivos PAK",
  "title" :"Formato de archivo PAK: archivo de paquete de videojuegos",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## ¿Qué es un archivo PAK?

Un archivo PAK es un archivo de paquete creado por diferentes videojuegos para archivar datos del juego. Esencialmente, es un formato de archivo de juego. Esto puede incluir varios elementos del juego, como gráficos, texturas, sonidos, objetos y otros datos del juego. El archivo se guarda principalmente como un archivo .zip y se puede extraer con un software de descompresión popular como WinZip y WinRAR. Los ejemplos de videojuegos que usan archivos PAK incluyen Quake, Hexen, Crysis y Half-Life.

## Formato de archivo PAK - Más información

En la mayoría de los casos, los archivos PAK se guardan en [formato de archivo ZIP](/es/compression/zip/). Pero diferentes aplicaciones pueden usar diferentes formatos de archivo para almacenar estos archivos.


## ¿Cómo abrir archivos PAK?

Puede abrir archivos PAK con aplicaciones como [PakExplorer](https://www.quaketerminus.com/tools.shtml) y [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- -----------------------**

## Formato de archivo PAK: archivo de objeto Simutrans

Un archivo con extensión .pak es un formato de archivo de juego de simulación de transporte de [Simutrans](https://www.simutrans.com/en/). Contiene objetos utilizados en la simulación, como gráficos y contenidos de datos creados por el usuario. Puede tener varios objetos diferentes, como vehículos de juego, edificios, terreno, etc. Los archivos PAK se generan utilizando MakeObject, una utilidad que compila archivos .dat e imágenes .png para crear estos objetos de simulación. Simutrans permite a los jugadores ejecutar un sistema de transporte exitoso al construir y administrar sistemas de transporte para pasajeros, correo y mercancías por tierra.

## ¿Cómo crear archivos PAK?

Simutrans ha enumerado ejemplos de muestra para crear archivos PAK en los sistemas operativos Windows y Linux.

### sistema operativo Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Sistema operativo Linux

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Referencias

* https://simutrans-alemania.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans


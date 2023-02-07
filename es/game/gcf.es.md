{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo GCF y las API que pueden crear y abrir archivos GCF",
  "title" :"Archivo GCF - Formato GCF del juego Nadeo",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## ¿Qué es un archivo GCF?

Un archivo .gcf es un archivo de caché de juego utilizado por la plataforma de juegos Steam. Contiene datos del juego, como texturas, modelos y otros archivos que utiliza el juego. Estos archivos se almacenan en la computadora del usuario y se utilizan para reducir la cantidad de datos que deben descargarse al actualizar o instalar un juego. Los archivos .gcf también se pueden usar para crear copias de seguridad de la instalación de un juego o para transferir un juego entre computadoras.

Los archivos GCF se pueden leer y escribir con la biblioteca de programación C++ de código abierto, [HLLib]((https://developer.valvesoftware.com/wiki/HLLib)).

## Formato de archivo GCF

Los archivos GCF se guardan en el disco como archivos binarios. GCF se usó originalmente como un acrónimo de Grid Cache File (el primer nombre en clave de Steam era Grid), pero más tarde se tomó como Game Cache File. Un archivo GCF es un archivo de almacenamiento que almacena juegos de Steam. Todo el contenido oficial se descarga como archivos GCF. Los archivos GCF también se pueden compartir entre juegos.

NOTA: GCF es el predecesor del [formato de archivo VPK](/es/game/vpk/).
## Referencias

* [Software de válvula](https://www.valvesoftware.com/en/)
* [Formato de archivo GCF](https://developer.valvesoftware.com/wiki/GCF)
* [HLLib - Biblioteca de programación C++ de código abierto para leer archivos GCF](https://developer.valvesoftware.com/wiki/HLLib)


{
  "date" : "2021-09-08",
  "keywords" :[ "archivo pcc", "formato de archivo pcc", "qué es un archivo pcc", "archivo", "ejemplo de pcc", "extensión de archivo pcc","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo PCC de Mass Effect y las API que pueden crear y abrir archivos PCC",
  "title" :"PCC - Archivo de paquete de efectos masivos",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## ¿Qué es un archivo PCC?

Un archivo con extensión .pcc es un archivo de [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) que contiene datos del juego para modificar el contenido del juego, como modelos, texturas y habitaciones. Mass Effect 2 y 3 son los primeros juegos de disparos basados en el motor de juego Unreal Engine 3. El juego fue desarrollado inicialmente por [Bioware](https://www.bioware.com/about/) que mantuvo la mayoría de los recursos del juego en su formato de archivo PCC patentado. Bioware fue adquirida por Electronic Arts, una editorial de entretenimiento interactivo líder a nivel mundial.

## Formato de archivo PCC: más información

Los archivos PCC contienen estructuras comprimidas y/o sin comprimir que contribuyen a la organización general del archivo.

### Estructura PCC comprimida

Un archivo PCC comprimido se compone de tablas y datos que se segmentan en fragmentos. Cada fragmento contiene un número variable de bloques comprimidos.

* `Encabezado de fragmentos`: un encabezado común de 16 bytes que contiene información sobre los fragmentos.
* `Encabezado de fragmento`: un encabezado de 16 bytes que contiene información sobre los datos comprimidos sin procesar contenidos en el formulario de bloque.

### Estructura PCC sin comprimir

Los archivos PCC sin comprimir se dividen en las siguientes cinco partes.

* `Header`: contiene información básica sobre la estructura del archivo PCC.
* `Tabla de nombres`: contiene el nombre que se encuentra dentro del paquete, incluidas las clases de importación, las exportaciones y las propiedades de exportación.
* `Importar tabla`: contiene todas las clases y objetos importados por el PCC.
* `Exportar tabla`: contiene todos los objetos almacenados en el paquete. Cada exportación puede variar en tamaño.

## Referencias

* [Me3Explorer - Formato de archivo PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Juego Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)


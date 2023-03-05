{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - Archivo de paquete de instalación multiplataforma",
  "description":"Obtenga información sobre el formato de archivo XPI y las API que pueden crear y abrir archivos XPI",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## ¿Qué es un archivo XPI?

Un archivo XPI es un archivo de instalación que se comprime para reducir el tamaño del archivo. Las aplicaciones de Mozilla lo utilizan para la instalación de complementos y archivos complementarios. Contiene un script de instalación o un manifiesto en la raíz del archivo junto con varios archivos de datos. Un archivo XPI puede contener temas, herramientas o complementos de Firefox que el usuario puede instalar para formar parte del navegador Firefox, Thunderbird o SeaMonkey.

## Formato de archivo XPI - Más información

Los archivos XPI se guardan en el disco como archivos comprimidos [ZIP](/es/compression/zip/) que combinan varios archivos en un único archivo comprimido. Los archivos dentro de un archivo XPI pueden incluir un archivo de script de instalación como JS y archivos web como [CSS](/es/web/css/), [HTML](/es/web/html/) y [JSON](/es/web/json/ ). A veces, también puede contener archivos de imagen [PNG](/es/image/png/) para que los complementos los utilicen como íconos.

### ¿Cómo ver el contenido del archivo XPI?

Un archivo XPI es prácticamente un archivo ZIP cuyo contenido se puede ver siguiendo los siguientes pasos.

* Cambiar la extensión del archivo de XPI a ZIP
* Extraiga el contenido del archivo con cualquier utilidad de descompresión estándar, como WinZip (Windows, Mac), 7-Zip (Windows) o Apple Archive Utility (Mac).

### Instalar archivo XPI en Firefox Android

La mayoría de las personas sienten curiosidad por saber si los archivos XPI se pueden instalar en Firefox en dispositivos Android. En Android, puede instalar el complemento desde un archivo XPI localizando el archivo y abriéndolo con Firefox.

## Referencias

* [Instalación XP - Wikipedia](https://en.wikipedia.org/wiki/Instalación XP)
* [¿Cómo puedo abrir una extensión de archivo XPI?](https://support.mozilla.org/en-US/questions/1009049)


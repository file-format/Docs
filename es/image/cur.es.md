{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "extensión", "archivo", "formato", "imagen", "Mapa de bits independiente del dispositivo", "Formato de archivo del cursor", "Cursor", "Windows", "aplicación" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Formato de archivo de cursor",
  "description":"Obtenga información sobre el formato de archivo CUR y las API que pueden crear y abrir archivos CUR",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## ¿Qué es un archivo CUR? ##

Un archivo CUR es un formato de archivo de cursor estático de Microsoft Windows. Básicamente, son imágenes estacionarias idénticas a los archivos ICO (icono) en todos los sentidos, excepto en la extensión. Tanto CUR como [ICO](/es/image/ico/) se establecen sobre la base de la especificación de mapa de bits independiente del dispositivo [DIB](/es/image/dib/) (mapa de bits independiente del dispositivo). El cursor predeterminado, así como el personalizado, como el puntero del mouse de Windows para el sistema operativo Windows, se almacenan en archivos CUR. Puede ser una flecha para el uso normal, un reloj de arena giratorio para demostrar los períodos de espera o una barra I para la edición de texto. Los archivos CUR vienen con el paquete de instalación de los temas de escritorio personalizados para garantizar que el cursor de Windows coincida con el tema de escritorio personalizado.

## Especificación técnica ##

Los archivos CUR son archivos de sistema binario que se pueden encontrar en dispositivos que funcionan con el sistema operativo Microsoft Windows. Las imágenes de puntero CUR vienen en diferentes tamaños estándar como 16 × 16, 32 × 32, etc. Los archivos CUR son muy similares a los archivos ICO; ambos consisten en pequeñas imágenes estacionarias. Solo la extensión de los archivos CUR e ICO son diferentes. Además, la explicación de un punto de acceso en el encabezado del archivo CUR es distinta del archivo ICO. El punto de acceso interpreta el desplazamiento de píxeles desde la esquina superior izquierda hasta el lugar donde está apuntando el mouse. Los sistemas de Windows todavía usan los archivos CUR, pero ahora los cursores animados generalmente tienen la extensión de archivo ANI en lugar de CUR.

## Breve historia ##

El archivo CUR se crea a partir del archivo ICO. El primer formato de archivo CUR se incorporó al sistema operativo Windows 1.0 de Microsoft en 1981 para suavizar el uso comercial. Pronto se introdujeron más cursores interactivos que permitían a los usuarios modificar sus preferencias de cursor a partir de las opciones preinstaladas disponibles. Sin embargo, es fácil editar un archivo CUR por su cuenta, incluso si no tiene suficientes conocimientos técnicos.


## CUR Ejemplo ##

Los archivos CUR se pueden encontrar en *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="Formato de archivo CUR" >}}


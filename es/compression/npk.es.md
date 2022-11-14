{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo NPK",
  "description":"Obtenga información sobre el formato de archivo NPK y las API que pueden crear y abrir archivos NPK",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## ¿Qué es un archivo NPK?

Un archivo NPK es un archivo de paquete de actualización de software utilizado por los enrutadores **MikroTik** para actualizar el sistema operativo del enrutador. Viene como un archivo binario comprimido que se carga en el enrutador para instalar actualizaciones de software. La información contenida dentro de un archivo NPK incluye información de red, como dirección IP y servicio IP, información de conectores (interfaces Ethernet y puerto serie), configuración de correo electrónico, configuración de puente y administración de usuarios locales.

## Formato de archivo NPK

Los archivos NPK se almacenan como archivos binarios comprimidos. Es un formato de archivo cerrado que solo utilizan los propios MikroTik. No está destinado a crear complementos de RouterOS a través de terceros. Los archivos NPK son mantenidos por MikroTik y las versiones actualizadas de los mismos se pueden descargar desde las secciones de descarga del sitio web [MikroTik] (https://mikrotik.com/download).

Cuando se carga un archivo NPK en un enrutador, el sistema operativo del enrutador no entra en vigencia a menos que se reinicie. Por lo tanto, se requiere un reinicio para que se actualice el sistema operativo del enrutador.

## Referencias

* [MikroTik - Actualización del sistema operativo del enrutador] (https://mikrotik.com/download)
* [Cómo crear archivos NPK](https://forum.mikrotik.com/viewtopic.php?t=87126)


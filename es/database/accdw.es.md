{
  "date" : "2021-08-30",
  "keywords" :[ "ACCDW", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo ACCDW y las API que pueden crear y abrir archivos ACCDW",
  "title" :"ACCDW - Archivo de enlace de base de datos de Microsoft Access",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-30"
}

## ¿Qué es un archivo ACCDW?

Un archivo con extensión .accdw es un archivo de enlace creado con Microsoft Access y contiene información sobre el enlace para descargar un archivo de base de datos de Access, es decir, [ACCDB](/es/base de datos/accdb/) desde el servidor de SharePoint. Esto permite a los usuarios compartir archivos de bases de datos alojados de forma remota. Al abrir el archivo ACCDW, se descarga el archivo ACCDB vinculado como una copia local en la computadora del usuario. El archivo descargado se guarda en la ubicación de descarga predeterminada y se puede acceder navegando hasta él. Por lo general, estos archivos se descargan y almacenan con el nombre "SiteServer.accdb" que hace referencia a las bases de datos del cliente.

## Formato de archivo ACCDW - Más información

El archivo ACCDW es un archivo XML que proporciona un vínculo al sitio de SharePoint donde se alojan los Servicios de Access. Es solo un acceso directo y requiere conexión a Internet para ejecutarlos. En caso de estar en línea, SharePoint se almacena en caché localmente para brindar la opción de desconectarlo más tarde.

## Referencias

* [Especificaciones de Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Descargando archivo .accdw](https://social.technet.microsoft.com/Forums/en-US/7bf02e9e-6246-44da-9513-4cf8f2cc2fb2/downloaded-accdw-file?forum=sharepointgeneralprevious)
* [¿Qué formato de archivo de Access debo usar?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=en-us&rs=en-us&ad=us)


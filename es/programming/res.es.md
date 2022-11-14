{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - Script de recursos compilado de C++",
  "description":"Obtenga información sobre el formato de archivo RES con el ejemplo de RES y las API que pueden crear y abrir archivos RES",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## ¿Qué es un archivo RES?
El archivo con el sufijo o extensión .res puede pertenecer a muchas categorías de formato de archivo. Aquí estamos discutiendo el formato de archivo RES, que es un script de recursos compilado de C++; un archivo binario creado por Microsoft Resource Compiler (rc) que contiene datos de recursos; basado en el contenido del archivo de definición de recursos; relevante para su proyecto de software principal. El archivo .res generalmente se vuelve a formatear en un archivo de objeto de recurso para vincularlo al archivo ejecutable de una aplicación.

## formato de archivo RES
El formato de archivo RES pertenece a Microsoft Resource Compiler (rc). El compilador de recursos es una herramienta que compila recursos como cursores, íconos, menús y cuadros de diálogo que usa su aplicación. Los archivos de recursos suelen tener una extensión .res; contiene recursos, como cursores, imágenes e información de versión. Un archivo RES puede ser un archivo de recursos de 16 o 32 bits.
## Estructura del archivo de recursos
Un archivo de recursos contiene una serie de varias entradas de recursos. Cada entrada contiene un encabezado de recursos y datos relevantes. Un encabezado de recurso suele estar alineado con DWORD en el archivo y contiene lo siguiente:

- Una **DWORD** para especificar el tamaño del encabezado del recurso
- Una **DWORD** para especificar el tamaño de los datos del recurso
- El tipo de recurso
- El nombre del recurso
- Información de recursos adicionales

La estructura del encabezado del recurso define el formato del archivo RES. Los datos del recurso siguen al encabezado del recurso. Algunos recursos también agregan un patrón de encabezado de grupo específico del recurso para proporcionar información sobre un grupo de recursos. Los siguientes son algunos de los tipos de entradas de recursos y su descripción:

### Recursos de la tabla aceleradora
Una tabla aceleradora es una entrada de recurso en un archivo RES sin un encabezado de grupo. El patrón **ACCELTABLEENTRY** define cada entrada en la tabla del acelerador. Un archivo RES puede tener múltiples tablas aceleradoras.

### Recursos de iconos y cursores
Aunque el sistema considera cada ícono y cursor como un solo archivo, estos se almacenan en archivos RES como un grupo de recursos de íconos o un grupo de recursos de cursor. Los formatos de archivo de los recursos de iconos y cursores son los mismos. Un encabezado de grupo de recursos sigue a todos los componentes individuales del grupo de iconos o cursores en el archivo .res.

### Recursos del cuadro de diálogo
También se realiza un cuadro de diálogo como entrada de recurso en el archivo RES. Contiene un patrón de encabezado de cuadro de diálogo **DLGTEMPLATE** y un patrón **DLGITEMTEMPLATE** para cada control específico del cuadro de diálogo. Los patrones **DLGTEMPLATEEX** y **DLGITEMTEMPLATEEX** explican el formato de los recursos del cuadro de diálogo ampliado.

### Recursos de fuentes
Un recurso de menú contiene un patrón **MENUHEADER** seguido de uno o más patrones **NORMALMENUITEM** o **POPUPMENUITEM**, uno para cada elemento de menú en la plantilla de menú. Los patrones **MENUEX_TEMPLATE_HEADER** y **MENUEX_TEMPLATE_ITEM** explican el formato de los recursos de menú ampliados.

### Recursos de la tabla de mensajes
Una tabla de mensajes consta de texto formateado para mostrar como un mensaje de error o en un cuadro de mensaje. El patrón principal en un recurso de tabla de mensajes es la estructura **MESSAGE_RESOURCE_DATA**.

### Recursos de versión
El patrón principal en un recurso de versión es **VS_FIXEDFILEINFO**. Los patrones adicionales incluyen **VarFileInfo** para almacenar datos relacionados con la información del idioma y **StringFileInfo** para información de cadena personalizada.




## Referencias

* [Formatos de archivo de recursos](https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 




{
  "date" : "2021-06-30",
  "keywords" :[ "archivo mst", "formato de archivo mst", "qué es un archivo mst", "archivo", "ejemplo de mst", "extensión de archivo mst","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo MST y las API que pueden crear y abrir archivos MST",
  "title" :"MST - Archivo de paquete del instalador de Windows",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## ¿Qué es un archivo MST?
Los archivos con extensión .mst se utilizan para transformar el contenido de un paquete MSI. Los administradores de sistemas suelen utilizarlos para aplicar la configuración personalizada a un archivo MSI existente. Los archivos MST se utilizan junto con el paquete MSI original en sus sistemas de distribución de software, como políticas de grupo. Los archivos MST generalmente se usan en el desarrollo y prueba de software para configurar sus versiones en desarrollo del software.

## formato de archivo MST
Un archivo MST o Transform se utiliza para recopilar las opciones de instalación de los programas que utilizan Microsoft Windows Installer en un archivo. Estos archivos se usan comúnmente en la línea de comandos del instalador (MSIEXEC.EXE) o se usan en una política de grupo de instalación de software; en un dominio de Microsoft Active Directory. Los archivos MST también se pueden usar con instaladores ejecutables empaquetados. Un caso general es que alguien quiera pasar parámetros de línea de comando al instalador empaquetado. Para hacerlo, necesita un archivo MST que agregue la propiedad WRAPPED_ARGUMENTS a la tabla de propiedades. Estos archivos no se pueden crear ni editar con editores generales. Hay herramientas específicas disponibles para este propósito.

### ¿Cómo usar archivos MST?
Los archivos MST se pueden generar utilizando varias herramientas y Ocra se usa generalmente para generar archivos MST. Luego, la configuración se puede personalizar según la necesidad y guardarla en una ubicación específica. Después de eso, los archivos MST se pueden usar junto con los archivos MSI. Si desea probar estos archivos; use la siguiente sintaxis en la línea de comando

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMA propiedad

También puede usar la propiedad **TRANSFORMS** del instalador de Windows, que en realidad es una lista de las transformaciones que aplica el instalador al instalar el paquete. El instalador ejecuta las transformaciones en el mismo orden en que aparecen en la propiedad TRANSFORM. Las transformaciones se pueden especificar por nombre de archivo con extensión .mst o ruta completa. Para especificar más de una transformación, separe cada nombre de archivo o un punto y coma como en el siguiente ejemplo.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Referencias

* [Archivos de transformación MST](https://www.exemsi.com/documentation/mst-transformation-files/)
* [propiedad TRANSFORMS](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)



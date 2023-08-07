{
  "date" : "2021-04-08",
  "keywords" :[ "archivo oar", "formato de archivo oar", "qué es un archivo oar", "archivo", "ejemplo oar", "extensión de archivo oar","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR: formato de archivo de archivo de OpenSimulator",
  "description":"Obtenga información sobre el formato de archivo OAR y las API que pueden crear y abrir archivos OAR",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## ¿Qué es un archivo OAR?

Un archivo con extensión .oar es un archivo de almacenamiento utilizado por la aplicación OpenSimulator, que es un servidor de aplicaciones 3D de código abierto para crear un entorno virtual accesible para múltiples usuarios a través de la red. El formato de archivo OAR proporciona los datos de activos necesarios para cargar completamente el terreno, las texturas de los objetos y los inventarios en un sistema diferente. OpenSimulator también tiene una hiperred opcional que permite a los usuarios visitar otras instalaciones de OpenSimulator en la web. Los archivos OAR tienen una aplicación/oar de tipo MIME de Internet y contienen uno o más archivos archivados.


## Formato de archivo OAR

OAR son archivos binarios que se almacenan en formato de archivo comprimido. La última versión del formato de archivo OAR es [versión 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) que tiene cambios importantes con respecto a su anterior [versión 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). La última versión admite el almacenamiento de varias regiones en un solo OAR y no es compatible con versiones anteriores de OpenSimulator anteriores a la 0.7.5. Un archivo OAR es un archivo tar comprimido con gzip (tar.gz) en el formato tar original de Unix (no USTAR).

## Ejemplo de Regiones OAR
Los archivos AOR pueden contener múltiples regiones. La estructura del archivo es la siguiente (este ejemplo contiene 4 regiones):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## Archivo OAR.xml

El archivo de control de archivo contiene un número de versión principal para definir la compatibilidad con futuros cambios de formato. La presencia de activos en formato OAR se indica mediante el elemento booleano<assets_included> . La información sobre las regiones incluidas está contenida en un manifiesto que está presente en el archivo de control. Un ejemplo de Archive.xml es el siguiente.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Referencias

* [Formato OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)


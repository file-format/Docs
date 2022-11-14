{
  "date" : "2019-10-11",
  "keywords" :[ "archivo mpkg", "formato de archivo mpkg", "qué es un archivo mpkg", "archivo", "ejemplo de mpkg", "extensión de archivo mpkg","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo MPKG - Archivo de metapaquete",
  "description":"Obtenga información sobre el formato de archivo MPKG y las API que pueden crear y abrir archivos MPKG",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## ¿Qué es un archivo MPKG?

Un archivo con la extensión .mpkg es un archivo instalador de archivos, que se encuentra principalmente en los sistemas operativos MacOS. Contiene todos los archivos de instalación necesarios de la aplicación sin necesidad de mantener los archivos asociados por separado. Un solo archivo MPKG puede contener archivos de paquete [PKG](/es/compression/pkg/) como uno de los archivos de instalación además de otros archivos. Los archivos MPKG no se pueden abrir con ningún software general y se ejecutan automáticamente en MacOS usando Apple Installer.

## Formato de archivo MPKG

Un archivo MPKG contiene diferentes tipos de archivos que se requieren para la instalación de varios paquetes que contiene. Esto se puede ver en la imagen a continuación, que es la estructura de árbol de un archivo MPKG de muestra. Esta estructura de árbol se exporta usando el comando `tree` en la terminal de MacOS.

{{< figure src="../mpkg.png" alt="Formato de archivo MPKG" >}}

La descripción de los diferentes elementos en la imagen es la siguiente.

`Directorio de paquetes`: almacena una lista de archivos pkg, es decir, una lista de subpaquetes
`Directorio de recursos`: almacena los recursos utilizados por pkg, como recursos e imágenes localizados, documentos Rtf, documentos pdf, etc.
`Distribution.dist file`: un documento xml que contiene información como los subpaquetes que se instalarán y los scripts de tiempo de ejecución

El archivo XML de muestra para un archivo MPKG puede tener el siguiente aspecto según los subpaquetes asociados.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/es/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - es el subpaquete que se instalará. Es un directorio de la estructura Bundle en formato pkg. Contiene un subdirectorio Contenidos.

## Referencias

* [Paquetes planos de OSX] (https://matthew-brett.github.io/docosx/flat_packages.html)
* [Gestor de paquetes C++ MPKG](https://github.com/puellavulnerata/mpkg)


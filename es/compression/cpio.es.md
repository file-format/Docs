{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo CPIO - Formato de archivo CPIO Unix",
  "description":"Aprenda a saber qué es un archivo CPIO y las API que pueden crear y abrir archivos CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## ¿Qué es un archivo CPIO?

Un archivo CPIO es un archivo creado en el formato Copy In Copy Out (CPIO) de Unix. Es similar al formato de archivo TAR, salvo que no está comprimido. Los archivos CPIO pueden almacenar archivos de dispositivos, enlaces simbólicos y atributos de archivos extendidos.

## Formato de archivo CPIO

Un archivo CPIO se crea como un archivo binario que no es legible por humanos. Almacena la colección de archivos y directorios. El contenido de un archivo CPIO se identifica con información de metadatos, como nombres de archivos, permisos, propiedad y marcas de tiempo. Esta información de metadatos también se almacena en el archivo para acceso lateral por parte del sistema.

## Formato del archivo CPIO

Un archivo CPIO se compone de uno o más archivos miembro concatenados. Cada archivo del archivo consta de un encabezado seguido opcionalmente del contenido del archivo como se menciona en el encabezado. El archivo contiene otro encabezado al final que se describe mediante un archivo vacío llamado TRAILER!!.

### Tipos de archivos CPIO

Hay dos tipos de archivos CPIO. Estos se diferencian sólo en el estilo del encabezado.

* Archivos ASCII: estos archivos CPIO tienen un encabezado imprimible que pasa a formar parte del archivo CPIO si el archivo en sí consta de archivos ASCII.
* Archivos binarios: estos archivos CPIO tienen encabezados binarios.

## Trabajar con el archivo CPIO

### ¿Cómo crear archivos CPIO?

Puede crear un CPIO en sistemas tipo Unix usando el comando **cpio**. El siguiente comando encontrará todos los archivos y directorios en el directorio actual y sus subdirectorios. Luego, esta salida se canaliza al comando cpio que generará un nuevo archivo CPIO llamado archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### ¿Cómo extraer archivos de archivos CPIO?

El siguiente comando extrae los archivos de un archivo existente.

```
cpio -id < archive_cpio.cpio
```
Leerá el archivo archive.cpio de la entrada estándar y extraerá los archivos al directorio actual.


## Referencias

* [CPIO - Por Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [Formato de archivo CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)


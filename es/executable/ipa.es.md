{
  "date" : "2021-08-30",
  "keywords" :[ "archivo ipa", "formato de archivo ipa", "qué es un archivo ipa", "archivo", "ejemplo de ipa", "extensión de archivo ipa","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo IPA y las API que pueden crear y abrir archivos IPA",
  "title" :"IPA - Archivo de paquete de aplicación iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## ¿Qué es un archivo IPA?
Un archivo con extensión .ipa pertenece a iOS y se conoce como archivo de paquete de aplicación. Este es un archivo (comprimido con compresión [ZIP](/es/compression/zip/)) que almacena una aplicación iOS, pero esa aplicación solo se puede instalar en dispositivos iOS o MacOS basados en ARM, como un iPad, iPhone o iPod Touch. Principalmente, se puede usar iTunes, Apple Configurator 2 o cualquier software de terceros para instalar archivos IPA.

## formato de archivo IPA
Los desarrolladores de IOS que están desarrollando las aplicaciones utilizando Apple Xcode están muy familiarizados con los archivos IPA porque necesitan empaquetar sus aplicaciones desarrolladas como archivos IPA para probar o implementar la tienda de aplicaciones. Aunque se sabe que los archivos IPA se instalan como aplicaciones de iOS, también puede descomprimirlos para ver los datos de la aplicación que contienen. Dado que un archivo IPA contiene solo un binario para la arquitectura ARM de los teléfonos móviles y no contiene un binario para la arquitectura x86, muchos archivos .ipa no se pueden instalar en el simulador de iPhone.
### Estructura de un archivo .ipa
El siguiente ejemplo muestra la estructura de un IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Lo anterior es una estructura integrada para que iTunes y App Store la reconozcan. Según esta estructura:
- El directorio Payload contiene todos los datos de la aplicación.
- El archivo iTunes Artwork es una imagen PNG de 512 × 512 píxeles que contiene el ícono de la aplicación para mostrar en iTunes y la aplicación App Store en el iPad.
- iTunesMetadata.plist contiene varios fragmentos de información, que van desde el nombre y la identificación del desarrollador, la información de derechos de autor, el identificador del paquete, el nombre de la aplicación, el género, la fecha de lanzamiento, la fecha de compra, etc.
- La carpeta META-INF solo contiene metadatos sobre qué programa se utilizó para crear el IPA.


## Referencias

* [.ipa - por Wikipedia](https://en.wikipedia.org/wiki/.ipa)



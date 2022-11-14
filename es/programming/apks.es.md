
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo APK - Archivo de conjunto de APK",
  "description":"¿Más información sobre qué es un archivo APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## ¿Qué es un archivo APKS?

Un archivo con la extensión .apks es un archivo comprimido que es una colección de archivos **APK** del paquete de Android. Cada archivo APK individual en el archivo APKS se genera teniendo en cuenta varios aspectos de los dispositivos. Estos incluyen arquitectura, idioma, densidad de pantalla y otras características del dispositivo. Los archivos APKS son generados por **bundletool**. Se utiliza para crear Android App Bundle y convertir el paquete de aplicaciones en diferentes APK para su implementación en dispositivos.

## Formato de archivo APKS - Más información

Los archivos APKS se guardan como archivos comprimidos usando el formato de archivo [ZIP](/es/compression/zip/).

## ¿Cómo generar un archivo APKS?

Cuando Android App Bundle (AAB) está listo, se puede probar su comportamiento en la tienda Google Play para su implementación en un dispositivo. Los archivos APKS pueden generarse, para este propósito, a partir de archivos AAB e instalarse en dispositivos de prueba usando el [bundletool] de Android de Google (https://developer.android.com/studio/command-line/bundletool). Proporciona herramientas de línea de comandos para crear el archivo de almacenamiento APKS a partir de APK utilizando el siguiente comando.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Para implementar los APK en un dispositivo, el archivo APKS se puede firmar con la información de firma del dispositivo de la siguiente manera.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Referencias

* [bundletool - línea de comandos](https://developer.android.com/studio/command-line/bundletool)


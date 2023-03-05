{
  "date" : "2019-10-11",
  "keywords" :[ "archivo apk", "formato de archivo apk", "qué es un archivo apk", "archivo", "ejemplo de apk", "extensión de archivo apk","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - ¿Qué es un archivo APK?",
  "description":"Aprenda a saber qué es un archivo APK y las API que pueden crear y abrir archivos APK",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## ¿Qué es un archivo APK?

Un archivo con extensión .apk es un archivo de aplicación de Google Android que se utiliza para instalar aplicaciones (aplicaciones) en los dispositivos Android. Se crea como un archivo ejecutable utilizando el IDE oficial de Google Android Studio y se carga en la tienda Google Play para que los usuarios finales lo descarguen e instalen. Los archivos APK también se pueden generar y poner a disposición para la instalación manual antes de publicarlos en la tienda Google Play. Esto ayuda a probar la funcionalidad y el comportamiento del archivo del paquete APK generado. Por lo tanto, uno debe asegurarse de que el archivo APK sea de una fuente confiable y no contenga ningún malware.

## Formato de archivo APK

Los archivos APK se empaquetan comprimidos en formato de archivo [ZIP](/es/compression/zip/) que se puede abrir con cualquier software de apertura de archivos ZIP. La extensión .apk de dicho archivo se puede cambiar el nombre a .zip y abrir el archivo en cualquier aplicación ZIP o extraer su contenido.

## Contenido del paquete APK

Un solo archivo APK contiene todos los archivos necesarios para su instalación y ejecución. Un archivo APK, cuando se extrae con una aplicación ZIP, contiene los siguientes archivos y carpetas.

* `META-INF/`: directorio que contiene el archivo de manifiesto, la firma y una lista de recursos en el archivo
* `lib/`: directorio que contiene código compilado relacionado con plataformas específicas como armeabi-v7a, x86, arm64-v8a, etc.
* `res/`: directorio que contiene recursos no compilados, como imágenes
* `assets/`: directorio que contiene activos de aplicaciones, que puede recuperar AssetManager.
* `androidManifest.xml`: contiene el nombre, la información de versión y el contenido del archivo APK
* `classes.dex`: estas son clases de Java compiladas que se pueden ejecutar en la máquina virtual Dalvik y por Android Runtime
* `resources.arsc`: archivo de recursos compilado, como cadenas

## ¿Cómo instalar el archivo APK en un dispositivo Android?

Para instalar un archivo APK en sus dispositivos Android, se pueden seguir los siguientes pasos.

1. Descarga el APK usando el navegador web
2. Tóquelo: debería poder verlo descargarse en la barra superior de su dispositivo
3. Una vez que se haya descargado, abra Descargas, toque el archivo APK y toque Sí cuando se le solicite.

Siguiendo estos pasos comenzará la instalación de la aplicación en su dispositivo.

## Referencias

* [Formato de archivo APK](https://en.wikipedia.org/wiki/Android_application_package)


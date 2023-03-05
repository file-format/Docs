{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","qué es un archivo arsc","cómo abrir un archivo arsc", "extensión", "archivo", "archivo arsc","formato de archivo arsc", "extensión de archivo arsc" ,"Ejemplo de archivo arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Archivo de tabla de recursos del paquete de Android",
  "description":"Obtenga información sobre el formato de archivo ARSC y las API que pueden crear y abrir un archivo ARSC",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## ¿Qué es un archivo ARSC?

Un archivo ARSC es un archivo de tabla de recursos de Android que contiene la lista de recursos de la aplicación en formato de tabla. Contiene información como nombres de recursos, propiedades e ID. Los archivos ARSC son parte de los paquetes APK que se utilizan para instalar estas aplicaciones de Android. Todos los recursos, como imágenes, diseños, estilos y cadenas, en una aplicación de Android se convierten en archivos binarios cuando se genera el archivo APK. El archivo ARSC también se genera al mismo tiempo, que contiene una lista de todos los recursos compilados del programa y sus ID.

## Formato de archivo ARSC

Los archivos de extensión .arsc son archivos binarios generados después de que el compilador, como ANT (Eclipse) o Gradle (AS), compila el código de la aplicación de Android para generar el archivo [APK](/es/compression/apk/). Puede extraer el archivo APK utilizando cualquier utilidad de archivo como WinZip para ver su contenido, que son los archivos de clase java compilados, es decir, classes.dex. Además de estos, también contiene este archivo ARSC que contiene metainformación sobre:

* Los nodos XML
* Los atributos
* Los ID de recursos

Los ID de recursos hacen referencia a los recursos en un archivo APK, mientras que los atributos se resuelven en un valor en tiempo de ejecución. La herramienta aapt de Android recopila todos los recursos definidos en los archivos en el momento de la compilación y les asigna ID de recursos. Una vez que se asignan los identificadores a los recursos compilados, se genera un archivo R.java a partir del código fuente y de resources.arsc.

## Referencias

* [Estructura de la tabla de recursos binarios](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)


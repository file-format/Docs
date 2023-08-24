{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "JSON", "Archivo de archivo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - Formato de archivo de archivo HTTP",
  "description" :"Su guía de formato de archivo para aprender qué es un archivo HAR y las API que pueden crear y abrir un archivo HAR",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## ¿Qué es un archivo HAR?

Un archivo con .har (archivo HTTP Archive) es un archivo de almacenamiento HTTP que almacena datos de sesión que se transfieren a través de muchos navegadores (como Chrome, Safari, IE, Firefox, etc.) en [JSON](/es/web/json/) formato de archivo. Los datos transferidos a través de Internet entre el servidor y el cliente (en este caso, el navegador del usuario) contienen encabezados de solicitud y respuesta HTTP que se almacenan en el archivo HAR. Además, contiene información detallada sobre los datos de rendimiento de las páginas web cargadas en el navegador. Los archivos HAR se pueden abrir en cualquier editor de texto, como Notepad en Microsoft Windows OS y TextEdit en Apple MacOS.

## Formato de archivo HAR - Más información

Los archivos HAR almacenan la información de la sesión en un archivo de texto sin formato utilizando el popular formato JSON. Las especificaciones para el formato de archivo HAR fueron elaboradas por Web Performance Group del World Web Consortium (W3C), pero no se pudieron publicar. Sin embargo, definió con éxito un formato de archivo para transacciones HTTP.

Además de monitorear la transferencia de información de solicitud y respuesta, los desarrolladores utilizan los archivos HAR para registrar el rendimiento del navegador web en términos de velocidad de carga de la página, duración de la carga del contenido, contenido cargado, consultas ejecutadas para obtener la respuesta del navegador y muchos otros. .

## ¿Por qué usar archivos HAR?

Los archivos HAR pueden ser útiles para mejorar el rendimiento de un sitio web mediante la evaluación de largos tiempos de carga, tiempos de procesamiento de páginas y tiempos de respuesta. Los archivos HAR se pueden analizar para encontrar dichos problemas y resolver cualquier problema con el sitio web para mejorar el rendimiento.

## ¿Cómo generar un archivo HAR?

Entonces, ¿cómo generar un archivo HAR? Bueno, esto depende del tipo de navegador que esté utilizando para generar un archivo HAR. En esta guía, enumeramos los pasos para el navegador Google Chrome. Los métodos para generar archivos HAR usando Safari, Firefox, etc. pueden buscarse fácilmente en Internet y seguirse.

### Pasos para generar un archivo HAR usando Google Chrome

Los siguientes pasos se pueden llevar a cabo en una página web donde se enfrentan problemas.

1. Abra la página web en Google Chrome donde ocurrió el problema.
1. Abra la herramienta de desarrollador (inspeccionar elemento).
1. Vaya a la izquierda del panel para iniciar la grabación del archivo. Hay un pequeño botón rojo redondo en esta sección.
1. Haga clic en el "icono Borrar" para eliminar cualquier registro guardado en el navegador.
1. Para guardar el contenido que desea como se muestra arriba, haga clic derecho y haga clic en "Guardar como archivo HAR"

## Referencias

* [Formato de archivo HAR - Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))


{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo APPCACHE - Formato de archivo de manifiesto de caché HTML5",
  "description" :"Obtenga más información sobre qué es un archivo APPCACHE y las API que pueden crear y abrir archivos APPCACHE",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## ¿Qué es un archivo APPCACHE?

Un archivo APPCACHE es un archivo de texto que contiene la lista de recursos que los navegadores almacenarán en caché para acceder sin conexión a las aplicaciones web. Esto es útil cuando no hay conexión a Internet. En tal situación, el navegador utiliza los recursos de caché fuera de línea para proporcionar acceso a los contenidos web. El archivo APPCACHE contiene recursos web como imágenes (por ejemplo **[PNG](/es/image/png/)**, **[WEBP](/es/image/webp/)**, etc.), hojas de estilo **([ CSS])(/es/web/css/)** y archivos de script (como archivos Javascript **[JS](/es/web/js/)**).

Las aplicaciones que pueden **abrir archivos APPCACHE** incluyen navegadores web como Google Chrome, Safari y Firefox.

## Formato de archivo APPCACHE - Más información

Los archivos APPCACHE son archivos de texto simples que brindan acceso sin conexión a páginas web para ejecutar sin conexión a Internet. La presencia de APPCACHE designa una página como disponible sin conexión.

### ¿Cómo hacer referencia a un archivo APPCACHE?

En su página HTML, se hace referencia a un archivo APPCACHE de la siguiente manera.

```
<html manifest="example.appcache">
  ...
</html>
```

## Estructura de un archivo de manifiesto APPCACHE

Un archivo de manifiesto APPCACHE simple tiene el siguiente aspecto.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Este es el ejemplo más simple y también puede haber estructuras más complejas presentes.

## Ventajas del Manifiesto APPCACHE

El uso de la interfaz de caché brinda a las aplicaciones web las siguientes ventajas.

1. Navegación sin conexión: la interfaz de caché permite a los usuarios finales navegar por todo el sitio cuando están sin conexión.
1. Velocidad: la memoria caché permite el acceso de alta velocidad al contenido sin conexión directamente desde el disco
1. Accesibilidad todo el tiempo: en caso de que su sitio se caiga, los usuarios seguirán teniendo acceso a los contenidos web y podrán obtener la experiencia fuera de línea

## Referencias

* [Una guía para principiantes del manifiesto de AppCache](https://web.dev/appcache-beginner/)


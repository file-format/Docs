---
date: 2019-10-11
keywords: json, .json, formato de archivo json, cómo abrir archivos json, notación de objetos javascript, formato de datos json, formato de archivo .json
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "Formato de archivo JSON: ¿Qué es un archivo JSON?"
linktitle: JSON
description: "Obtenga información sobre el formato de archivo JSON y las API que pueden crear y abrir archivos JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## ¿Qué es un archivo JSON?

JSON (Notación de objetos de JavaScript) es un formato de archivo estándar abierto para compartir datos que utiliza texto legible por humanos para almacenar y transmitir datos. Los archivos JSON se almacenan con la extensión .json. JSON requiere menos formato y es una buena alternativa para [XML](/es/web/xml/). JSON se deriva de JavaScript, pero es un formato de datos independiente del idioma. Muchos lenguajes de programación modernos admiten la generación y el análisis de JSON. *application/json* es el tipo de medio utilizado para JSON.

## Formato de archivo JSON - Breve historia

Había una necesidad de comunicación entre el servidor y el cliente en tiempo real que condujo a la creación de JSON. El formato JSON fue especificado por primera vez por Douglas Crockford en marzo de 2001. JSON se basó en el estándar ECMA-262, 3.ª edición, diciembre de 1999, que es un subconjunto de JavaScript.

La primera edición del estándar JSON ECMA-404 fue publicada en octubre de 2013 por Ecma International. RFC 7159 se convirtió en la principal referencia para los usos de Internet de JSON en 2014. En noviembre de 2017, se publicó ISO/IEC 21778:2017 como estándar internacional. RFC 8259 fue publicado el 13 de diciembre de 2017 por The Internet Engineering Task Force, que es la versión actual del Internet Standard STD 90.

## Estructura de archivos JSON

Los datos JSON se escriben en pares **clave/valor**. La clave y el valor están separados por dos puntos (:) en el medio con la clave a la izquierda y el valor a la derecha. Los diferentes pares clave/valor están separados por una coma (,). La clave es una cadena entre comillas dobles, por ejemplo, "nombre". Los valores pueden ser de los siguientes tipos.

- `Número`
- `String`: Secuencia de caracteres Unicode entre comillas dobles.
- `Booleano`: Verdadero o Falso.
- `Array`: una lista de valores entre corchetes, por ejemplo

```json
[ "Manzana", "Plátano", "Naranja" ]
```

- `Objeto`: una colección de pares clave/valor rodeados de llaves, por ejemplo

```json
{"nombre": "Jack", "edad": 30, "Deporte favorito": "Fútbol"}
```

Los objetos JSON también se pueden anidar para representar la estructura de los datos. A continuación se muestra un ejemplo de un objeto JSON.

### Ejemplo de formato JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## ¿Cuál es el tamaño máximo del archivo JSON?

Prácticamente no hay límite en el tamaño máximo de un archivo JSON. Puede ser tan largo como el espacio que requiera el contenido a almacenar.

Cuando se trata de usar el formato de archivo JSON para transferir datos a través de Internet, se debe tener cuidado con los recursos disponibles de la computadora. Si se transfieren datos JSON grandes, la transferencia se verá afectada si el navegador del cliente tiene memoria limitada.


No hay un límite estricto definido por la especificación, pero debe tener cuidado de no agotar los recursos en las computadoras de sus usuarios, ya que degradará rápidamente su experiencia de usuario y es probable que abandonen su aplicación.

## JSON frente a XML

**XML** es otro formato de archivo común y ampliamente utilizado para el intercambio de datos a través de Internet. Cuando se trata de intercambio de datos entre aplicaciones, los desarrolladores tienen la opción de usar formatos de archivo XML y JSON. Sin embargo, JSON se adopta como la forma más conveniente para el intercambio de datos entre aplicaciones a través de Internet por las siguientes razones.

1. JSON brinda una vista clara y más fácil de leer de los datos en comparación con los formatos de archivo XML
1. JSON reduce la sobrecarga de la transferencia de datos a través de Internet, ya que tiene menos caracteres para definir el mismo conjunto de datos en comparación con XML.
1. Los lenguajes de programación modernos proporcionan analizadores integrados para analizar la respuesta JSON en la web.

## ¿Sabías?

Puede convertirse en colaborador en FileFormat.com para mantener la comunidad de formato de archivo actualizada con sus hallazgos. Si tiene que compartir algo sobre JSON o formatos de archivo web, puede publicar sus hallazgos en la sección [Noticias de formato de archivo web](https://news.fileformat.com/t/Web) para que las personas obtengan más información sobre estos.

## Referencias

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [Una introducción a JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)


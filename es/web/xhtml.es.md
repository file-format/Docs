{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "html extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Formato de archivo de lenguaje de marcado de hipertexto extensible",
  "description":"Obtenga información sobre el formato de archivo XHTML y las API que pueden crear y abrir archivos XHTML",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo XHTML?

El XHTML es un formato de archivo basado en texto con marcado en el XML, utilizando una reformulación de HTML 4.0. Estos archivos son adecuados para abrirlos o verlos en un navegador web. XHTML fue diseñado para ser más estructurado, menos secuencias de comandos, genérico; utilizando todas las instalaciones existentes de XML y más dispositivo independiente. XHTML proporciona un conjunto de elementos y atributos que en general valen la pena, con opciones de extensión en combinación con hojas de estilo. Los atributos se utilizan de la colección de atributos de metadatos. XHTML proporciona flexibilidad y accesibilidad al subordinar todos los elementos de presentación **[HTML](/es/web/html/)** a hojas de estilo. Las hojas de estilo son más versátiles que estos elementos de presentación. El World Wide Web Consortium (W3C) está desarrollando dinámicamente especificaciones para HTML 4.01, HTML5 y XHTML.

## Breve historia del formato de archivo XHTML

La historia de XHTML comienza con un documento preliminar publicado en diciembre de 1998 por el World Wide Web Consortium. Este documento hace referencia a la "Reformulación de HTML en XML", una especificación denominada XHTML 1.0. Esta nueva especificación reformula HTML en XML utilizando los elementos o atributos existentes. En mayo de 1999, W3 Consortium declaró que HTML 4.0 se había reformado como una aplicación XML. es decir, XHTML. El 26 de enero de 2000, W3C publicó la primera especificación que define XHTML 1.0. Además, el 31 de mayo de 2001, el W3C anunció XHTML como lenguaje independiente y comenzó a trabajar en el desarrollo de HTML 5.0. Sin embargo, en 2005, se formó un grupo de trabajo (WHATWG) cuyo objetivo era mejorar el HTML común independientemente de XHTML. El WHATWG eventualmente comenzó a trabajar en HTML5 en paralelo a XHTML 2.

## Formato de archivo XHTML

XHTML es un formato, que es una colección de diferentes tipos de documentos y módulos que imitan, categorizan y amplían HTML 4. Los archivos en XHTML están basados en XML y están destinados a trabajar con los agentes de usuario basados en XML. Los archivos XHTML son compatibles con XML. Las herramientas XML estándar se utilizan para ver, editar y validar archivos XHTML. Las aplicaciones dependientes del Modelo de objetos de documento HTML o del Modelo de objetos de documento XML [DOM] pueden operar a través de documentos XHTML. Al optar por XHTML hoy, los desarrolladores de contenido pueden disfrutar de todos los beneficios asociados de XML sin preocuparse por la compatibilidad hacia adelante o hacia atrás de su contenido.

Un conjunto de elementos relacionados construyen un módulo en XHTML. Un módulo de formularios o tablas puede contener varios elementos de formularios o tablas que se pueden mostrar en una página web. La modularización tenía como objetivo aislar los elementos HTML en conjuntos de numerosos elementos vinculados. Para que los desarrolladores de contenido puedan aprovechar la selección de módulos para diferentes tipos de dispositivos. Además, los módulos permiten a los agentes de usuario seleccionar elementos sin perder la coherencia con el estándar XHTML. Los requisitos de análisis de XHTML son los mismos que los de XML, mientras que HTML practica los suyos.

### Conformidad del documento

Las especificaciones de la oferta XHTML2 se ajustan a los documentos XHTML 1.0, que utiliza los elementos y atributos de los espacios de nombres de XML y XHTML 1.0. La conformidad del documento es de dos tipos.

Un documento de conformidad estricta está basado en XML y solo necesita los servicios obligatorios definidos en esta especificación. Se deben cumplir los siguientes criterios para los archivos XHTML:

* Un archivo debe cumplir con las restricciones definidas en las DTD y en el Apéndice B.
* El elemento base del archivo debe ser html.
* El elemento base del archivo debe contener una declaración para el espacio de nombres XHTML y debe definirse como:

```
http://www.w3.org/1999/xhtml.
```

* El elemento base podría escribirse como:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Antes que el elemento base, se debe declarar un DOCTYPE, cuyo identificador público debe hacer referencia a una de las tres definiciones de tipo de documento (DTD). El identificador del sistema puede modificarse para cumplir con las convenciones actuales del sistema.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

En documentos XML, no es necesario especificar declaraciones XML en todos los documentos; sin embargo, los desarrolladores de contenido se ven tentados a usar declaraciones XML en todos sus documentos XHTML. Estas declaraciones son obligatorias cuando la codificación de caracteres del documento es diferente de UTF-8/16 o cuando un protocolo de gobierno no especifica ninguna codificación. El siguiente ejemplo de un documento XHTML define las declaraciones XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Un agente de usuario conforme debe cumplir con las siguientes reglas:

* El análisis y la evaluación del documento XHTML lo realiza un agente de usuario que garantiza su coherencia con la recomendación XML 1.0.
* En caso de validar agente de usuario, debe verificar la validez de los documentos para sus DTD referenciados según XML. Cuando el agente de usuario procesa el archivo XHTML como XML genérico, las características del tipo ID se reconocerán como identificadores de fragmento.

Si un agente de usuario se topa con un elemento no reconocido, los siguientes son los criterios obligatorios que debe cumplir

* procesar el contenido de ese elemento desconocido
* ignorar el atributo y su valor
* Utilice el valor del atributo proporcionado por defecto.

Cuando el agente de usuario se encuentra con una declaración de referencia de entidad que no se ha procesado antes, debe procesarse como los caracteres (comenzando con el signo "&" y terminando con el punto y coma). Durante el procesamiento de contenido, los caracteres o las referencias a entidades de caracteres que son predecibles por el agente de usuario pero que no se pueden representar pueden usar cualquier representación alternativa que produzca un significado similar. En tal caso, el documento debe mostrarse de una manera que haga evidente al usuario el hecho de que el proceso de renderizado no ha sido normal. Para procesar espacios en blanco, el agente de usuario debe buscar la definición de los caracteres CSS [CSS2].

## Compatibilidad con versiones anteriores de XHTML

La compatibilidad con versiones anteriores de los documentos XHTML 1. está bien versada con los agentes de usuario de HTML 4, si se siguen las reglas adecuadas. XHTML 1.1 es totalmente compatible, excepto las anotaciones Ruby, aunque generalmente los navegadores HTML 4 las ignoran. XHTML 2.0 es comparativamente menos compatible, sin embargo, el problema se ha solucionado hasta cierto punto mediante el uso de secuencias de comandos.

## Referencias

* [Una historia de XHTML: desde la década de 1990 hasta la actualidad](https://www.brighthub.com/internet/web-development/articles/109224.aspx)


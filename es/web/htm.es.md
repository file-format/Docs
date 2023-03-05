{
  "date" : "2019-10-11",
  "keywords" :[ "htm","archivo htm", "formato de archivo htm", "tipo de archivo htm", "archivo", "tipo", "qué es un archivo htm"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo HTM",
  "description" :"Su guía de formato de archivo para aprender qué es un archivo HTM y las API que pueden crearlos y abrirlos",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo HTM?

Los archivos con la extensión **.htm** representan el lenguaje de marcado de hipertexto para crear páginas web para mostrar en navegadores web como Google Chrome, Internet Explorer, Firefox y muchos otros. Define las marcas para crear páginas estáticas que se publicarán en la World Wide Web (WWW) para que otras personas accedan a ellas. Estas marcas le dicen a los navegadores cómo mostrar el contenido de una página web. Dichas páginas pueden contener texto sin formato, imágenes, hipervínculos a otras páginas, videos y otra información multimedia. Cuando se publica una página web, puede echar un vistazo al código de marcado detrás de ella al ver la fuente de la página. Los navegadores modernos permiten inspeccionar cada sección de una página web donde se elabora cada subdivisión o elemento de marcado en la fuente HTM.

## Breve historia de HTM

Desde su creación y primera función, las especificaciones HTML han sido mantenidas por World Wide Web Consortium (W3C) desde 1996. En 2000, también se convirtió en un estándar internacional (ISO/IEC 15445:2000). En 1999, se publicó HTML 4.01. En 2004, el Grupo de Trabajo de Tecnología de Aplicaciones de Hipertexto Web (WHATWG) comenzó a trabajar en la versión HTML5 que se convirtió en un producto conjunto con el W3C en 2008. Se completó y estandarizó el 28 de octubre de 2014.

## Formato de archivo HTML

Un documento HTML 4 se compone de tres partes:

1. una línea que contiene información de la versión HTML
1. una sección de encabezado declarativo
1. un cuerpo, que contiene el contenido real del documento. El cuerpo puede ser implementado por el elemento BODY o el elemento FRAMESET para contener el cuerpo en marcos

Cada sección puede estar dirigida o seguida por espacios en blanco, nuevas líneas, tabulaciones y comentarios. Un ejemplo de un documento HTML simple es como se muestra a continuación:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Información de versión

La primera línea de código,<!DOCTYPE html> , se llama declaración de tipo de documento y le dice al navegador en qué versión de HTML está escrita la página. Dependiendo de la versión de HTML, hay varias declaraciones de tipo de documento diferentes que nombran la definición de tipo de documento (DTD) en uso para el documento. Cada DTD se diferencia de los demás en los elementos que admite y se diferencian de la siguiente manera:

* HTML 4.01 estricto: incluye todos los elementos y atributos que no han sido [obsoletos](https://www.w3.org/TR/html401/conform.html#deprecated) o no aparecen en los documentos de conjunto de marcos
* HTML 4.01 de transición: incluye todo lo que se encuentra en la estricta DTD más elementos y atributos obsoletos (la mayoría de los cuales se refieren a la presentación visual).
* Conjunto de marcos HTML 4.01: incluye todo en los marcos DTD plus de transición también

Para **HTML5**, la información de la versión es simplemente como se menciona a continuación.

```
<!DOCTYPE html>
```

### Información del encabezado

El encabezado de un documento HTML puede incluir una serie de elementos HTML que el navegador no procesa. Dichos elementos son metadatos que describen información sobre la página o incluyen secciones que se utilizan para obtener información de recursos externos como hojas de estilo CSS o archivos JavaScript. El encabezado de una página está representado por \<head> etiqueta y termina con \</head> etiqueta.

<html>Para configurar el título de la página, el \<title> El elemento es el único que se requiere dentro de las etiquetas \<head>. El mismo es utilizado por los motores de búsqueda para identificar el título de una página. </html>

### Información del cuerpo

Esta es la sección principal del archivo que contiene todo el contenido del archivo que procesan los navegadores. El cuerpo HTML puede contener marcas que pueden hacer referencia a varios bloques de construcción en forma de etiquetas. Puede contener varios tipos diferentes de información como texto, imágenes, colores, gráficos, etc. Además, los elementos de audio y video también se pueden incrustar en el cuerpo html para que los navegadores los representen. En presencia de la aplicación de hojas de estilo modernas para la representación visual, los atributos de presentación de BODY, como el color de fondo, el color del enlace, el color del texto, etc. han quedado obsoletos. Por lo tanto, se pueden lograr los mismos efectos usando hojas de estilo como se muestra a continuación:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Las hojas de estilo en línea son fáciles de incrustar y para aplicaciones rápidas a los efectos visuales, las hojas de estilo externas hacen que sea más conveniente implementar una vez y acceder en muchos lugares.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Elementos HTML

Como se mencionó anteriormente, los contenidos dentro del cuerpo HTML están representados por etiquetas, también conocidas como elementos Html. Cada etiqueta puede tener información adicional en forma de atributos que se escriben como
```
<tag attribute1#"value1" attribute2#"value2">
```
aunque no es necesario tener atributos con cada etiqueta. Si no se mencionan los atributos, se utilizan los valores predeterminados en cada caso. Los siguientes son algunos de los ejemplos de elementos:

#### Encabezado

```
<head>
  <title>The Title</title>
</head>
```

#### Encabezados

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Párrafos

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Referencias

* [La estructura global del documento HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


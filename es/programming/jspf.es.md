{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - Formato de archivo de fragmento JSP",
  "description":"Obtenga información sobre el formato de archivo JSPF y las API que pueden crear y abrir archivos JSPF",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## ¿Qué es un archivo JSPF?
El archivo con extensión .jspf se llama fragmento JSP; un archivo estático incluido en otro archivo JSP. Los archivos JSPF no se compilan solos, sin embargo, se compilan junto con la página en la que se incluyeron. Su sintaxis es similar al código Java Server Pages (JSP). Contiene solo un fragmento de JSP; no incluido todo el documento JSP completo.

## Formato de archivo JSPF
En su lugar, se utiliza el término "segmento JSP", ya que el término "fragmento JSP" está sobrecargado en la especificación JSP 2.0. Los fragmentos JSP pueden usar extensiones .jsp o .jspf y deben colocarse en **/WEB-INF/jspf** o con el resto de los archivos estáticos. Los fragmentos JSP que no sean páginas completas deben usar la extensión .jspf y deben colocarse en **/WEB-INF/jspf**

### Organización de archivos de fragmentos JSP o JSP
Un archivo JSP contiene las siguientes secciones en el orden en que aparecen:

1. Comentarios de apertura
2. Directiva(s) de página JSP
3. Directivas de biblioteca de etiquetas opcionales
4. Declaración(es) JSP opcional(es)
5. Código HTML y JSP

Un archivo JSP o JSPF comienza con un comentario de estilo del lado del servidor que se llama **Comentario de apertura**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Este comentario solo puede verse en el lado del servidor porque se elimina durante la representación de la página JSP.

## ¿Cuándo usar el archivo JSP Fragment?
Cuando una página JSP requiere una estructura determinada pero compleja que también puede reutilizarse en otras páginas JSP, una forma de manejar esto es dividirla en partes, utilizando el patrón Vista compuesta (la sección Patrones de Java Blueprints). Por ejemplo, una página JSP a veces tiene el siguiente diseño lógico en su estructura de presentación:

{{< figure src="../jspf.png" alt="Formato de archivo JSPF" >}}

En esta situación, esta página JSP compuesta se puede convertir en varios módulos, cada uno de los cuales se denominará un fragmento JSP independiente. Los fragmentos JSP se pueden colocar en las ubicaciones adecuadas en la página JSP compuesta. Por lo tanto, el archivo JSPF se usa cuando se usan directivas de inclusión estáticas para incluir una página que no sería llamada por sí misma, los archivos con la extensión .jspf deben colocarse en el directorio /WEB-INF/jspf/ del archivo de la aplicación web ( guerra).

## Ejemplo JSPF
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Referencias

* [Convenciones de código para las páginas de JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)


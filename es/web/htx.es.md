{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo HTX - Formato de archivo de extensión HTML",
  "description" :"Su guía de formato de archivo para saber qué es un archivo HTX y las API que pueden crear y abrir un archivo HTX",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo HTX?

Un archivo HTX es en realidad un archivo HTML que contiene variables de datos para mostrar los resultados de la consulta de la base de datos como una página web. En su mayoría creados con el software de desarrollo web de Microsoft FrontPage, los archivos HTX se guardan para guardarlos en la misma carpeta que el archivo Conector de base de datos de Internet (.IDC) correspondiente.

Los archivos HTX se pueden abrir con aplicaciones como Microsoft FrontPage y cualquier editor de texto como Notepad, TextEdit o Atom.

## Formato de archivo HTX

Los archivos HTX se guardan como archivos de texto sin formato con código para recuperar datos de una base de datos y guardarlos en variables para su visualización.


### Ejemplo de archivo HTX

Un ejemplo de archivo HTX es el siguiente que define un encabezado de página para mostrar la restricción de consulta y los documentos que se muestran en la página para mostrar al usuario.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

El resultado de este código de ejemplo es el siguiente.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Como puede verse, el archivo HTX es una plantilla que formatea cómo se devuelven y muestran los resultados a los usuarios finales. Está escrito en formato HTML con algunas extensiones de IIS y el Servicio de indexación. Estas extensiones incluyen nombres de variables y otros códigos para procesar los resultados.

## Referencias

* [Formatear los resultados en un archivo .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)


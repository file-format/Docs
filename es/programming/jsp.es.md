{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Formato de archivo de páginas del servidor Java",
  "description":"Obtenga más información sobre el formato de archivo JSP con el ejemplo de JSP y las API que pueden crear y abrir archivos JSP",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## ¿Qué es un archivo JSP?
Los archivos JSP se realizan como páginas dinámicas basadas en datos para sus aplicaciones web Java. El JSP significa Java Server Pages; se puede realizar como una extensión de Servlet porque permite más funciones que servlet, como el lenguaje de expresión. JSP y Servlet hacen el mismo trabajo juntos en aplicaciones web Java más antiguas. Desde una perspectiva de programación, la diferencia más clara entre ellos es que con los servlets usted escribe el programa Java y luego incrusta el marcado estático (como HTML) en ese código, mientras que JSP comienza con el script del lado del cliente o el marcado, luego incrusta las etiquetas JSP para conecte su página al backend de Java.

## Formato de archivo JSP
Un archivo guardado con **extensión de archivo jsp** contiene las siguientes secciones en el orden en que aparecen:

1. Comentarios de apertura
2. Directiva(s) de página JSP
3. Directivas de biblioteca de etiquetas opcionales
4. Declaración(es) JSP opcional(es)
5. Código HTML y JSP

### Comentarios de apertura
Un archivo JSP o un archivo de fragmento comienza con un comentario de estilo del lado del servidor:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
El comentario anterior aparece solo en el lado del servidor porque se elimina al mostrar la página en el navegador. El comentario puede contener información sobre el(los) autor(es), la fecha y el aviso de copyright de la revisión, un identificador y una descripción sobre la página JSP para desarrolladores. Ciertos programas reconocen que la combinación de los caracteres " @(#)" indica el inicio de un identificador.

### Directiva(s) de página JSP
Una directiva de página JSP define los atributos asociados con la página JSPF en el momento de la traducción. La especificación JSP no impone una restricción sobre cuántas directivas de página JSP se pueden escribir en una sola página. Vea el siguiente ejemplo:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Si una directiva de página excede el ancho normal de una página JSP, la directiva se divide en varias líneas:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Directivas de biblioteca de etiquetas opcionales
En la página JSP, una directiva de biblioteca de etiquetas declara bibliotecas de etiquetas personalizadas. Una directiva corta se puede declarar en una sola línea. Varias directivas de biblioteca de etiquetas se apilan juntas en la misma ubicación dentro del cuerpo de la página JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Declaración(es) JSP opcional
  


Los métodos y variables declarados en un archivo JSPF deben existir en las declaraciones JSP. Estos métodos y variables son similares a las declaraciones en el lenguaje de programación Java, y es por eso que se deben seguir las convenciones de código relevantes. Las declaraciones generalmente se escriben en un solo < %! ... %> bloque de declaraciones JSP, para centralizar las declaraciones dentro de un área del cuerpo de la página JSP. mira los siguientes ejemplos:

#### Bloques de declaración dispares:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Bloque de declaración preferido:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Código HTML y JSP
Esta sección de una página JSP contiene el cuerpo HTML de la página JSP y el código JSPF, tales como expresiones JSP, scriptlets e instrucciones JavaBeans.

## Ciclo de vida de una página JSP

El flujo de la página JSP por fases se proporciona aquí:

- Traducción de página JSP
- Compilación de la página JSP
- Classloading (el cargador de clases carga el archivo de clase)
- Instanciación (Se crea el Objeto del Servlet Generado).
- Inicialización (el contenedor invoca el método jspInit()).
- Procesamiento de solicitudes (el contenedor invoca el método _jspService()).
- Destruir (el contenedor invoca el método jspDestroy()).

{{< figure src="../jsp.jpg" alt="Formato de archivo JSP" >}}

## Ejemplo JSP

Aprender sobre las tecnologías JSP es muy fácil hoy en día porque muchos tutoriales JSP están disponibles en Internet. El siguiente ejemplo de JSP es para procesar el pedido, actualizando los registros apropiados en la base de datos.
```
<html>
<head>
  <title>Order Book</title>
</head>
 

<body>
  <h1>Another E-Bookstore</h1>
  <h2>Thank you for ordering...</h2>
 

  <%
    String[] ids = request.getParameterValues("id");
    if (ids != null) {
  %>
  <%@ page import = "java.sql.*" %>
  <%
      Connection conn = DriverManager.getConnection(
          "jdbc:mysql://localhost:8888/ebookshop", "myuser", "xxxx"); // <== Check!
      // Connection conn =
      //    DriverManager.getConnection("jdbc:odbc:eshopODBC");  // Access
      Statement stmt = conn.createStatement();
      String sqlStr;
      int recordUpdated;
      ResultSet rset;
  %>
      <table border=1 cellpadding=3 cellspacing=0>
        <tr>
          <th>Author</th>
          <th>Title</th>
          <th>Price</th>
          <th>Qty In Stock</th>
        </tr>
  <%
      for (int i = 0; i < ids.length; ++i) {
        // Subtract the QtyAvailable by one
        sqlStr = "UPDATE books SET qty = qty - 1 WHERE id = " + ids[i];
        recordUpdated = stmt.executeUpdate(sqlStr);
        // carry out a query to confirm
        sqlStr = "SELECT * FROM books WHERE id =" + ids[i];
        rset = stmt.executeQuery(sqlStr);
        while (rset.next()) {
  %>
          <tr>
            <td><%= rset.getString("author") %></td>
            <td><%= rset.getString("title") %></td>
            <td>$<%= rset.getInt("price") %></td>
            <td><%= rset.getInt("qty") %></td>
          </tr>
  <%}
        rset.close();
  }
      stmt.close();
      conn.close();
}
  %>
  </table>
  <a href="query.jsp"><h3>BACK</h3></a>
</body>
</html>
```


 


## Referencias

* [Convenciones de código para las páginas de JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Tutorial JSP](https://www.javatpoint.com/jsp-tutorial)


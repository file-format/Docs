{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","archivo shtml", "formato de archivo shtml", "tipo de archivo shtml", "archivo", "tipo", "qué es un archivo shtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Lado del servidor incluye archivo HTML",
  "description":"Obtenga información sobre el formato de archivo SHTML y las API que pueden crear y abrir archivos SHTML",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## ¿Qué es un archivo SHTML?

Un archivo con extensión .shtml es una página web que está escrita en [HTML](/es/web/html/) e incluye instrucciones del servidor. También puede contener archivos del lado del servidor similares a los archivos ASP para una carga más rápida. Los archivos del lado del servidor también pueden contener código ejecutable que puede hacer que el servidor se cargue más lento de lo habitual. Los archivos SHTML son similares a HTML pero también permiten el uso de comandos de servidor simples. Estos comandos del servidor se realizan en un lenguaje de programación de computadora simple llamado Server Side Incluye (SSI). SHTML ha sido reemplazado en gran medida por otros lenguajes de programación del lado del servidor, como [PHP](/es/programming/php/).

## Formato de archivo SHTML

Los archivos SHTML están escritos en texto sin formato y usan los [comandos SSI] (https://www.w3.org/Jigsaw/Doc/User/SSI.html) que se ejecutan en el lado del servidor. Estos comandos del lado del servidor se pueden usar incluso para conectarse a la base de datos usando los controladores de la base de datos y obtener datos de los usuarios de las tablas.

## Ejemplo SHTML

Las instrucciones del lado del servidor se utilizan en aplicaciones como el contador de visitantes de la página o el calendario de la página web. El siguiente ejemplo muestra las primeras cuatro columnas de las primeras tres líneas de la base de datos de usuarios.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## Referencias

* [Lado del servidor incluye](https://en.wikipedia.org/wiki/Server_Side_Includes)


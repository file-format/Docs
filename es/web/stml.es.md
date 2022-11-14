{
  "date" : "2021-05-20",
  "keywords" :[ "stml","archivo stml", "formato de archivo stml", "tipo de archivo stml", "archivo", "tipo", "qué es un archivo stml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - Archivo SSI HTML",
  "description":"Obtenga más información sobre el formato de archivo STML y las API que pueden crear y abrir archivos STML",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## ¿Qué es un archivo STML?

Un archivo con extensión .stml es una página web con instrucciones del lado del servidor que se ejecutan cuando un usuario carga la página en el navegador web. Las páginas STML contienen código del lado del servidor que incluye elementos del lado del servidor para realizar tareas que no son posibles de lograr con HTML simple. Aunque es similar a [HTML](/es/web/html/), STML ofrece más potencia al ejecutar los comandos en el servidor, también llamado Server Side Incluye (SSI). Con la introducción de nuevos lenguajes de programación con secuencias de comandos del lado del servidor, como PHP, el uso de STML se reduce, aunque todavía es compatible con todas las tecnologías del lado del servidor. Los archivos STML se pueden abrir en cualquier editor de texto y editar para actualizar los comandos.

## Formato de archivo STML

STML se basa en un formato de archivo de texto ascii simple que es legible por humanos. Sin embargo, sigue la sintaxis definida y ejercitada mediante los [comandos SSI] (https://www.w3.org/Jigsaw/Doc/User/SSI.html) que se ejecutan en el lado del servidor. Como cualquier otro lenguaje de secuencias de comandos del lado del servidor, STML puede usar los comandos del lado del servidor para realizar tareas como el contador de visitantes de la página, el calendario de la página web, recuperar registros de la base de datos y otros similares.

## Ejemplo STML

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


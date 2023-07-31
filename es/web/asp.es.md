{
  "date" : "2019-10-11",
  "keywords" :[ "asp","archivo asp", "formato de archivo asp", "tipo de archivo asp", "archivo", "tipo", "qué es un archivo asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Formato de archivo de páginas Active Server",
  "description" :"Obtenga información sobre qué es un archivo ASP y las API que pueden crearlos y abrirlos",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo ASP?

ASP significa Active Server Pages, que es un marco de desarrollo para crear páginas web. Permite que el código de la computadora sea ejecutado por un servidor interno para atender las solicitudes web. Cuando el navegador web genera una solicitud para un archivo ASP, el servidor lee el archivo y ejecuta cualquier código/secuencia de comandos dentro de él para generar el resultado **[HTML](/es/web/html/)** que se devuelve al navegador para la visualización.

A diferencia de las páginas HTML, que son páginas estáticas servidas por el servidor, los archivos ASP generan contenidos dinámicos en tiempo de ejecución que pueden implicar solicitudes de datos de una base de datos. Las páginas ASP suelen utilizar la extensión .asp en lugar de .html. Dado que el código/secuencia de comandos dentro de un archivo ASP se ejecuta en el lado del servidor, el navegador solicitante no puede ver el código utilizado para crear la página servida. Todos los navegadores modernos son capaces de mostrar páginas generadas como resultado. Al estar construidas con tecnología de Microsoft, las páginas creadas con ASP se alojan en servidores de Microsoft Internet Information Services (IIS).

## Breve historia del formato de archivo ASP
ASP ha pasado por algunas revisiones hasta que fue reemplazado por ASP.NET, que es una forma más moderna y eficiente de desarrollar y administrar páginas del lado del servidor. La compatibilidad con ASP se incluye de forma predeterminada junto con Internet Information Services (IIS). ASP se publicó en tres versiones diferentes con mejoras en cada una.

* ASP 1.0 se lanzó en diciembre de 1996 como parte de IIS 3.0
* ASP 2.0 se lanzó en septiembre de 1997 como parte de IIS 4.0
* ASP 3.0 se lanzó en noviembre de 2000 como parte de IIS 5.0

## Objetos funcionales ASP

Los archivos ASP usan objetos del lado del servidor para procesar las solicitudes de los usuarios y generar páginas de salida para servir a los usuarios. Cada objeto tiene un conjunto de colecciones, propiedades y métodos para procesar solicitudes y respuestas. Estos objetos incluyen:

### Objeto de solicitud

Cuando un navegador solicita una página de un servidor, se denomina solicitud. El objeto Solicitud se utiliza para obtener información de un visitante.

### Objeto de respuesta

El objeto de respuesta ASP se utiliza para enviar resultados al usuario desde el servidor.

### Objeto de servidor

El objeto Servidor ASP se utiliza para acceder a propiedades y métodos en el servidor. Permite conexiones a bases de datos (ADO), sistema de archivos y uso de componentes instalados en el servidor.

### Objeto de sesión

Un objeto de sesión es como un enlace entre el navegador del usuario que solicita una página del servidor y el propio servidor. Esto se logra mediante una cookie creada por ASP y enviada a la computadora del usuario. El objeto Session almacena información o cambia la configuración de una sesión de usuario. La información se almacena en un objeto de sesión y se comparte en todas las páginas de una aplicación. La información común almacenada en las variables de sesión son el nombre, la identificación y las preferencias. El servidor crea un nuevo objeto de sesión para cada nuevo usuario y destruye el objeto de sesión cuando la sesión caduca.

### Objeto de aplicación

El objeto Aplicación contiene información que será utilizada por muchas páginas de la aplicación (como la información de conexión de la base de datos). Se puede acceder a la información desde cualquier página. La información también se puede cambiar en un solo lugar y los cambios se reflejarán automáticamente en todas las páginas. El objeto Aplicación se usa para almacenar y acceder a variables desde cualquier página, al igual que el objeto Sesión.

### Objeto ASPError

El objeto ASPError se implementó en ASP 3.0 y está disponible en IIS5 y versiones posteriores. El objeto ASPError se usa para mostrar información detallada de cualquier error que ocurra en los scripts de una página ASP.

**Nota:** El objeto ASPError se crea cuando se llama a Server.GetLastError, por lo que solo se puede acceder a la información del error mediante el método Server.GetLastError.

## Referencias

* [ASP - Por W3C](https://www.w3schools.com/asp/default.asp)
* [Creación de páginas ASP simples](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))


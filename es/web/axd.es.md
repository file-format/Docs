{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo AXD - Formato de archivo del controlador web ASP.NET",
  "description" :"Obtenga más información sobre qué es un archivo AXD y las API que pueden crear y abrir archivos AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## ¿Qué es un archivo AXD?

Un archivo AXD es un archivo de configuración web que se utiliza para manejar y recuperar solicitudes de recursos integrados en ASP.NET. Se compone de instrucciones para recuperar recursos incrustados, como imágenes, archivos JavaScript ([.JS](/es/web/js/)) y archivos [.CSS](/es/web/css/). Los archivos AXD se utilizan para inyectar recursos en páginas del lado del cliente. Esto permite que las páginas del cliente accedan a estos recursos en el servidor de forma estándar.

## Formato de archivo AXD

Los archivos AXD se almacenan como archivos binarios en el lado del servidor. Se refiere a un archivo de controlador web en ASP.NET, que son componentes que generan respuestas a solicitudes específicas a un servidor web. Los archivos AXD realizan un procesamiento personalizado antes de generar la respuesta basada en las solicitudes de la página del lado del cliente. Por lo general, se guardan como archivos **WebResource.axd**.

### ¿Qué es el archivo WebResource.axd?

La mayoría de los proyectos ASP.NET guardan archivos AXD como archivos WebResource.axd que permiten que las páginas del lado del cliente descarguen recursos integrados en un ensamblado. Su aplicación puede tener un rendimiento lento si la ejecuta en modo de depuración, ya que el controlador WebResources.axd no está almacenado en caché.

## Referencias

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)


{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","archivo ascx", "formato de archivo ascx", "tipo de archivo ascx", "archivo", "tipo", "qué es un archivo ascx"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo ASCX",
  "description" :"Obtenga información sobre qué es un archivo ASCX y las API que pueden crear y abrir archivos ASCX",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo ASCX?

Un archivo con extensión .ascx es un control de usuario que se utiliza como componente reutilizable en las páginas web. Se hace referencia en cualquier sitio web ASP arrastrándolo desde el cuadro de control a la página. Los controles de usuarios de ASCX se agregan al proyecto como una fuente central, lo que hace que cualquier cambio en el control de usuario se refleje en todo el sitio web. A diferencia de los archivos ASMX que definen un mecanismo para comunicarse dentro de 2 objetos a través de Internet, los archivos ASCX son controles de usuario para incrustar en páginas o sitios web.

## Formato de archivo ASCX

Los archivos ASCX se escriben en formato de texto sin formato y pueden usar código detrás de funciones como páginas web que terminan en .ascx.cs. El código de marcado de los controles de usuario comienza con la directiva @Control, como se muestra en el siguiente ejemplo.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Este control de usuario web se puede reutilizar en muchas páginas, como el pie de página, el encabezado o algún tipo de navegación del sitio. Los controles de usuario web tienen propiedades, métodos y eventos como cualquier otro control que los hace útiles para establecer su comportamiento visual.

### Ejemplo de registro de controles de usuario en web.config

Para utilizar un único control de usuario en muchas páginas, el control web se puede registrar en web.config. Esto permite utilizar el control sobre todo el sitio web en lugar de registrarse en cada página individualmente. El siguiente código de ejemplo define cómo registrar un control web en web.config para que se muestre como pie de página en todo el sitio web.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Referencias

* [ASCX frente a ASMX](https://forums.asp.net/t/1838934.aspx?Cómo+trabajar+con+archivos+ascx+)
* [Control de usuario de ASCX] (http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)


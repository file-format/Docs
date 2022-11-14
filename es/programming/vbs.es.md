{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "archivo", "extensión", "formato de archivo", "Script de Visual Basic", "Guía de programación", "ejemplo de vbs", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Archivo de secuencias de comandos de Visual Basic",
  "description":"Obtenga información sobre el formato de archivo VBS y las API que pueden crear y abrir archivos VBS",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## ¿Qué es un archivo VBS?

VBS o VBScript está conectado con la edición de secuencias de comandos de Microsoft Visual Basic. En el entorno informático, el usuario puede acceder y controlar muchos aspectos del mismo. VBScript puede usar un modelo denominado **Modelo de objetos componentes** para aprovechar los elementos y las herramientas del entorno. Este entorno se especifica para trabajar y ejecutar VBScript.

Funciona de manera similar a Javascript cuando el cliente accede a él en el campo del desarrollo web. También es utilizado por los servidores para el procesamiento de páginas web. Se puede considerar en otros tipos de archivos de secuencias de comandos, como aplicaciones de [HTML](/es/web/html/).


## Breve historia ##

Se lanzó por primera vez en 1996, como parte de las tecnologías utilizadas por Microsoft especificadas para Windows Scripts. Inicialmente, se desarrolló específicamente para ayudar a los desarrolladores web. En el mismo año, se lanzó el explorador de Microsoft Windows llamado Internet Explorer junto con las características de Visual Basic Script.

Con el progreso de la tecnología y el desarrollo web, se lanzaron muchas versiones de VBScript junto con muchas funciones avanzadas. Además, el próximo año, este lenguaje de scripting formará parte de Microsoft Windows con nuevas funciones.

## Especificación técnica ##

Para las páginas web del lado del servidor, se utilizan herramientas como **Active Server Pages** junto con VBScript. Este lenguaje de secuencias de comandos también se puede utilizar en el componente de secuencias de comandos de Windows. Los archivos de este idioma se almacenan con extensión .vbs en Windows.

Hay muchas estructuras de control, como bucles, que se utilizan en el código de este lenguaje. También incluye argumentos que son línea de comando y pueden ser con o sin nombre. Los archivos de este idioma se pueden almacenar simplemente en las carpetas o en el escritorio de un sistema operativo Windows. Aunque no existe un entorno de desarrollo integrado específico para VBScript, los programas como Microsoft Script Editor brindan la facilidad de desarrollo de este lenguaje.

Cuando VBScript está alojado en el host Script de Windows, proporciona varias funciones que son bastante comunes a los lenguajes de secuencias de comandos pero que no están disponibles en Visual Basic 6.0. Las funciones que implican un acceso fácil o directo incluyen impresoras de red, argumentos de línea de comandos con nombre y sin nombre, stdout y stdin, recursos compartidos de red, instrumentación de administración de Windows, información de usuario de redes como membresía de grupo y mucho más.

## Ejemplo de formato de archivo VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Referencia ##

* [VBS - por Wikipedia](https://en.wikipedia.org/wiki/VBScript)




{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "formato de archivo", "tipo de archivo", "qué es un archivo .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - Archivo de configuración ASP",
  "description" :"Obtenga información sobre qué es un archivo ASA y las API que pueden crear y abrir archivos ASA",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## ¿Qué es un archivo ASA?

Un archivo ASA es un archivo de configuración, creado para proyectos [ASP](/es/web/asp/)/ASP.NET. Contiene declaraciones de variables, contenidos y funciones que están destinadas a ser accesibles a nivel global en la aplicación. Todas las páginas del proyecto pueden acceder a estas variables y funciones, evitando así el requerimiento de reescribirlas. Un ejemplo de ello es la página Global.asa que se almacena en el directorio raíz para que otras páginas del sitio web de ASP puedan acceder a ella. Los archivos Global.asa son opcionales, pero si se usan, cada aplicación puede tener solo un archivo Global.asa.

## Formato de archivo ASA: más información

Los archivos ASA son archivos de texto sin formato con la siguiente información.

* Eventos de aplicación
* Eventos de sesión
* \<object> declaraciones
* Declaraciones de TypeLibrary
* la directiva #include

## Ejemplo de archivo ASA

Un archivo Global.asa podría verse así.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Referencias

* [Archivo ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)


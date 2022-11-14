{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "extensión", "archivo", "formato", "sistema", "Cold Fusion Markup Language", "idioma", "páginas web CFM", "motor CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Marcado de fusión en frío",
  "description":"Obtenga información sobre el formato de archivo CFM y las API que pueden crear y abrir archivos CFM",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## ¿Qué es un archivo CFM? ##

Las páginas web y los archivos utilizados en **Cold Fusion Markup Language** contienen extensiones de CFM y se denominan páginas web de CFM. Este lenguaje de secuencias de comandos de desarrollo web se ejecuta en Google App Engine, .NET framework y JVM. Puede contener un lenguaje de programación o código del lenguaje. Cuando el usuario accede a alguna de sus páginas, el servidor web de ColdFusion la ejecuta. Se pueden usar CFScript (que está cerca de JavaScript) o etiquetas para escribir CFML. CFML se puede usar para generar otros lenguajes además de [HTML](/es/web/html/) como [CSS](/es/web/css/), [JavaScript](/es/web/js/), [XML](/es/web/ xml/), y más.

El uso de este lenguaje y las etiquetas que admite es principalmente en el desarrollo de aplicaciones web dinámicas. Los archivos se pueden ejecutar directamente en el navegador en línea si ocurre algún error durante el uso fuera de línea de la plataforma de desarrollo de la aplicación.
 

CFML funciona de manera que se otorgan extensiones de archivo de servidor específicas (.cfc, .cfm) para su procesamiento en el motor CFML. Si los motores están basados en Java, se consigue mediante servlets de Java. El motor de CFML solo procesa funciones y etiquetas y devuelve funciones y texto fuera de las etiquetas CFML al servidor web sin ningún cambio.


## Breve historia ##

En 1995, fue creado por primera vez por una corporación llamada Allaire. En 2005 Adobe lo adquirió y aún ahora brinda servicios para desarrollar ColdFusion. Con el paso de los años, muchas personas y empresas lo desarrollaron y actualizaron. En 2012, se lanzó una fundación llamada OpenCFML. Posteriormente, en 2015, el ex Railo prestó sus servicios para mejorar el rendimiento de CFM y redujo los recursos para una mejor funcionalidad. La actualización más reciente se lanzó en 2020 y se anuncia que continuará hasta 2028.

## Formato de archivo CFM ##

El código de los archivos CFM y las páginas web se compone principalmente de etiquetas como HTML, pero con una ligera diferencia. Estos archivos son responsables de realizar varias operaciones que los scripts de ColdFusion permiten ejecutar.
* Se puede acceder a estos archivos y ejecutarlos directamente tanto en Windows como en macOS usando el navegador de cualquier sistema operativo.
* Adobe ColdFusion proporciona la plataforma para el desarrollo de páginas web y aplicaciones dinámicas en PC.
* Se puede usar cualquier editor de texto como NotePad o cualquier otro editor de texto en un sistema operativo para abrir estos archivos, ya que estos archivos están basados en texto.
* Cuando cualquier archivo CFM se abre en un editor de texto, muestra un código que consta de etiquetas y scripts que uno no entendería a menos que sea un desarrollador web.

## Ejemplo de uso de CFM ##

A continuación se muestra un archivo CFM de ejemplo de uso simple.

### Documento CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Referencias ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)


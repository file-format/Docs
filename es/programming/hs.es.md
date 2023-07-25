{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Formato de archivo de script Haskell",
  "description":"Obtenga información sobre qué es un formato de archivo HS y las API que pueden crear y abrir archivos HS",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Formato de archivo de conjunto de ayuda de Java

## ¿Qué es un archivo HS de Java?

Un archivo con la extensión .hs en el lenguaje de programación Java es un archivo de documentación de ayuda que utiliza el sistema JavaHelp cuando lo activa una aplicación. Define el conjunto de ayuda para la aplicación en particular instalada y se compone de múltiples subconjuntos como parte de la ayuda del sistema para la aplicación. El programa Java debe poder encontrar el archivo del conjunto de ayuda cuyo nombre termina con la extensión .hs.

## Información del conjunto de ayuda de Java

Un archivo .hs puede contener la siguiente información.

|Información|Descripción|
---|---|
|Archivo de mapa|El archivo de mapa se emplea para asociar ID de tema con el localizador uniforme de recursos o el nombre de ruta de los archivos de tema de lenguaje de marcas de hipertexto.|
|Ver información|Información que describe los navegadores que se emplean en el conjunto de ayuda. los navegadores de calidad son: índice, índice y búsqueda de texto completo. otros navegadores incluyen el brillo y también los navegadores favoritos. Los datos relativos a los navegadores personalizados se adjuntan aquí más.|
<html>|Título del conjunto de ayuda|El \<title> se describe dentro del archivo helpset (.hs). Este título aparece en la parte superior de la mayoría de las ventanas y de las ventanas secundarias descritas en el archivo del conjunto de ayuda.| </html>
|Identificación del hogar|El título de la identificación (predeterminada) que se muestra cuando se llama al vigilante de asistencia sin indicar una identificación.|
|Presentación|Las ventanas en las que mostrar los temas de asistencia. Esta es una versión moderna del programa informático JavaHelp 2 que se muestra con más detalle debajo de \<presentation> .|
|Sub-conjuntos de ayuda|Esta área discrecional incorpora estáticamente otros conjuntos de ayuda utilizando la etiqueta. Los conjuntos de ayuda que muestra esta etiqueta se combinan naturalmente en el conjunto de ayuda que contiene la etiqueta. Se pueden encontrar más puntos de interés sobre la combinación en Blending Helpsets.|
|Implementación|Este segmento discrecional crea un registro que proporciona un mapeo de información clave para caracterizar la clase HelpBroker para utilizar dentro del método HelpSet.createHelpBroker. El registro también decide el visor de sustancia al cliente para un tipo de emulación determinado.

## Formato de archivo Java HS

Los archivos Java HS están en formato de archivo XML y se basan en la recomendación propuesta por el lenguaje de marcado extendido del World Wide Web Consortium (W3C) [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Esto significa que un archivo Java HS tiene un formato de archivo XML legible por humanos que se puede abrir en cualquier aplicación de lectura de XML.

### Ejemplo de formato de archivo Java HS

El siguiente es un ejemplo de un archivo de conjunto de ayuda a partir de [documentación de Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## Referencias
* [Archivo del conjunto de ayuda de Oracle Java](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Formato de archivo de script de Haskell

## ¿Qué es un archivo HS?

Un archivo con la extensión .hs es un archivo Haskell Script que está escrito en [Haskell](https://wiki.haskell.org/Haskell), un lenguaje de programación avanzado de código abierto puramente funcional. El código escrito en el archivo HS se basa puramente en funciones, a diferencia de [C](/es/programming/c/), [C++](/es/programming/cpp/) y similares, que siguen los principios de desarrollo rápido de software robusto y conciso. Haskell proporciona simultaneidad y paralelismo integrados junto con API ricas, generadores de perfiles y depuradores para producir aplicaciones flexibles y de alta calidad.

## Formato de archivo SA

Como cualquier lenguaje de programación, los archivos HS están escritos en formato de texto sin formato que es legible por humanos. Estos se pueden crear, editar y ver con cualquier herramienta de texto disponible. El archivo de código fuente .hs se compila con un compilador Haskell, generando el archivo binario ejecutable.

### Ejemplo de formato de archivo HS

El código se puede escribir en un archivo .hs y compilar usando un compilador Haskell como [GHC](https://haskell.org/ghc). La siguiente línea de código se guarda como `HelloWorld.hs` como se muestra en el siguiente ejemplo.

```
main = putStrLn "Hello, World!"
```

Esto se compila usando el comando:

```
$ ghc -o hello hello.hs
```
y el archivo ejecutable resultante se puede ejecutar como:

```
$ ./hello
```
Esto imprime el mensaje "¡Hola, mundo!" declaración a la salida.

## Referencias

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell en 5 sencillos pasos](https://wiki.haskell.org/Haskell_in_5_steps)


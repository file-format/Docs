{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - Archivo de lenguaje de marcado ColdFusion",
  "description" :"Obtenga información sobre qué es un archivo CFML y las API que pueden crear y abrir archivos CFML",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## ¿Qué es un archivo CFML?

Un archivo con extensión .cfml es un archivo de lenguaje de marcado ColdFusion que se utiliza para crear una página web. Se refiere a un conjunto de reglas utilizadas para definir cómo el programador desarrollará la aplicación ColdFusion. ColdFusion es un lenguaje de programación que se utiliza para crear aplicaciones web del lado del servidor rápidamente y con menos que otras tecnologías como [ASP](/es/web/asp/), [PHP](/es/web/php/), etc. Algunos de las aplicaciones que pueden abrir archivos CML incluyen Adobe ColdFusion 2018, Adobe ColdFusion Builder y Adobe Dreamweaver.

## Formato de archivo CFML - Más información

Los archivos CFML son archivos de marcado y contienen elementos web en forma de etiquetas. Estos son archivos de texto que se pueden abrir y editar en cualquier editor de texto. Los archivos CFML constan de varias etiquetas que son similares a [HTML](/es/web/html/) y generalmente se componen de una etiqueta de apertura y otra de cierre. Estas etiquetas también pueden contener uno o más atributos.

### Sintaxis de etiquetas

A continuación se muestra la sintaxis generalizada de las etiquetas CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

La mayoría de las etiquetas aceptan atributos y se definen de la siguiente manera.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Algunas de estas etiquetas también aceptan múltiples atributos con la siguiente sintaxis.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Ejemplo de código CFML

Aquí hay un ejemplo que usa una etiqueta CFML real: la etiqueta `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Referencias

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)


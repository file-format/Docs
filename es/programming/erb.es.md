{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "archivo", "extensión", "formato de archivo", "implementación de erb", "Guía de programación", "ejemplo de erb", "eRuby", "formato de archivo de eRuby", "script de lenguaje eRuby", " plantillas de eRuby", "idioma erb", "idioma ERB Ruby", "idioma eRuby" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - Archivo de idioma eRuby",
  "description":"Obtenga información sobre el formato de archivo ERB y las API que pueden crear y abrir archivos ERB",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## ¿Qué es un archivo ERB?

El lenguaje eRuby es un sistema de plantillas que incrusta Ruby en un documento de texto. El sistema de plantillas de eRuby combina el código Ruby y el texto sin formato para proporcionar control de flujo y sustitución de variables, lo que facilita su mantenimiento. A menudo se usa para incrustar código Ruby en un documento [HTML](/es/web/html/), similar a АSР, [JSР](/es/programming/jsp/) y [РHР](/es/programming/php/) y otros servidores. -Idiomas de escritura laterales. ERB Ruby suele generar páginas web.

El módulo de vista de Ruby on Rails es responsable de mostrar la respuesta o salida en un navegador. En su forma más simple, una vista puede ser una pieza de código HTML que tiene algo de contenido estático. Para la mayoría de las aplicaciones, tener contenido estático puede no ser suficiente. Muchas aplicaciones de Rails requerirán que el contenido dinámico creado por el controlador se muestre en su vista. Esto es posible mediante el uso de Embedded Ruby para generar plantillas que pueden contener contenido dinámico.

Embedded Ruby permite que el código Ruby se incruste en un documento de vista. Este código se reemplaza con el valor adecuado resultante de la ejecución del código en tiempo de ejecución. Pero, al tener la capacidad de incrustar código en un documento de vista, corremos el riesgo de salvar la clara separación presente en el marco MVС. Por lo tanto, es responsabilidad del desarrollador asegurarse de que haya una clara separación de responsabilidades entre los módulos de modelo, vista y controlador de la aplicación.



## Breve historia ##

Ruby fue diseñado a mediados de la década de 1990 por Yukihir® Mаtsumоtо. Yukihirо Matsumоtо es el padre de Ruby y en la comunidad de Ruby, es conocido como Matz'. Ruby script se introdujo inicialmente en 1995 y la primera versión de Ruby fue Ruby 95, que se lanzó en 1995.

Yukihirо Mаtsumоtо quería un lenguaje de programación totalmente orientado a objetos que pudiera usarse fácilmente como lenguaje de escritura. Entonces, diseñó el lenguaje eRuby. En una sesión de chat de Yukihirо Matsumоtо y Keiju Ishitshukа, se alistaron dos nombres para el lenguaje de programación que es "Сorаl" y "Ruby", luego Yukihirо Mаtsumоtо seleccionó el nombre "Ruby".


## Especificación técnica ##

El formato de archivo eRuby admite diferentes conceptos de enfoque de programación orientado a objetos como clase, herencia, abstracción, polimorfismo y encapsulación, etc. La característica del enfoque de programación orientada a objetos facilita el mantenimiento y el desarrollo. El script del lenguaje eRuby también es compatible con la característica del enfoque de programación procesal. En la programación de procedimientos, hay pasos específicos para que cada programa resuelva un problema en particular.

Las plantillas de eRuby proporcionan una amplia gama de bibliotecas integradas de clase enriquecida con las que los programadores pueden desarrollar cualquier aplicación o programa web de manera fácil y rápida. eRuby es un lenguaje de programación de propósito general o de propósito múltiple, lo que significa que puede ser utilizado por programadores para desarrollar diferentes tipos de aplicaciones y programas.

El lenguaje ERB Ruby es un lenguaje de programación simple y de código abierto y también puede modificarlo de acuerdo con los requisitos de su proyecto. Proporciona varios tipos de funciones y herramientas integradas. El idioma también proporciona la función de recolector de basura automático.

La codificación en eRuby es muy rápida en comparación con otros lenguajes de programación. Y también es un lenguaje de programación flexible, ya que permite a cada usuario modificar sus partes de acuerdo con sus requisitos. Es compatible con la función de herencia única y mezclas y también proporciona la función de escritura dinámica a sus usuarios. eRuby es un lenguaje de programación que distingue entre mayúsculas y minúsculas y tiene una gran comunidad de apoyo debido a su sensibilidad.


## Ejemplo de formato de archivo ERB ##

Los siguientes son los tipos de etiquetas en las plantillas ERB:

### Expresión ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Ejecución ###

```
<% %>
```

```
<ul>
<% 4.times do %>

  <li>list item</li>

<% end %>
</ul>
```

### Comentarios ###

```
<%# %>
```

```
<%# ruby code %>
```

### Otras etiquetas ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Ejemplo de clase ###

```
class ERBExample
  attr_accessor:variable1
  
  # using bind to access class variables
  def render()
    renderer.result(binding)
  end

  def initialize(variable1)
    @variable1 = variable1
  end

  # Expose private binding() method.
  def get_binding
    binding()
  end
end

example = ERBExample.new(variable1)
renderer = ERB.new(template)
puts output = renderer.result(example.get_binding)

```

## Referencia ##

* [ERB - por Wikipedia](https://en.wikipedia.org/wiki/ERuby)




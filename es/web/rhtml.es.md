{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","archivo rhtml", "formato de archivo rhtml", "tipo de archivo rhtml", "archivo", "tipo", "qué es un archivo rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Página HTML de Ruby",
  "description":"Obtenga información sobre el formato de archivo RHTML y las API que pueden crear y abrir archivos RHTML",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## ¿Qué es un archivo RHTML?

Un archivo con la extensión .rhtml es un archivo del lado del servidor [HTML](/es/web/html/) que contiene código Ruby o scripts. El código se ejecuta en el servidor utilizando Ruby on Rails que se ejecuta en el backend. Para aquellos que no conocen Ruby on Rails, es un marco completo para desarrollar aplicaciones web con bases de datos back-end basadas en el patrón Model-View-Control. En pocas palabras, RHTML es una combinación de HTML y Ruby donde el poder de los scripts/programación de Ruby está disponible para los desarrolladores web que usan etiquetas HTML.

## Formato de archivo RHTML

Los archivos RHTML se escriben en formato de texto sin formato como cualquier otro archivo web basado en texto. El código que se ejecutará se incluye dentro de `<% %>`, mientras que para la salida, el código se escribe dentro de declaraciones `<%= %>`.

## Ejemplo RHTML

El siguiente ejemplo utiliza la combinación más simple de HTML y Ruby on Rails para generar el nombre de cada producto de una lista de productos.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Referencias

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


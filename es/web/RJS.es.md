{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "RJS", "Archivo Ruby Javascript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Archivo Javascript Rubí",
  "description":"Obtenga información sobre el formato de archivo RJS y las API que pueden crear y abrir archivos RJS",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## ¿Qué es un archivo RJS?

Un archivo con extensión .rjs es una combinación de código Ruby y JavsScript que permite a los desarrolladores de Rails usar Ruby para producir código JavaScript dinámico. El código Ruby está incrustado en las funciones de Java y se compila en el servidor web que requiere que el motor Ruby se ejecute en el servidor. RJS es similar a [RHTML](/es/web/rhtml/); la única diferencia es que el lateral contiene código Ruby en [HTML](/es/web/html/) mientras que contiene código Ruby en funciones Javascript.

## Formato de archivo RJS

Los archivos RJS están codificados en texto sin formato como cualquier otro lenguaje de secuencias de comandos o programación. Cuando el cliente solicita una página de este tipo, el código Ruby se ejecuta en el servidor y solo se devuelve el código HTML y Javascript al navegador del cliente. La sintaxis del archivo RJS es similar a la combinación de la sintaxis de Ruby y JavaScript, de modo que solo el código de Ruby está incrustado en las funciones de JavaScript.

### Ejemplo de RJS

El siguiente ejemplo muestra un código Ruby simple de forma independiente y luego incrustado en una función de JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
y el siguiente es el RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Referencias

* [RJS](https://github.com/makevoid/rjs)


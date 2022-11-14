{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "archivo", "extensión", "formato de archivo", "lenguaje de programación NUT", "Guía de programación", "ejemplo NUT", "formato de archivo NUT", "lenguaje de ardilla", "archivo de extensión .nut ", "archivos NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Archivo de lenguaje de ardilla",
  "description":"Obtenga información sobre el formato de archivo NUT y las API que pueden crear y abrir archivos NUT",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## ¿Qué es un archivo NUT?

La NUT se refiere al archivo de formato de contenedor abierto NUT. Este formato de archivo NUT pertenece al lenguaje de programación conocido como Squirrel. Es un lenguaje de programación imperativo, de alto nivel y orientado a objetos que se utiliza principalmente en sistemas integrados y videojuegos.

El lenguaje de ardilla se considera un lenguaje de secuencias de comandos ligero que se puede ajustar fácilmente según el tamaño y el ancho de banda. Implica la ventaja del conteo automático de referencias y la gestión de basura en la memoria.

La sintaxis del lenguaje de ardilla atrae a los desarrolladores, ya que es similar a C e incluye la característica del lenguaje de secuencias de comandos. Pero aún así, tiene bastantes menos ventajas en comparación con otros lenguajes de programación más populares para este propósito.



## Breve historia ##

Fue diseñado por Alberto Demichelis en 2003. Sin embargo, en 2016 se lanzó una versión estable de este lenguaje. Fue diseñado bajo la licencia de zlib/libpng. En 2010 se cambió la licencia y se transfirió al MIT. Este lenguaje se considera como una versión inspirada de [LUA](/es/programming/lua/) (Lenguaje de programación). Hay una lista de sugerencias para el idioma anterior en el sitio web diseñado por Alberto para hacerlo más ventajoso.


## Especificación técnica ##

Las características y especificaciones del lenguaje de las ardillas son múltiples. Proporciona la facilidad de tipado dinámico, propiedad de delegación, varios usos de clases e interfaces. La sintaxis de este lenguaje tiene una similitud con la sintaxis del lenguaje C. Aplicaciones como Enduro/X (un servidor de aplicaciones de clúster) utilizan este lenguaje. Como Squirrel también se usa para videojuegos, algunos de ellos son OpenTTD, GTA IV, etc.

La versión estable del lenguaje es 3.0.7. Un conjunto de herramientas conocido como MirthKit utiliza el lenguaje de programación Squirrel para proporcionar un código abierto y multiplataforma para juegos bidimensionales. La naturaleza de este lenguaje es dinámica y la mayoría de las funciones son similares a [Python](/es/programming/py/), LUA, etc. También implica la implementación de una máquina virtual basada en registros. El rendimiento de Squirrel es más lento en comparación con LUA.

También hay otro tipo de archivo de extensión ".nut", por lo que debe mirar el tamaño del archivo para averiguar qué archivo NUT tiene. Los archivos NUT de Squirrel script son en su mayoría más pequeños que 1 MB, mientras que los archivos NUT de video suelen tener más de 1 MB de tamaño.


## Ejemplo de formato de archivo NUT ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Referencia ##

* [NUT - por Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))




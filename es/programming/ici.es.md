{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "archivo", "extensión", "formato de archivo", "implementación de ICI", "Guía de programación", "ejemplo de ICI", "lenguaje de programación de ICI", "módulos de ICI", "modelo de datos de ICI ", "documentación de ICI", "idioma ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Archivo de lenguaje de programación",
  "description":"Obtenga información sobre el formato de archivo ICI y las API que pueden crear y abrir archivos ICI",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## ¿Qué es un archivo ICI?

Un lenguaje de programación de propósito general que se interpreta y contiene varias funciones, como tipificación dinámica junto con tipos de datos flexibles, se conoce como lenguaje de programación ICI (no es un acrónimo). Se considera similar al lenguaje [Perl](/es/programming/pl/). Este lenguaje ICI comprende construcciones de control de flujo y también contiene algunos operadores del lenguaje C. No es un lenguaje orientado a objetos, pero algunas de las características de OOP se pueden lograr mediante un método de herencia específico conocido como superestructuras. Similar a [C](/es/programming/c), este lenguaje de programación ICI tiene la misma interfaz de sistema y una biblioteca estándar para funciones integradas.


## Breve historia ##

A fines de la década de 1980, Tim Long lo desarrolló como un lenguaje de programación interpretado de propósito general. La mayoría de las funciones de este lenguaje son similares a C y también puede lograr algunas de las funciones aplicando algunos métodos especiales. Este lenguaje es propiedad de dominio público y está disponible como lenguaje revendible y nadie está obligado a mencionar de dónde obtuvo el código fuente. La documentación de ICI está protegida por derechos de autor de Canon Information System Research Australia.

## Especificación técnica ##

Hay dos tipos de datos diferentes utilizados en este lenguaje. Estos dos son tipos de datos primitivos y agregados. Ambos incluyen diferentes expresiones según su composición predefinida en el idioma. Este lenguaje admite diferentes módulos, como anidados y subrutinas. Como algunas de sus propiedades son similares a las de Perl, tiene una integración estricta con las expresiones regulares.

Los conjuntos se limitan a ser heterogéneos y anidados. Estos conjuntos brindan soporte para operaciones de conjuntos de uso común, como Unión e Intersección, etc. Se usa principalmente como lenguaje para la implementación central de aplicaciones propiedad de organizaciones multinacionales.

Casi todos los tipos de programas pueden escribirse en este lenguaje y la mayoría de los programas específicos que involucran estructuras de datos complejas están escritos en el lenguaje de programación ICI. Las aplicaciones pueden implicar la implementación de ICI de manera que deban estar escritas en él. Las porciones funcionales de la aplicación pueden ser implementadas por los módulos de ICI. El lenguaje de ICI se parece un poco al lenguaje C, pero el modelo de datos de ICI es de un nivel bastante superior y diferente con tipos como diccionarios (estructura), conjuntos, matrices dinámicas, expresiones regulares y cadenas (reales).


## Ejemplo de formato de archivo ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Referencia ##

* [Lenguaje de programación ICI](http://atrn.org/ici/doc/ici.html)




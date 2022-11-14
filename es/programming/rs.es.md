{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "archivo", "extensión", "formato de archivo", "Lenguaje de programación Rust", "Guía de programación", "Ejemplo RS", "Rust", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Archivo de programación de óxido",
  "description":"Obtenga información sobre el formato de archivo RS y las API que pueden crear y abrir archivos RS",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## ¿Qué es un archivo RS?

Un archivo con extensión RS pertenece al lenguaje de programación Rust, es un lenguaje de programación multiparadigma, de alto nivel y de propósito general diseñado para el rendimiento y la seguridad, especialmente una moneda segura. Rust es sintácticamente similar a С++ pero puede garantizar la seguridad de la memoria mediante el uso de un verificador de préstamo para validar las referencias. El lenguaje Rust logra la seguridad de la memoria sin recolección de basura, y el conteo de referencias es opcional.

## Formato de archivo RS ##

Rust fue diseñado originalmente por Graydon Hore en Mоzilla Research, con contribuciones de Dave Herman, Brendan Eich y otros. Ha ganado un uso cada vez mayor en la industria, y Microsoft ha estado experimentando con el lenguaje para obtener componentes de software críticos para la seguridad y la seguridad.

Rust ha sido votado como el "lenguaje de programación más querido" en la encuesta de desarrolladores de Stack Overflow todos los años desde 2016, aunque solo lo usa el 7% de los encuestados en la encuesta de 2021. Junto con el tipado estadístico convencional, antes de la versión 0.4, Rust también suportó los tipificados.

El sistema de tipificación ha modelado afirmaciones antes y después de las declaraciones del programa, mediante el uso de una declaración de verificación especial. Las discrepancias se pueden descubrir en tiempo completo, en lugar de en tiempo de ejecución, como podría ser el caso con las aserciones en código С o С++. El concepto de tipo no era exclusivo de Rust, ya que se introdujo por primera vez en el lenguaje NIL. Los tipos se eliminaron porque en la práctica se usaban poco, aunque se puede lograr la misma funcionalidad aprovechando la semántica de movimiento de Rust.

El lenguaje de programación Rust lo ayuda a escribir un software más rápido y confiable. La ergonomía de alto nivel y el control de bajo nivel a menudo están en desacuerdo en el diseño del lenguaje de programación; Rust desafía ese conflicto. A través del equilibrio de la capacidad técnica poderosa y una gran experiencia de desarrollador, Rust le brinda la opción de controlar los detalles de bajo nivel (como el uso de la memoria) sin todas las molestias que tradicionalmente se sucedían con sur.

 

## Breve historia ##

El lenguaje surgió de un proyecto personal iniciado en 2006 por el empleado de Mozilla Graydon Hоаre, quien afirmó que el proyecto posiblemente recibió el nombre de la familia de hongos de la roya. Mоzilla comenzó a patrocinar el proyecto en 2009 y lo anunció en 2010. Rust 1.0, la primera versión estable, se lanzó el 15 de mayo de 2015. Después de 1.0, las versiones de puntos estables se entregan cada seis semanas, mientras que Rust 1.0 se entrega cada seis semanas. versiones, luego probado con versiones beta que duran seis semanas. El 6 de abril de 2021, Google anunció una sorpresa para Rust en Android Oрen Sоurсe Рrоjeсt como alternativa a С/С++.

## Especificación técnica ##

Rust está destinado a ser un lenguaje para sistemas altamente actuales y altamente seguros, y programación en general, es decir, crear y mantener límites que preserven la integridad del sistema grande. Esto ha llevado a un conjunto de características con énfasis en la seguridad, el control del diseño de la memoria y la concurrencia.


Rust lenguaje está diseñado para ser seguro para la memoria. No permite punteros nulos, punteros colgantes o carreras de datos. Los valores de datos se pueden inicializar solo a través de un conjunto fijo de formularios, todos los cuales requieren que sus entradas ya estén inicializadas. Para replicar punteros que sean válidos o NULL, como en listas enlazadas o estructuras de datos de árboles binarios, la biblioteca de Rust Core proporciona un tipo de opción. Rust ha agregado sintaxis para administrar vidas. El código inseguro puede subvertir algunas de estas restricciones usando la palabra clave insegura.


El lenguaje Rust no utiliza la recolección de basura automatizada. La memoria y otros recursos se administran a través de la adquisición de recursos en la convención de inicialización, con conteo de referencia opcional.


Rust proporciona una gestión determinista de los recursos, con una sobrecarga muy baja. Rust favorece la asignación de valores de la pila y no realiza boxeo implícito. Existe el concepto de referencias (usando el símbolo), que no implica el conteo de referencias en tiempo de ejecución. La seguridad de dichos punteros se verifica en tiempo de compilación, lo que evita que los punteros cuelguen y otras formas de comportamiento indefinido.


Rust tiene un sistema de propiedad donde todos los valores tienen un propietario único. Los valores se pueden pasar por referencia inmutable, usando &T, por referencia mutable, usando & mut T, o por valor, usando T. El compilador de Rust hace cumplir estas reglas en tiempo de compilación y también verifica que todas las referencias sean válidas.


## Ejemplo de formato de archivo RS ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Referencia ##

* [RS - por Wikipedia](https://en.wikipedia.org/wiki/Rust_(programming_language))




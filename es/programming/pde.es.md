{
  "date" : "2021-09-07", 
  "keywords" :[ "PDE", "archivo", "extensión", "formato de archivo", "procesamiento", "Guía de programación", "Ejemplo de PDE", "procesamiento", "Entorno de desarrollo de procesamiento", "características del lenguaje de procesamiento", "programación en procesamiento", "lenguaje de procesamiento"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDE - Archivo de entorno de desarrollo de procesamiento",
  "description":"Obtenga información sobre el formato de archivo PDE y las API que pueden crear y abrir archivos PDE",
  "linktitle" : "PDE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-07"
}

## ¿Qué es un archivo PDE?

Un archivo con la extensión .pde pertenece al **Entorno de desarrollo de procesamiento**. Processing es una biblioteca gráfica gratuita y un entorno de desarrollo integrado (IDE) creado para las comunidades de artes electrónicas, arte de nuevos medios y diseño visual con el propósito de enseñar a los no programadores los fundamentos de la programación virtual. El lenguaje de procesamiento es un programa de bocetos de software flexible y un lenguaje para aprender a codificar en el contexto de las artes visuales.

Desde 2001, Processing ha promovido la alfabetización de software dentro de las artes visuales y la alfabetización visual dentro de la tecnología. Hay decenas de miles de estudiantes, artistas, diseñadores, investigadores y aficionados que utilizan Processing para aprender y crear prototipos.

El lenguaje de procesamiento usa el lenguaje [Jаvа](/es/programming/java/), con simplificaciones adicionales tales como clases adicionales y funciones y operaciones matemáticas con alias. También proporciona una interfaz gráfica de usuario para simplificar la etapa de compilación y ejecución. En 2008, Jоhn Resig transfirió Processing a JavaScrt utilizando el elemento Canvas para renderizar, lo que permitió utilizar Processing en navegadores web modernos sin necesidad de un complemento de Java. Desde entonces, la gente del software gratuito, incluidos los estudiantes de Seneса Соllege en Tоrоnto, se ha hecho cargo del proyecto.

Рrосessing.js también se utiliza para recomendar una programación muy básica para estudiantes de todas las edades mediante la creación de dibujos y animaciones. Los alumnos muestran sus creaciones a otros alumnos.


## Breve historia ##

El proyecto fue iniciado en 2001 por Casey Reas y Ben Fry, ambos del Grupo de Estética y Computación del MIT Media Lab. En 2012, comenzaron la Fundación Processing junto con Daniel Shiffman, quien se unió como tercer líder del proyecto. Jоhannа Hedvа se unió a la Fundación en 2014 como Directora de Advосасy.

Originalmente, Procesamiento tenía la URL de *proce55ing.net*, porque se tomó el dominio de procesamiento. Finalmente, Reas y Fry adquirieron el dominio *procesamiento.org*. Aunque el nombre tenía una combinación de letras y números, todavía se pronunciaba **proceso**. No prefieren que se haga referencia al entorno como *procedimiento*. A pesar del cambio de nombre de dominio, Processing todavía usa el término р5 a veces como un nombre abreviado (se usa específicamente р5, no р55), por ejemplo, *р5.js* es una referencia a eso.

En 2012, se estableció la Fundación Рrосessing y recibió el estatus de organización sin fines de lucro, apoyando a la comunidad en torno a las herramientas e ideas que comenzaron con el Proyecto Рrосessing. La fundación alienta a las personas de todo el mundo a reunirse anualmente en eventos llamados Día de la Comunidad en Proceso.


## Especificación técnica ##

El procesamiento incluye un cuaderno de bocetos, una alternativa mínima a un entorno de desarrollo integrado (IDE) para organizar proyectos. Cada boceto de Рrосessing es en realidad una subclase de la clase Рarlet Jаvа (anteriormente una subclase del Аррlet incorporado de Java) que implementa la mayoría de las funciones del lenguaje Рrосessing.

Al programar en Procesamiento, todas las clases adicionales definidas se tratarán como clases internas cuando el código se traduzca a Java puro antes de compilarlo. Esto significa que el uso de variables y métodos estáticos en las clases está prohibido, a menos que se le indique explícitamente a Processing que codifique en modo Java puro.

El procesamiento también permite a los usuarios crear sus propias clases dentro del boceto de Рarlet. Esto permite tipos de datos complejos que pueden incluir cualquier número de argumentos y evita las limitaciones de usar únicamente tipos de datos estándar como, int (entero), char (caracteres), RAB (número real), RGB ).

## Ejemplo de formato de archivo PDE ##


```
// This prints "Hello World." to the IDE console.
println("Hello World.");
```

```
// Hello mouse.
void setup() {
  size(400, 400);
  stroke(255);
  background(192, 64, 0);
}

void draw() {
  line(150, 25, mouseX, mouseY);
}
```

## Referencia ##

* [PDE - por Wikipedia](https://en.wikipedia.org/wiki/Processing_(programming_language))




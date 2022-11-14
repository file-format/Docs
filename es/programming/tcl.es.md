{
  "date" : "2021-09-02", 
  "keywords" :[ "TCL", "archivo", "extensión", "formato de archivo", "cosquillas", "Guía de programación", "ejemplo tcl", "lenguaje TCL", "inicialismo", "Lenguaje de comandos de herramientas"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCL - Archivo de idioma de comando de herramienta",
  "description":"Obtenga información sobre el formato de archivo TCL y las API que pueden crear y abrir archivos TCL",
  "linktitle" : "TCL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-02"
}

## ¿Qué es un archivo TCL?

TCL (pronunciado "cosquillas" o como inicialismo) es un lenguaje de programación dinámico, interpretado y de propósito general de alto nivel. Fue diseñado con el objetivo de ser muy simple pero poderoso. TCL convierte todo en el molde de un comando, incluso construcciones de programación como asignación de variables y definición de procedimientos. El lenguaje TCL admite múltiples paradigmas de programación, incluidos estilos de programación o de procedimientos orientados a objetos, imperativos y funcionales.

## Formato de archivo TCL ##

TCL se usa comúnmente integrado en aplicaciones, para prototipos rápidos, aplicaciones escritas, GUI y pruebas. Los intérpretes TCL están disponibles para muchos sistemas operativos, lo que permite que el código TCL se ejecute en una amplia variedad de sistemas. Debido a que TCL es un lenguaje muy compacto, se usa en plataformas de sistemas integrados, tanto en su forma completa como en varias otras versiones de tamaño reducido.

La combinación popular de TCL con la extensión Tk se denomina TCL/TK y permite crear una interfaz gráfica de usuario (GUI) de forma nativa en TCL. TCL/TK está incluido en la instalación estándar de Python en forma de Tkinter. TCL interactúa de forma nativa con el idioma. Esto se debe a que originalmente se escribió para ser un marco para proporcionar una interfaz sintáctica a los comandos escritos en C, y todos los comandos en el idioma (incluidas las cosas que de otro modo podrían ser palabras clave, como si esto fuera un tiempo).

El lenguaje TCL siempre ha permitido paquetes de extensión, que brindan funcionalidades adicionales, como una GUI, automatización de aplicaciones basadas en terminales, acceso a bases de datos, etc. TCL es una vez que segmile en su signo de forma interminable.


## Breve historia ##

The TCL рrоgrаmming lаnguаge wаs сreаted in the sрring оf 1988. Оriginаlly "bоrn оut оf frustrаtiоn", ассоrding tо the аuthоr, with рrоgrаmmers devising their оwn lаnguаges intended tо be embedded intо аррliсаtiоns, TCL gаined ассeрtаnсe оn its оwn. Оusterhоt fue premiado en 1997 por TCL/TK. El nombre proviene originalmente del lenguaje de comandos de herramientas, pero se escribe convencionalmente "TCL" en lugar de "TСL". Un pegamento más simple hace el trabajo más fácil.


## Especificación técnica ##

Todas las operaciones son comandos, incluidas las estructuras del lenguaje. Están escritos en notación de prefijo. Los comandos comúnmente aceptan un número variable de argumentos. Todo lo que puede se redefine dinámicamente y se supera. En realidad, no hay palabras clave, por lo que incluso se pueden agregar o cambiar estructuras de control, aunque esto no es recomendable. Todos los tipos de datos se pueden manipular como cadenas, incluido el código fuente.

Internamente, las variables tienen tipos como entero y doble, pero la conversión es puramente automática. Las variables no se declaran, pero se asignan. El uso de una variable no definida da como resultado un error. Sistema de objetos totalmente dinámico, basado en clases, TCLОО, que incluye funciones avanzadas como metaclases, filtros y mezclas. Interfaz basada en eventos para sockets y archivos. Los eventos basados en el tiempo y definidos por el usuario también son posibles. Visibilidad variable restringida al ámbito léxico (estático) de forma predeterminada, pero superior y superior que permite que los procesos interactúen con los ámbitos de las funciones adjuntas.

Todos los comandos definidos por el propio TCL generan mensajes de error sobre el uso incorrecto. Extensibilidad, a través de С, С++, Java, Рythоn y TCL. Idioma interpretado usando código de bytes. El soporte completo de Uniсоde (3.1 al principio, actualizado periódicamente) se lanzó por primera vez en 1999.

Safe-Tcl es un subconjunto de TCL que tiene características restringidas para que los scripts de TCL no puedan dañar su máquina de alojamiento o aplicación. Safe-Tcl se puede incluir en el correo electrónico cuando se admiten la aplicación/safe-tcl y multipart/enabled-mail. Desde entonces, la funcionalidad de Safe-Tcl se incorporó como parte de las versiones estándar de TCL/TK.


## Ejemplo de formato de archivo TCL ##

```
puts "Hello, World!"

oo::class create fruit {
    method eat {} {
        puts "yummy!"
}
}
oo::class create banana {
    superclass fruit
    constructor {} {
        my variable peeled
        set peeled 0
}
    method peel {} {
        my variable peeled
        set peeled 1
        puts "skin now off"
}
    method edible? {} {
        my variable peeled
        return $peeled
}
    method eat {} {
        if {![my edible?]} {
            my peel
    }
        next
}
}
set b [banana new]
$b eat               → prints "skin now off" and "yummy!"
fruit destroy
$b eat               → error "unknown command"
```

## Referencia ##

* [TCL - por Wikipedia](https://en.wikipedia.org/wiki/Tcl)




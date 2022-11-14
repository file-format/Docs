{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "archivo", "extensión", "formato de archivo", "implementación de mrc", "Guía de programación", "ejemplo de mrc", "mIRC", "lenguaje de script de mIRC", "archivos de INI", " lenguaje de secuencias de comandos mSL", "lenguaje mIRC", "guiones mIRC", "lenguaje de secuencias de comandos" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - Archivo de lenguaje de script mIRC",
  "description":"Obtenga información sobre el formato de archivo MRC y las API que pueden crear y abrir archivos MRC",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## ¿Qué es un archivo MRC?

mIRC es un lenguaje de secuencias de comandos que está integrado como un cliente IRC (Internet Relay Chat) en el sistema operativo Windows. Proporciona una instalación de protección contra el spam para uso personal y de canal. Para brindar una mejor experiencia de compatibilidad con el usuario, este lenguaje de script mIRC permite la creación de ventanas de diálogo. Los archivos que contienen scripts, en su mayoría en formato de texto sin formato, se almacenan con la extensión MRC o como archivos de [INI](/es/system/ini/). Las funciones de este lenguaje se conocen como comandos e identificadores (cuando devuelven valor).

El lenguaje mIRC proporciona la carga de múltiples archivos de secuencias de comandos a la vez. Por otro lado, un archivo puede hacer que el otro ya no se use cuando se carga simultáneamente. Los comandos se guardan y pueden existir en IRC automáticamente. Los comandos y alias utilizados en este idioma no comprenden la precedencia de ninguno de los caracteres.

mIRC se usa ampliamente para hacer que los bots administren un canal automáticamente, pero también puede ser modificado por el lenguaje de programación mSL. Puede introducir muchas características nuevas como macros, capacidad de reproducción de música, pequeñas macros y funciones, juegos básicos o el funcionamiento de pequeñas aplicaciones.


## Breve historia ##

Este lenguaje de secuencias de comandos fue desarrollado por primera vez en 1995 por Khaled Adam Bey. El diseño del lenguaje de secuencias de comandos también fue creado por Khalid. El objetivo de este lenguaje era la programación dirigida por eventos. Inicialmente, la extensión de archivo utilizada para los archivos de este lenguaje de programación era .mrc e .ini. Además, fue desarrollado bajo la licencia de software propietario.

## Especificación técnica ##

Algunas funciones tienen scripts personalizados a través de este lenguaje mIRC y se conocen como alias. Cuando estos alias devuelven valores, se conocen como identificadores personalizados. Todas las variables contenidas en este lenguaje mIRC se escriben dinámicamente. Los scripts mIRC utilizan los sigilos. Otra característica de este lenguaje de secuencias de comandos son las ventanas emergentes. Los usuarios pueden llamar ventanas emergentes simplemente seleccionándolas. Los controles remotos se especifican para ciertos eventos. Los remotos son llamados cuando ocurre el evento relativo.

Los tokens delimitados por espacios se utilizan para dividir cada línea de código de este lenguaje. Hay algunas otras extensiones populares utilizadas para archivos mIRC como MDX (extensión de diálogo mIRC) y DCX (extensión de control de diálogo). Ambos son extensiones de diálogo y son comparativamente más populares. Las construcciones del lenguaje se denominan mediante la nomenclatura de este lenguaje de secuencias de comandos. El lenguaje mIRC involucra diferentes aspectos de un lenguaje de secuencias de comandos, como variables locales y globales, variables binarias, tablas hash y manejo de archivos.


## Ejemplo de formato de archivo MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/es/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Referencia ##

* [MIRC - por Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)




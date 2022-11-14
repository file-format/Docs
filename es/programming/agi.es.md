{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo AGI - Formato de archivo de interfaz de puerta de enlace Asterisk",
  "description":"Aprenda qué es el formato de archivo AGI con ejemplos y API que pueden crear y abrir archivos AGI",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## ¿Qué es un archivo AGI?

Un archivo AGI es un archivo de secuencia de comandos utilizado por el sistema de telefonía de código abierto, Asterisk. Contiene información que se puede utilizar para automatizar procesos y el plan de marcación de Asterisk. Usando archivos de script AGI, se pueden establecer conexiones con bases de datos relacionales como PostgreSQL o MySQL. Además, los scripts AGI también se pueden usar para acceder a otros recursos externos. Los scripts AGI pueden entregar el control del plan de marcación a un script AGI externo, lo que permite a Asterisk realizar tareas complejas.

## Formato de archivo AGI - Más información

Los archivos de script AGI se guardan como archivos de texto y se pueden abrir en cualquier editor de texto para realizar cambios.

### Patrón estándar de comunicación AGI

El script AGI carga las variables y sus valores enviados por Asterisk. Un aspecto común de estas variables es el siguiente.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Estas variables van seguidas de una línea en blanco enviada por Asterisk, que muestra que el script AGI puede tomar el control del plan de marcación ahora.

### Lenguaje de programación para archivos AGI Script

Los scripts AGI normalmente se pueden escribir en Perl, [PHP](/es/programming/php/), [C](/es/programming/c/), Pascal o Bourne Shell.

## Referencias

* [Guión AGI de Asterisk](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)


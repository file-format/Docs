{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Formato de archivo", "Abrir", "Leer", "Crear", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo HPGL y las API que pueden crear y abrir archivos HPGL",
  "title" :"Formato de archivo HPGL - ¡Aprende de los expertos en formato de archivo!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## ¿Qué es un archivo HPGL?

Un archivo HPGFL (Lenguaje de gráficos de Hewlett-Packard) contiene un conjunto de instrucciones para el control del plóter desarrollado por HP. Los plotters HP utilizan este archivo para dibujar e imprimir contenido vectorial y rasterizado en el papel.

### Comando HPGL

Un comando HPGL consta de lo siguiente.
* Una sección de comando del alfabeto de dos caracteres
* Una sección de parámetros
* Sección de terminador

Cada parámetro en el archivo debe dividirse con un separador en caso de múltiples parámetros.

### Ejemplo de comando HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Sistema coordinado

Los sistemas de coordenadas se componen de indicadores de medición bidimensionales para ubicar cualquier ubicación específica. El HPGL utiliza tanto el sistema de coordenadas del plóter como el del usuario para este propósito.

#### Sistema de coordenadas del trazador

Este sistema de coordenadas se utiliza para trazar dibujos basados en el movimiento del trazador. Una unidad XY típica de movimiento mínimo del trazador es 0,025 mm. El rango posible de cambios de dibujo con tipos de plotter.

#### Sistema de coordenadas del usuario

El sistema de coordenadas especificado por el usuario se puede configurar utilizando la escala y el origen. Estos se convierten en coordenadas de plóter mediante el comando IP y el comando SC. Las coordenadas del sistema de plóter se utilizan por defecto si no se realiza esta conversión.

## Formato de archivo HPGL
Los archivos HPGL están en formato ASCII (archivo de texto) y comienzan con unos pocos comandos de configuración. Esto configura ciertos parámetros para el plotter para el trazado. Un archivo HPGL típico tiene el siguiente aspecto.

|Comando|Significado
---|---|
|IN;|inicializar, iniciar un trabajo de trazado|
|IP;|establecer los puntos de escala (P1 y P2) en sus posiciones predeterminadas|
|SP1;|seleccionar bolígrafo 1|
|PU0,0;|levantar el lápiz y pasar al punto de inicio para la siguiente acción|
|PD100,0,100,100,0,100,0,0;|baje el lápiz y muévase a las siguientes ubicaciones (dibuje un cuadro alrededor de la página)|
|PU50,50;|Pluma arriba y moverse a las coordenadas X,Y 50,50|
|CI25;|dibujar un círculo de radio 25|
|SS;|seleccione el juego de caracteres estándar|
|DT*,1;|establezca el delimitador de texto en el asterisco, y no los imprima (el 1, que significa "verdadero")|
|PU20,80;|levantar la pluma y pasar a 20,80|
|LBHello World*;|dibujar una etiqueta|

## Referencias
* [HPGL por Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [Guía de referencia de HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)


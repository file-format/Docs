{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Archivo GCODE: ¿Qué es un archivo .gcode y cómo abrirlo?",
   "description":"Obtenga información sobre el formato de archivo GCODE y las API que pueden crear y abrir archivos GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-es-gcode",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## ¿Qué es un archivo GCODE?

Un **archivo GCODE** es un archivo de texto sin formato que contiene instrucciones para controlar máquinas herramienta computarizadas e impresoras 3D; El código G, o Código Geométrico, es un lenguaje utilizado para controlar los movimientos y acciones de máquinas **CNC (Control Numérico por Computadora)**; Las máquinas CNC incluyen fresadoras, tornos, enrutadores e impresoras 3D.

Los comandos de código G están escritos en una sintaxis específica que generalmente consta de letras y números; Cada comando indica a la máquina que realice una acción específica, como mover la herramienta a una posición particular, cambiar la herramienta o ajustar la velocidad.

El código G a menudo se genera mediante software **CAM (fabricación asistida por computadora)**; El software CAM toma un modelo 3D o un diseño 2D y genera las correspondientes trayectorias de herramientas e instrucciones de código G; Luego, el archivo de código G se carga en una máquina CNC o en una impresora 3D para su ejecución.

Los archivos de código G suelen tener la extensión de archivo .nc o .gcode, por ejemplo, program.nc o print.gcode.

## Estructura del archivo GCODE:

Los archivos GCODE son archivos de texto sin formato y cada línea contiene un comando específico; Estos comandos van desde controlar el movimiento de la máquina hasta ajustar la temperatura, la velocidad y otros parámetros cruciales para la fabricación de un objeto.

La sintaxis de GCODE implica una combinación de letras y números; cada uno representa una acción o parámetro distinto; Los comandos comunes incluyen G0 y G1 para movimiento, M3 y M5 para control del husillo, y S y F para ajustes de velocidad y avance, respectivamente.

## Generación GCODE:

El software de corte, como **Simplify3D** y **Slic3r**, traduce dibujos de diseño asistido por computadora (CAD) a GCODE; El software CAD se utiliza para crear modelos 3D, que luego se exportan en formatos como STL; el software de corte toma estos modelos y genera un archivo GCODE que especifica detalles como la altura de la capa, la velocidad de impresión y la configuración de temperatura.

## Ejemplo de código G

A continuación se muestra un ejemplo sencillo de código G para mover una máquina CNC:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## ¿Cómo abrir un archivo GCODE?

Para abrir un archivo de código G puede utilizar diferentes tipos de software según sus necesidades.

Si generó código G para impresora 3D; puedes abrirlo usando el software que viene con tu impresora 3D o un software de corte dedicado; los ejemplos incluyen **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** o **Repetier-Host**; Estos programas suelen tener una interfaz fácil de usar que le permite cargar y visualizar código G.

Los archivos GCODE son texto sin formato, por lo que puedes abrirlos con cualquier editor de texto; Los editores de texto comunes incluyen **Bloc de notas (en Windows)**, **TextEdit (en macOS)** o **Gedit (en Linux)**; simplemente **haga clic derecho** en el archivo de código G, elija **Abrir con** y seleccione un editor de texto.


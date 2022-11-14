{
  "date" : "2021-06-24",
  "keywords" :[ "archivo bat", "qué es un archivo bat", "archivo", "ejemplo de archivo bat", "extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo BAT y las API que pueden crear y abrir archivos BAT",
  "title" :"BAT - Formato de archivo por lotes",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## ¿Qué es un archivo BAT?
Un archivo BAT se conoce como un archivo por lotes que se ejecuta con DOS y todas las versiones de Windows, en cmd.exe. Consiste en una serie de comandos de línea en texto sin formato que ejecuta el intérprete de línea de comandos para realizar diferentes tareas, como ejecutar utilidades de mantenimiento dentro de Windows o iniciar programas típicos. Un archivo por lotes puede incluir cualquier comando que el intérprete pueda aceptar de forma interactiva y usar la estructura de código que permite la bifurcación y el bucle condicionales como está escrito en el archivo por lotes.
## formato de archivo BAT
Un formato de archivo BAT es simplemente un script incorporado para automatizar secuencias de comandos que son de naturaleza repetitiva. El término "lote" se utiliza para el procesamiento por lotes. Se puede considerar como "ejecución no interactiva". Por lo tanto, es posible que un archivo por lotes no procese un lote de datos múltiples. En el antiguo sistema operativo de disco (DOS), el archivo por lotes se ejecutaba en la interfaz de línea de comandos escribiendo el nombre del archivo y la extensión .bat. El anterior sistema operativo basado en la interfaz gráfica de Microsoft, como Microsoft Windows, dependía de DOS. Los usuarios tenían que usar DOS para realizar operaciones típicas como reparar, optimizar o reinstalar Windows. Más tarde, Microsoft introdujo Windows NT, que no dependía del sistema operativo DOS. Por lo tanto, los archivos por lotes se pueden ejecutar mediante el Símbolo del sistema o **cmd.exe** en los sistemas operativos modernos de Microsoft.
### Parámetros del archivo por lotes
El símbolo del sistema admite una serie de variables especiales como **%0, %1 a %9** para hacer referencia al nombre y la ruta del trabajo por lotes y los nueve parámetros de llamada desde dentro del trabajo por lotes. Los parámetros inexistentes se reemplazan por una cadena de longitud cero. Aunque se pueden usar de manera similar a las variables de entorno, pero no se guardan en el entorno. Microsoft e IBM se refieren a estas variables como parámetros de reemplazo, mientras que Novell, Digital Research y Caldera introdujeron el término variables de reemplazo para ellos.

Aquí hay algunos comandos útiles de archivos por lotes:
| Comando | Descripción |
------|------------|
| VER | Este comando por lotes muestra la versión de MS-DOS que está utilizando. |
|ASOC| Este es un comando por lotes que asocia una extensión con un tipo de archivo (FTYPE), muestra las asociaciones existentes o elimina una asociación. |
|CD| Este comando por lotes ayuda a realizar cambios en un directorio diferente o muestra el directorio actual. |
|CLS| Este comando por lotes borra la pantalla. |
|COPIAR| Este comando por lotes se usa para copiar archivos de una ubicación a otra. |
|DEL| Este comando por lotes elimina archivos y no directorios. |
|DIR| Este comando por lotes enumera el contenido de un directorio. |
|FECHA| Este comando por lotes ayuda a encontrar la fecha del sistema. |
|ECO| Este comando por lotes muestra mensajes o activa o desactiva el eco del comando. |
|SALIR| Este comando por lotes sale de la consola de DOS. |
|MD| Este comando por lotes crea un nuevo directorio en la ubicación actual. |
|MOVER| Este comando por lotes mueve archivos o directorios entre directorios. |
|RUTA| Este comando por lotes muestra o establece la variable de ruta. |
|PAUSA| Este comando por lotes solicita al usuario y espera a que se ingrese una línea de entrada. |
|AVISO| Este comando por lotes se puede usar para cambiar o restablecer el indicador cmd.exe. |
|RD| Este comando por lotes elimina directorios, pero los directorios deben estar vacíos antes de poder eliminarlos. |
|REN| Renombra archivos y directorios |
|REM| Este comando por lotes se usa para comentarios en archivos por lotes, evitando que se ejecute el contenido del comentario. |
|INICIO| Este comando por lotes inicia un programa en una nueva ventana o abre un documento. |
|HORA| Este comando por lotes establece o muestra la hora. |
|TIPO| Este comando por lotes imprime el contenido de un archivo o archivos en la salida. |
|VOLUMEN| Este comando por lotes muestra las etiquetas de volumen. |
|ATRIBUIR| Muestra o establece los atributos de los archivos en el directorio actual |
|CHKDSK| Este comando por lotes verifica el disco en busca de problemas. |
|ELECCIÓN| Este comando por lotes proporciona una lista de opciones al usuario. |
|CMD| Este comando por lotes invoca otra instancia del símbolo del sistema. |
|COMP| Este comando por lotes compara 2 archivos según el tamaño del archivo. |
|CONVERTIR| Este comando por lotes convierte un volumen del sistema de archivos FAT16 o FAT32 al sistema de archivos NTFS. |
|CONSULTA DEL CONDUCTOR| Este comando por lotes muestra todos los controladores de dispositivos instalados y sus propiedades. |
|AMPLIAR| Este comando por lotes extrae archivos de archivos comprimidos .cab. |
|ENCONTRAR| Este comando por lotes busca una cadena en archivos o entrada, generando líneas coincidentes. |
|FORMATO| Este comando por lotes formatea un disco para usar un sistema de archivos compatible con Windows, como FAT, FAT32 o NTFS, sobrescribiendo así el contenido anterior del disco. |
|AYUDA| Este comando por lotes muestra la lista de comandos proporcionados por Windows. |
|CONFIGURACIÓNIP| Este comando por lotes muestra la configuración de IP de Windows. Muestra la configuración por conexión y el nombre de esa conexión. |
|ETIQUETA| Este comando por lotes agrega, establece o elimina una etiqueta de disco. |
|MÁS| Este comando por lotes muestra el contenido de un archivo o archivos, una pantalla a la vez. |
|NETO| Proporciona varios servicios de red, según el comando utilizado. |
|PING| Este comando por lotes envía paquetes de "eco" ICMP/IP a través de la red a la dirección designada. |
|APAGAR| Este comando por lotes apaga una computadora o cierra la sesión del usuario actual. |
|ORDENAR| Este comando por lotes toma la entrada de un archivo fuente y ordena su contenido alfabéticamente, de la A a la Z o de la Z a la A. Imprime la salida en la consola. |
|SUSTITUIR| Este comando por lotes asigna una letra de unidad a una carpeta local, muestra las asignaciones actuales o elimina una asignación. |
|INFOSISTEMA| Este comando por lotes muestra la configuración de una computadora y su sistema operativo. |
|TAREA| Este comando por lotes finaliza una o más tareas. |
|LISTA DE TAREAS| Este comando por lotes enumera las tareas, incluido el nombre de la tarea y la identificación del proceso (PID). |
|XCOPIAR| Este comando por lotes copia archivos y directorios de una manera más avanzada. |
|ÁRBOL| Este comando por lotes muestra un árbol de todos los subdirectorios del directorio actual a cualquier nivel de recursividad o profundidad. |
|FC |Este comando por lotes enumera las diferencias reales entre dos archivos. |
|DISKPART |Este comando por lotes muestra y configura las propiedades de las particiones de disco. |
|TITLE |Este comando por lotes establece el título que se muestra en la ventana de la consola. |
|CONFIGURAR | Muestra la lista de variables de entorno en el sistema actual. |

## Ejemplo de archivo BAT
Los scripts por lotes generalmente se guardan como archivos de texto simples; que contienen comandos que se ejecutan en una secuencia. Estos archivos se guardan con la extensión .bat; reconocido y ejecutado usando el software **Command Interpreter**. Este software está disponible de forma nativa en Microsoft Windows con el nombre **cmd.exe**.

Aquí hay una secuencia de comandos por lotes de muestra que elimina todos los archivos en el directorio actual:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Referencias

* [Secuencia de comandos por lotes - Guía rápida](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Archivo por lotes - por Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


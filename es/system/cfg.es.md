{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "extensión", "archivo", "formato", "sistema", "configuración", "ajustes", "programas", "ordenador", "aplicación" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Formato de archivo",
  "description":"Obtenga información sobre el formato de archivo CFG y las API que pueden crear y abrir archivos CFG",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## ¿Qué es un archivo CFG? ##

Un archivo con una extensión .cfg es un tipo de archivo de "configuración". Es un tipo de archivo de uso popular y se utiliza para almacenar información sobre la configuración y la configuración de los programas informáticos. La mayoría de los tipos de archivos CFG se almacenan en formato de texto y no deben abrirse manualmente, sino que deben abrirse con un editor de texto. Sin embargo, existen diferentes tipos de archivos CFG, que difieren en el formato con el que se almacena la información. Las funciones que ofrecen los archivos CFG varían de una aplicación a otra. Algunas aplicaciones informáticas permiten a los usuarios modificar o desarrollar la sintaxis de sus archivos de configuración mediante el uso de interferencias gráficas, mientras que otras solo permiten modificaciones mediante un editor de texto. Después de modificar estos archivos, los usuarios pueden indicarle a la aplicación que vuelva a leer estos archivos y aplique las modificaciones al sistema.


## Formato de archivo CFG ##

Los archivos CFG son compatibles con varios sistemas operativos, como Unix y sistemas operativos similares a Unix, MS-DOS, macOS, Microsoft Windows e IBM OS/2. El formato en que estos archivos se almacenan y utilizan en cada uno de estos sistemas operativos varía. La mayoría de los sistemas utilizan y almacenan estos archivos en un formato de texto sin formato editable y legible por humanos, mientras que otros almacenan en un formato más complejo, según el uso de los archivos y los requisitos del sistema operativo.

En los sistemas operativos Unix y similares a Unix, la mayoría de los archivos CFG se utilizan varios estilos de formato diferentes para los archivos CFG, sin embargo, el formato más común es un formato de texto sin formato fácil de leer, y casi todos los formatos permiten hacer y editar comentarios. Las extensiones de archivo más comunes para archivos CFG en estos sistemas operativos son CNF, CONF, CF e INI.

En el sistema operativo MS-DOS, inicialmente solo había un formato de archivo de configuración, a saber, texto sin formato, sin embargo, MS-DOS 6 trajo consigo la introducción de un formato de archivo de configuración INI.

macOS utiliza un archivo de configuración de estilo de formato de lista de propiedades estándar.

En Microsoft Windows, los archivos de configuración de estilo INI de texto sin formato eran una fuente importante de almacenamiento y edición de información; sin embargo, se introdujo un nuevo sistema de base de datos en 1993, lo que provocó una disminución en el uso de archivos de configuración en Microsoft Windows después de 1993.


## CFG Ejemplo ##

A continuación se puede ver un archivo CFG de muestra:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```

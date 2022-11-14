{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Obtenga más información sobre el formato de archivo PCL y las API que pueden crear y abrir archivos PCL",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PCL? ##

PCL son las siglas de Printer Command Language, que es un lenguaje de descripción de página introducido por Hewlett Packard (HP). HP creó PCL para proporcionar una forma eficiente de controlar las funciones de la impresora en muchos dispositivos de impresión diferentes. El formato se desarrolló originalmente para las impresoras matriciales y de inyección de tinta de HP, pero con el paso del tiempo ha formado parte de varias impresoras térmicas, matriciales y de páginas. El formato se sometió a varias revisiones diferentes, lo que dio como resultado diferentes versiones en las que cada versión se mejoró para satisfacer las exigencias del tiempo con respecto a las funciones de control de la impresora. Hoy en día, PCL es el lenguaje de impresión más difundido en el último mercado de impresoras.

## Versiones PCL ##

Las versiones PCL difieren en funcionalidad (por ejemplo, soporte de tipo de fuente: fuentes de mapa de bits, fuentes escalables (Intellifonts, fuentes TrueType), métodos de compresión de gráficos rasterizados, soporte de gráficos HP-GL/2).

**PCL 1:** alrededor de 1980: la funcionalidad de impresión y espacio es el conjunto básico de funciones proporcionadas para una salida de estación de trabajo simple, conveniente y de un solo usuario.

**PCL 2:** alrededor de 1980: la funcionalidad EDP (procesamiento electrónico de datos)/transacción es un superconjunto de PCL 1. Se agregaron funciones para la impresión de sistema multiusuario de propósito general.

**PCL 3**: 1984: la funcionalidad de procesamiento de textos de Office es un superconjunto de PCL 2. Se agregaron funciones para la producción de documentos de oficina de alta calidad y se aumentó el ppp hasta 300 ppp. Permitió el uso de un número limitado de fuentes y gráficos de mapa de bits y admitió HP-GL. PCL 3 fue ampliamente imitado por otros fabricantes de impresoras y estas empresas lo denominaron "Emulación LaserJet Plus".
(Impresoras: familia HP DeskJet, impresora serie HP LaserJet, impresora serie HP LaserJet Plus)

**PCL3+:** Utilizado por la familia de impresoras DeskJet y DesignJet.

**PCL3c:** Utilizado por la familia de impresoras DeskJet y DesignJet.

**PCL3e**: utilizado por la familia de impresoras DeskJet y DesignJet. Ahora también se usa en PhotoSmart.

**PCL3GUI**: Utiliza RTL y es utilizado por la familia de impresoras DeskJet y DesignJet.

**PCLSLEEK**: Utiliza RTL y es utilizado por la familia de impresoras DeskJet y DesignJet.

**PCL 4**: 1985: la funcionalidad de formato de página es un superconjunto de PCL 3. Macros compatibles, fuentes de mapas de bits más grandes y gráficos. (Impresoras: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990: la funcionalidad de publicación de Office es un superconjunto de PCL 4. Las nuevas capacidades de publicación incluyen escalado de fuentes y gráficos HP-GL/2 (vectoriales). (Impresoras: HP LaserJet III)

**PCL 5e:** 1994: esta es una revisión importante que incluye nuevas características como el sistema de compresión adaptable, codificación de caracteres de 2 bytes, soporte para fuentes vectoriales y comandos de configuración bidireccional. Incluye operaciones lógicas (corresponde a GDI ROP) para mejorar el soporte de Windows antes de las rutas de recorte. (Impresoras: HP LaserJet 4)

**PCL 5j:** Nuevas funciones, como compatibilidad con caracteres de 2 bytes para fuentes escalables residentes en japonés, escritura vertical, tamaños de papel en japonés y cadenas tipográficas. (Impresoras: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Se agregaron soporte de color y operaciones lógicas a PCL5. PCL5c es anterior a PCL5e. Algunos modelos también admiten trazados de recorte. (Impresoras: HP Color LaserJet, HP PaintJet 300 XL (primera impresora con PCL5c), HP DeskJet 1200C/1600C (estos números de modelo se han reutilizado y los modelos más nuevos no son PCL 5c)

**PCL 5ce:** Admite tipos de letra escalables Agfa Microtype. (Impresoras: Impresora HP 2500c Pro)

**PCL 6 / XL:** 1996 - PCL 6 o PCL XL es un nuevo formato introducido en 1995, que no es compatible con ninguna versión anterior de PCL. (Impresoras: HP LaserJet 5, 5M y 5N)

## Descripción general de PCL 6 ##

HP presentó PCL 6 en 1996, que fue la siguiente evolución del lenguaje PCL y tecnologías relacionadas. Tiene los siguientes componentes:

**PCL 6 mejorado:** proporciona una versión optimizada para imprimir desde interfaces gráficas de usuario (GUI) como MS Windows y OS/2

**Estándar PCL 6:** proporciona compatibilidad retroactiva completa con impresoras HP LaserJet anteriores

**Síntesis de fuentes PCL:** proporciona fuentes escalables, gestión de fuentes y almacenamiento de formularios y fuentes.

La versión extendida PCL XL está más cerca de GDI que muchas aplicaciones usan. Se asegura de que se realicen menos traducciones, lo que da como resultado mayores capacidades WYSIWYG y un mejor rendimiento con aplicaciones que admiten escapes implementados por el controlador mejorado. Es posible que la salida del controlador mejorado (PCL XL) no sea la misma que la salida del controlador estándar. Si la salida no es la esperada, elija el controlador estándar (PCL5e) en su lugar.

Los comandos PCL 6 Enhanced están diseñados para adaptarse de manera óptima a los requisitos de impresión de gráficos para aplicaciones basadas en GUI. En la mayoría de los casos, para cada comando de impresión de gráficos que una GUI desea ejecutar, existe un comando PCL 6 mejorado coincidente. Esto reduce el número de comandos necesarios para describir una página de gráficos. Cada comando en PCL 6 Enhanced está diseñado para requerir una mínima transferencia de datos desde la PC host a la impresora. Esto reduce la cantidad de datos necesarios para describir una página.

El sistema de impresión de Windows para la mayoría de las impresoras HP LaserJet proporciona dos controladores independientes: estándar y mejorado. El controlador estándar proporciona compatibilidad con versiones anteriores mediante el uso de comandos PCL 6 estándar (PCL5e) para imprimir páginas de texto simple o texto y gráficos combinados. El controlador mejorado utiliza los comandos PCL 6 mejorados que se han optimizado para imprimir páginas con gráficos complejos.

## Revisiones de clase PCL 6 ##

#### Clase 1.1 ####

**Herramientas de dibujo:** Admite líneas de dibujo, arcos/elipses/cuerdas, rectángulos (redondeados), polígonos, rutas Bézier, rutas recortadas, imágenes de trama, líneas de exploración, operaciones de trama.
**Manejo de color:** Admite paletas de 1/4/8 bits, espacio de color RGB/gris. Admite patrones de medios tonos personalizados (máx. 256 patrones).
**Compresión:** Admite RLE.
**Unidades de medida:** Pulgada, milímetro, décima de milímetro.
**Manejo de papel:** Admite conjuntos personalizados o predefinidos de tipos de papel, incluidos Carta común, Legal, A4, etc. Puede elegir papel de alimentación manual, bandejas, casetes. El papel se puede imprimir a dos caras horizontal o verticalmente. El papel se puede orientar en vertical, horizontal o rotación de 180 grados de los dos anteriores.
**Fuente:** admite fuentes de mapa de bits o TrueType, puntos de código de 8 o 16 bits. La elección del conjunto de caracteres utiliza un código de conjunto de símbolos diferente al de PCL 5. Cuando se utiliza una fuente de mapa de bits, muchos comandos de escala no están disponibles. Cuando se utiliza la fuente TrueType, los descriptores de longitud variable, los bloques de continuación no son compatibles. La fuente del contorno se puede rotar, escalar o cortar.

#### Clase 2.0 ####

**Compresión:** Se agregó una compresión JPEG patentada llamada JetReady.
**Manejo de papel:** Los medios se pueden redirigir a diferentes bandejas de salida (hasta 256). Se agregaron tamaños de medios preestablecidos A6 y B6 japonés. Se agregó el preajuste de tercer casete, 248 fuentes de medios de bandeja externa.
**Fuente:** El texto se puede escribir verticalmente.

#### Clase 2.1 ####

**Manejo de color:** Función de coincidencia de color agregada.
**Compresión:** Se agregó Delta Row.
**Manejo del papel:** La orientación y el tamaño del papel son opcionales al declarar una página nueva. Se agregaron tipos de papel B5, JIS 8K, JIS 16K, JIS Exec.

#### Clase 3.0 ####

**Manejo de color:** Permite usar diferentes configuraciones de medios tonos para gráficos vectoriales o rasterizados, texto. Admite medios tonos adaptativos.
**Protocolo:** Admite el paso de PCL, lo que permite que las secuencias de PCL 6 utilicen las características de PCL 5. Sin embargo, algunos estados de PCL 6 no se conservan cuando se utiliza esta función.
**Fuente:** Admite fuentes PCL.
**Visor/Convertidor:** PCLReader (software gratuito) puede ver, convertir o imprimir cualquier nivel de PCL 6 (incluido JetReady) en cualquier impresora.

## Referencias ##

* [PCL - Por Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)


{
"fecha": "2023-07-20",
   "keywords":[
"PAPELERA",
"Archivo BIN",
"archivo",
"Extensión de archivo BIN",
"extensión",
"archivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo BIN: archivo codificado MacBinary",
   "description":"Obtenga más información sobre el formato BIN y las API que pueden crear y abrir archivos BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
"parent": "compresión"
}
},
"último mod": "2023-07-20"
}

## ¿Qué es un archivo BIN?

Un archivo BIN, en el contexto de las computadoras Macintosh, puede referirse a un archivo guardado en formato MacBinary. MacBinary es un formato de archivo diseñado específicamente para transferir archivos de Macintosh a través de Internet, correo electrónico, FTP o medios portátiles. El propósito de MacBinary es preservar la estructura completa de archivos y los atributos de los archivos de Macintosh, incluidos tanto la bifurcación de datos como la bifurcación de recursos, dentro de un solo archivo.

El formato MacBinary logra esto al encapsular la bifurcación de recursos y la bifurcación de datos del sistema de archivos jerárquico (HFS) de Macintosh en un archivo comprimido. También incluye un encabezado del buscador que contiene metadatos importantes sobre el archivo. Al combinar todos estos componentes en un solo archivo, MacBinary garantiza que el archivo conserve su integridad y pueda transferirse y compartirse fácilmente entre diferentes plataformas.

Con los avances en los sistemas de archivos y protocolos de transferencia de archivos de Apple, el uso de archivos BIN y formato MacBinary se ha vuelto menos común. La introducción de formatos de archivo como ZIP y la transición a sistemas de archivos más modernos, como HFS+ y APFS, han reducido la necesidad de archivos codificados en MacBinary. Estos sistemas de archivos más nuevos proporcionan formas más eficientes de manejar atributos de archivos, bifurcaciones de recursos y bifurcaciones de datos, lo que hace que el formato MacBinary sea menos necesario en el panorama informático actual.

## Formato de archivo BIN - Más información

En los primeros días de las computadoras Macintosh, los archivos se almacenaban en dos "bifurcaciones" separadas debido a limitaciones de datos. La "bifurcación de recursos" contenía datos estructurados, mientras que la "bifurcación de datos" contenía datos no estructurados. Si bien el sistema operativo Mac clásico trataba estas bifurcaciones como un solo archivo, la transferencia de archivos a sistemas que no eran Mac generaba una pérdida de datos porque no reconocían las bifurcaciones como una sola entidad. Para solucionar este problema, el formato MacBinary fue creado por personas como los hermanos Dennis, Harry Chesley e Yves Lempereur. MacBinary comprimió y combinó las bifurcaciones en un solo archivo, conocido como archivo BIN, para transferirlo a sistemas que no sean Mac. Al regresar al sistema operativo Mac, las bifurcaciones se separarían nuevamente. Con la transición del HFS basado en bifurcaciones en la década de 2000, el uso del formato MacBinary disminuyó significativamente. Hoy en día, es raro encontrar un archivo BIN codificado en MacBinary, a menos que encuentre un archivo antiguo en un sistema que no sea Mac o descargue uno de Internet.

El formato MacBinary ha pasado por varias versiones a lo largo del tiempo para adaptarse a los cambios en los sistemas Macintosh y el manejo de archivos. Estas son algunas de las diferentes versiones del formato MacBinary:

- **MacBinary I:** La versión inicial de MacBinary, introducida a finales de los años 1980. Combinó la bifurcación de recursos y la bifurcación de datos en un único archivo binario, lo que permitió la transferencia multiplataforma de archivos Macintosh.

- **MacBinary II:** Esta versión, lanzada a principios de la década de 1990, mejoró el formato MacBinary original al agregar información adicional, como el tipo de archivo y los códigos de creador, al encabezado del archivo binario. Estos códigos ayudaron a mantener la integridad y la identificación de los archivos de Macintosh durante la transferencia.

- **MacBinary III:** El formato MacBinary III, introducido a mediados de la década de 1990, mejoró aún más las versiones anteriores al incluir metadatos adicionales, como el nombre del archivo y las fechas de creación y modificación del archivo, en el encabezado del archivo binario. Esto permitió una preservación más completa de los atributos de los archivos de Macintosh durante la transferencia.

- **MacBinary IV:** MacBinary IV fue desarrollado para abordar problemas de compatibilidad con el sistema operativo emergente Mac OS X a principios de la década de 2000. Incorporó cambios para adaptarse a la nueva estructura y atributos del sistema de archivos introducidos en Mac OS X.

## ¿Cómo abrir un archivo BIN?

Los archivos BIN codificados en MacBinary se pueden abrir utilizando varias utilidades de compresión. Para los usuarios de macOS, la **Utilidad Apple Archive** es una opción adecuada. Los usuarios de Windows pueden utilizar software como **Smith Micro StuffIt Deluxe** para extraer el contenido de un archivo BIN codificado en MacBinary. Otra opción para los usuarios de macOS es **The Unarchiver**, que es una herramienta versátil capaz de manejar múltiples formatos de archivos, incluido MacBinary.

Es importante tener en cuenta que la extensión de archivo .bin se utiliza en varios formatos de archivo, no solo en MacBinary. Por lo tanto, si encuentra un archivo BIN que no se puede abrir con las utilidades antes mencionadas, es posible que se guarde en un formato diferente. En tales casos, es posible que necesite identificar el formato de archivo específico y utilizar el software o utilidad adecuada diseñada para ese formato para acceder al contenido del archivo.

## Otros archivos BIN

Aquí hay otros tipos de archivos que usan la extensión de archivo **.bin**.

- [BIN - Archivo de imagen de disco binario](/es/disc-and-media/bin/)
- [BIN - Archivo ejecutable Unix](/es/executable/bin/)
- [BIN - Archivo de políticas de TI de BlackBerry](/es/settings/bin/)
- [BIN - ROM del juego Sega Genesis](/es/juego/bin/)
- [BIN - Imagen del BIOS de PSX PlayStation](/es/game/bin-pcsx/)

## Referencias

* [MacBinario](https://en.wikipedia.org/wiki/MacBinary)


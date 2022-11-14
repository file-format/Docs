{
  "date" : "2021-08-31",
  "keywords" :[ "archivo xbe", "formato de archivo xbe", "qué es un archivo xbe", "archivo", "ejemplo xbe", "extensión de archivo xbe","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo XBE y las API que pueden crear y abrir archivos XBE",
  "title" :"XBE - Archivo de paquete de aplicación iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## ¿Qué es un archivo XBE?
Un archivo con extensión .xbe es una aplicación ejecutable de un disco de videojuego de Xbox. Los archivos XBE son los archivos principales que se ejecutan en el sistema Xbox y no se supone que se abran normalmente en una computadora, pero se pueden abrir en una PC usando un programa de emulación de Xbox. Estos archivos generalmente son creados por desarrolladores de juegos y luego firmados por Microsoft. La estructura de archivos es similar a los archivos de Windows PE, pero se aplican algunos cambios importantes según la configuración de XBox para que se pueda ejecutar en XBox.

## formato de archivo XBE
El archivo XBE se compone de un encabezado de imagen, una colección de encabezados de sección, un certificado, datos de almacenamiento local de subprocesos, una colección de versiones de biblioteca, un mapa de bits de Microsoft y las secciones que contienen el código y los recursos.

### Encabezado de imagen
El encabezado de la imagen comprende la información que explica dónde se encuentran los otros componentes del ejecutable dentro del archivo y cómo se debe tratar y cargar el ejecutable.

### Tabla TLS
La tabla TLS consta de toda la información que necesita el XBE para configurar correctamente el almacenamiento local de subprocesos. Básicamente, es exclusivo del directorio TLS que se encuentra en los archivos PE32 y se puede copiar directamente desde allí. Esta tabla se puede omitir si el archivo XBE no utiliza ningún almacenamiento local de subprocesos y el campo respectivo en el encabezado de la imagen se establece en cero.

| Compensación | Tamaño | Nombre | Descripción |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Inicio de datos sin procesar | Dirección absoluta (es decir, no un RVA) de inicio de los datos variables de TLS en la imagen del programa. |
| 0x0004 | 0x0004 | Fin de datos sin procesar | Dirección absoluta (es decir, no un RVA) del final de los datos variables de TLS en la imagen del programa. |
| 0x0008 | 0x0004 | Dirección del Índice | Dirección absoluta (es decir, no un RVA) de la variable de índice TLS. |
| 0x000C | 0x0004 | Dirección de devoluciones de llamadas | Dirección absoluta (es decir, no un RVA) de la tabla de funciones de devolución de llamada TLS terminada en nulo. |
| 0x0010 | 0x0004 | Tamaño de relleno cero | El número de bytes que siguen a los datos sin procesar que deben establecerse en cero en la memoria. |
| 0x0014 | 0x0004 | Características | Describe la alineación. |

### Certificado

Un certificado es obligatorio para cada ejecutable de Xbox que contenga información sobre los títulos:
 


- Hora y fecha en que se creó el certificado
- Identificación del título
- Nombre del título
- ID de títulos alternativos
- Tipos de medios permitidos desde los que se puede ejecutar el ejecutable (HD, DVD, CD, etc.)
- Región del juego
- Calificaciones de juegos
- Número de disco
- Versión
- Datos sin procesar de la clave LAN utilizados para System Link
- Datos sin procesar de la clave de firma (utilizados para firmar partidas guardadas)
- Claves de firma alternativas
- Tamaño original del certificado
- Nombre del servicio en línea (no presente en los primeros ejecutables)
- Indicadores de seguridad de tiempo de ejecución (no presentes en los primeros ejecutables)
 


### Tipos de medios permitidos
Tipos de medios que el ejecutable permite ejecutar. Se conocen los siguientes valores:
| Tipo de medio | Valor |
---------------------|------------|
| DISCO_DURO | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| discos compactos | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| LLAVE | 0x00000100 |
| TABLERO DE MEDIOS | 0x00000200 |
| DISCO_DURO_NO_SEGURO | 0x40000000 |
| MODO_NO_SEGURO | 0x80000000 |
| MÁSCARA_MEDIA | 0x00FFFFFF |

### Secciones
Las secciones se expresan mediante los encabezados de sección. Los encabezados de sección comienzan justo después del certificado y contienen información en qué lugar del archivo se encuentran las secciones reales. Al menos dos secciones siempre están presentes en un ejecutable de Xbox:


- .texto


- .rdata


## Referencias



* [Xbe - Ejecutable de XBox](https://xboxdevwiki.net/Xbe)



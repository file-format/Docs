{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo OBML: archivo de página web guardado de Opera Mini",
  "description" :"Obtenga más información sobre qué es un archivo OBML y las API que pueden crear y abrir un archivo OBML",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## ¿Qué es un archivo OBML?

Un archivo OBML (Opera Binary Markup Language) es una versión fuera de línea de una página web guardada por el navegador web móvil Opera Mini. Es una versión compacta e independiente de los archivos [HTML](/es/web/html/) que contiene todos los elementos de la página para mostrarlos en dispositivos específicos sin conexión. El formato de archivo OBML se ha actualizado a varias versiones y se utilizan OBML15 y OBML16 en general. Un punto importante a tener en cuenta es que cada versión de Opera Mini solo es compatible con un formato OBML. Por lo tanto, la actualización de Opera Mini dejará legibles las páginas previamente guardadas. Los archivos OBML se pueden convertir a HTML y [PDF](/es/pdf/).

## Formato de archivo OBML

El formato de archivo OBML se guarda en el formato de archivo propietario de Opera y sus especificaciones de formato de archivo no están disponibles públicamente. Sin embargo, [formato OMBL] (https://github.com/grawity/obml-parser/blob/master/obml.md) se realizó ingeniería inversa para decodificar su estructura de la siguiente manera.

### Tipos de datos OBML

Según los resultados de la ingeniería inversa, OBML utiliza los siguientes tipos primitivos:

* `byte` – entero sin signo (1 byte)
* `short` – entero con signo (2 bytes, big-endian)
* `medium` – entero con signo (3 bytes, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char`: un byte que contiene un carácter ASCII
* `string`: un blob que contiene texto codificado en UTF-8

### Encabezado OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## Referencias

* [formato OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)


{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file OBML - File di pagina Web salvato di Opera Mini",
  "description" :"Scopri cos'è un file OBML e le API che possono creare e aprire file OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Che cos'è un file OBML?

Un file OBML (Opera Binary Markup Language) è una versione offline di una pagina Web salvata dal browser Web mobile Opera Mini. È una versione compatta e autonoma dei file [HTML](/it/web/html/) che contiene tutti gli elementi della pagina per la visualizzazione su dispositivi specifici offline. Il formato di file OBML è stato aggiornato a diverse versioni con OBML15 e OBML16 utilizzati in generale. Un punto importante da tenere in considerazione è che ogni versione di Opera Mini è compatibile solo con un formato OBML. Pertanto, l'aggiornamento di Opera Mini lascerà leggibili le pagine salvate in precedenza. I file OBML possono essere convertiti in HTML e [PDF](/it/pdf/).

## Formato file OBML

Il formato file OBML viene salvato nel formato file proprietario di Opera e le sue specifiche del formato file non sono disponibili pubblicamente. Tuttavia, [formato OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) è stato decodificato per decodificare la sua struttura come segue.

### Tipi di dati OBML

Secondo i risultati del reverse engineering, OBML utilizza i seguenti tipi primitivi:

* `byte` – intero senza segno (1 byte)
* `short` – intero con segno (2 byte, big-endian)
* `medium` – intero con segno (3 byte, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – un byte contenente un carattere ASCII
* `string` – un blob contenente testo codificato UTF-8

### Intestazione OBML

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
## Riferimenti

* [formato OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)


{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML файлов формат – Opera Mini запазен файл на уеб страница",
  "description" :"Научете какво е OBML файл и API, които могат да създават и отварят OBML файл.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Какво е OBML файл?

OBML (Opera Binary Markup Language) файл е офлайн версия на уеб страница, запазена от мобилния уеб браузър Opera Mini. Това е самостоятелна, компактна версия на [HTML](/bg/web/html/) файловете, която съдържа всички елементи на страницата за показване на определени устройства, докато сте офлайн. Файловият формат OBML е надстроен до няколко версии, като OBML15 и OBML16 се използват като цяло. Важен момент, който трябва да имате предвид, е, че всяка версия на Opera Mini е съвместима само с един OBML формат. По този начин надграждането на Opera Mini ще остави запазените преди това страници четими. OBML файловете могат да бъдат конвертирани в HTML и [PDF](/bg/pdf/).

## OBML файлов формат

Файловият формат OBML се записва в собствения файлов формат на Opera и неговите спецификации за файловия формат не са публично достъпни. Въпреки това, [OMBL формат] (https://github.com/grawity/obml-parser/blob/master/obml.md) беше обратно проектиран, за да декодира структурата си, както следва.

### Типове данни OBML

Според резултатите от обратното инженерство, OBML използва следните примитивни типове:

* `байт` – цяло число без знак (1 байт)
* `short` – цяло число със знак (2 байта, big-endian)
* `среден` – цяло число със знак (3 байта, голям ред)
 * `blob` – { length: short, data: byte[length] }
* `char` – байт, съдържащ ASCII символ
* `string` – петно, съдържащо UTF-8 кодиран текст

### OBML заглавка

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
## Препратки

* [OMBL формат](https://github.com/grawity/obml-parser/blob/master/obml.md)


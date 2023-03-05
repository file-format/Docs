{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла OBML — файл сохраненной веб-страницы Opera Mini",
  "description" :"Узнайте, что такое файл OBML и API, которые могут создавать и открывать файл OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## .OBML вариант №

Файл OBML (Opera Binary Markup Language) — это автономная версия веб-страницы, сохраненная мобильным веб-браузером Opera Mini. Это автономная компактная версия файлов [HTML](/ru/web/html/), которая содержит все элементы страницы для отображения на определенных устройствах в автономном режиме. Формат файла OBML был обновлен до нескольких версий, при этом OBML15 и OBML16 используются в целом. Важно помнить, что каждая версия Opera Mini совместима только с одним форматом OBML. Таким образом, обновление Opera Mini оставит ранее сохраненные страницы доступными для чтения. Файлы OBML можно преобразовать в HTML и [PDF](/ru/pdf/).

## Формат файла OBML

Формат файла OBML сохраняется в проприетарном формате файла Opera, и его спецификации формата файла недоступны для общественности. Однако [формат OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) был реконструирован для декодирования его структуры следующим образом.

### Типы данных OBML

Согласно результатам обратного проектирования, OBML использует следующие примитивные типы:

* `байт` – беззнаковое целое (1 байт)
* `short` – целое число со знаком (2 байта, обратный порядок байтов)
* `medium` – целое число со знаком (3 байта, обратный порядок байтов)
 * `blob` – { length: short, data: byte[length] }
* `char` – байт, содержащий символ ASCII
* `string` – большой двоичный объект, содержащий текст в кодировке UTF-8.

### Заголовок OBML

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
## использованная литература

* [формат OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)


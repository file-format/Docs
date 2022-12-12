{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу OBML – збережений файл веб-сторінки Opera Mini",
  "description" :"Дізнайтеся, що таке файл OBML та API, які можуть створювати та відкривати файл OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Що таке файл OBML?

Файл OBML (мова бінарної розмітки Opera) — це офлайн-версія веб-сторінки, збережена мобільним веб-браузером Opera Mini. Це самодостатня, компактна версія файлів [HTML](/uk/web/html/), яка містить усі елементи сторінки для відображення на певних пристроях у режимі офлайн. Формат файлу OBML було оновлено до кількох версій із загалом використанням OBML15 та OBML16. Важливо пам’ятати, що кожна версія Opera Mini сумісна лише з одним форматом OBML. Таким чином, оновлення Opera Mini залишить раніше збережені сторінки читабельними. Файли OBML можна конвертувати в HTML і [PDF](/uk/pdf/).

## Формат файлу OBML

Формат файлу OBML зберігається у власному форматі файлу Opera, і його специфікації формату файлу недоступні для всіх. Однак [формат OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) було реверсно спроектовано для декодування його структури, як описано нижче.

### Типи даних OBML

Відповідно до результатів зворотного проектування, OBML використовує такі примітивні типи:

* `byte` – ціле число без знаку (1 байт)
* `short` – ціле число зі знаком (2 байти, старше)
* `medium` – ціле число зі знаком (3 байти, старше)
 * `blob` – { length: short, data: byte[length] }
* `char` – байт, що містить символ ASCII
* `рядок` – blob, що містить текст у кодуванні UTF-8

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
## Список літератури

* [Формат OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)


{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за FZP файловия формат и API, които могат да създават и отварят FZP файлове.",
  "title" :"FZP файлов формат – Fritzing XML файл с описание на част",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Какво е FZP файл?

FZP файлът е XML файл, създаден от [Fritzing](https://fritzing.org/) приложение за прототипиране и проектиране на електронни схеми. Той съдържа информация за свойствата, конекторите и шините на частта във файлов формат [XML](/bg/web/xml/). FPZ файловете не могат да се използват самостоятелно във Fritzing. Вместо това те се импортират като част от архивния файл на FZPZ.

## FZP файлов формат - повече информация

FZP файловете са XML файлове, които съдържат информация за свойствата, конекторите и шините на частта. В допълнение към тях FZP файловете също съдържат информация за заглавието, описанието, автора и датата на публикуване на FZP файла. Когато се експортира файл на част от Fritzing, приложението Fritzing създава компресиран [FZPZ](/bg/compression/fzpz/) архив, който съдържа FZP файл и четири [SVG](/bg/page-description-language/svg/) файла.

[Спецификациите на FZP файловия формат](https://github.com/fritzing/fzp/blob/master/docs/README.md) са достъпни в Github от Fritzing.

## Пример за файлова структура на FZP

Типичен FZP файл има следната XML структура.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Препратки

* [Спецификации на FZP файловия формат](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Нови части с разширение fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


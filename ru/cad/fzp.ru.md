{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла FZP и API-интерфейсах, которые могут создавать и открывать файлы FZP.",
  "title" :"Формат файла FZP - файл описания части Fritzing XML",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## .FZP вариант №

Файл FZP представляет собой XML-файл, созданный [Fritzing](https://fritzing.org/) приложением для прототипирования и проектирования электронных схем. Он содержит информацию о свойствах детали, соединителях и шинах в формате файла [XML](/ru/web/xml/). Файлы FPZ нельзя использовать отдельно во Fritzing. Вместо этого они импортируются как часть файла архива FZPZ.

## Формат файла FZP — дополнительная информация

Файлы FZP — это XML-файлы, содержащие информацию о свойствах детали, соединителях и шинах. В дополнение к этому файлы FZP также содержат информацию о названии, описании, авторе и дате публикации файла FZP. Когда файл детали Fritzing экспортируется, приложение Fritzing создает сжатый архив [FZPZ](/ru/compression/fzpz/), который содержит файл FZP и четыре файла [SVG](/ru/page-description-language/svg/).

[Спецификации формата файла FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) доступны на Github от Fritzing.

## Пример структуры файла FZP

Типичный файл FZP имеет следующую структуру XML.

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
## использованная литература

* [Спецификации формата файла FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Новые детали с расширением fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


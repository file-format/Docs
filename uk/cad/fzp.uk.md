{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу FZP та API, які можуть створювати та відкривати файли FZP.",
  "title" :"Формат файлу FZP - файл опису частини XML Fritzing",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Що таке файл FZP?

Файл FZP – це XML-файл, створений програмою [Fritzing](https://fritzing.org/) для створення прототипів і проектування електронних схем. Він містить інформацію про властивості частини, з’єднувачі та шини у форматі файлу [XML](/uk/web/xml/). Файли FPZ не можна використовувати окремо у Fritzing. Натомість вони імпортуються як частина архівного файлу FZPZ.

## Формат файлу FZP – додаткова інформація

Файли FZP — це XML-файли, які містять інформацію про властивості частини, роз’єми та шини. Окрім цього, файли FZP також містять інформацію про назву, опис, автора та дату публікації файлу FZP. Коли експортується файл частини Fritzing, програма Fritzing створює стислий архів [FZPZ](/uk/compression/fzpz/), який містить файл FZP і чотири файли [SVG](/uk/page-description-language/svg/).

[Специфікації формату файлу FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) доступні на Github від Fritzing.

## Приклад структури файлу FZP

Типовий файл FZP має таку структуру XML.

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
## Список літератури

* [Специфікації формату файлу FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Нові частини з розширенням fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу SY_ - стиснутий файл SYS",
  "description":"Дізнайтеся про формат файлу SY_ та API, які можуть створювати та відкривати файли SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Що таке файл SY_?

Файл SY_ — це стислий файл .sys, який використовується інсталяторами програмного забезпечення для зменшення розміру інсталяційних файлів, упакованих у інсталятор. Це зменшує загальний розмір інсталятора. Файли SY_ можна розширити за допомогою утиліти командного рядка Microsoft Expand, яка розгортає один або кілька стиснутих файлів.

## Формат файлу SY_ - Додаткова інформація

Файли SY_ зберігаються на диску як стислі двійкові файли. Однак їхній внутрішній формат файлу не є загальнодоступним. Утиліта командного рядка Microsoft Expand може розгортати файли SY_ за допомогою одного з наведених нижче командних рядків.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Після розгортання файли SY_ перетворюються на файл [SYS](https://docs.fileformat.com/system/sys/).

Файли SY_ схожі на файли EX_ і DL_.

## Список літератури

* [StuffIt - Вікіпедія](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)


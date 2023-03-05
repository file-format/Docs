{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла SY_ — сжатый файл SYS",
  "description":"Узнайте о формате файла SY_ и API, которые могут создавать и открывать файлы SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## .SY_ вариант №

Файл SY_ — это сжатый файл .sys, который используется установщиками программного обеспечения для уменьшения размера установочных файлов, упакованных внутри установщика. Это уменьшает общий размер установщика. Файлы SY_ можно расширить с помощью утилиты командной строки Microsoft Expand, которая расширяет один или несколько сжатых файлов.

## Формат файла SY_ — дополнительная информация

Файлы SY_ сохраняются на диск как сжатые двоичные файлы. Однако их внутренний формат файла недоступен публично. Утилита командной строки Microsoft Expand может расширять файлы SY_ с помощью одной из следующих командных строк.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
При расширении файлы SY_ преобразуются в файл [SYS](https://docs.fileformat.com/system/sys/).

Файлы SY_ аналогичны файлам EX_ и DL_.

## использованная литература

* [StuffIt — Википедия](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)


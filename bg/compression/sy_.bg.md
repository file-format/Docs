{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ файлов формат - компресиран SYS файл",
  "description":"Научете за SY_ файловия формат и API, които могат да създават и отварят SY_ файлове.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Какво е SY_ файл?

SY_ файлът е компресиран .sys файл, който се използва от софтуерните инсталатори за намаляване на размера на инсталационните файлове, пакетирани в инсталатора. Това намалява общия размер на инсталатора. SY_ файловете могат да бъдат разширени с помощта на помощната програма за команден ред на Microsoft Expand, която разширява един или повече компресирани файлове.

## SY_ файлов формат - повече информация

SY_ файловете се записват на диск като компресирани двоични файлове. Техният вътрешен файлов формат обаче не е публично достъпен. Помощната програма за команден ред на Microsoft Expand може да разшири SY_ файлове с помощта на един от следните командни редове.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Когато се разгънат, SY_ файловете се преобразуват в [SYS](/system/sys/) файл.

SY_ файловете са подобни на EX_ и DL_ файловете.

## Препратки

* [StuffIt - от Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)


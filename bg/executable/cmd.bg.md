{
  "date" : "2021-07-12",
  "keywords" :[ "cmd файл", "какво е cmd файл", "файл", "cmd пример", "cmd файл разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за CMD файловия формат и API, които могат да създават и отварят CMD файлове.",
  "title" :"CMD – Windows команден файлов формат",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Какво е CMD файл?
CMD файлът се състои от скрипт, съдържащ една или няколко команди под формата на обикновен текст, които се изпълняват, за да се изпълнят различни задачи. Той е подобен на [BAT](/bg/executable/bat/) файл, който обикновено се използва и за съхраняване на пакет от изпълними команди. CMD файловете се използват широко в операционната система Microsoft Windows. Тези файлове бяха въведени почти през 90-те години, но все още се използват в най-новата операционна система Windows. Тези файлове обикновено се записват за изпълнение на повече от една команда в последователност.

## CMD файлов формат
CMD е файлов формат, използван от изпълними програми в стил CP/M. Като цяло е сравним с [COM](/bg/executable/com/) в CP/M-80 и [EXE](/bg/executable/exe/) в DOS. CMD файлът съдържа от 1 до 8 групи код или данни и 128-байтово заглавие. Всяка група може да бъде с размер до 1 mb. CMD файловете могат също да съдържат информация за преместване и Resident System Extensions (RSX) в по-късните си версии. CMD е новодошъл в сравнение с [BAT](/bg/executable/bat/) файл; използван за MS-DOS преди пускането на windows В MS-DOS. Въпреки че днес все още можете да запазвате файлове с разширение .bat, много хора използват разширението .cmd, за да запазят своите изпълними скриптове.

### Спецификация на CMD формат

Началото на заглавката съдържа списъка на групите, присъстващи във файла, заедно с техните типове. Всеки тип може да се използва най-много веднъж. Тези видове са:

- Код
- Данни
- Екстра
- Купчина
- Потребител 1
- Потребител 2
- Потребител 3
- Потребител 4
- Споделен код

Подобно на префикса на програмния сегмент в DOS, първите 256 байта от групата данни са нула. Те ще бъдат попълнени от CP/M-86 с нулевата страница. Ако няма група данни, вместо това ще се използват първите 256 байта от кодовата група.
## Пример за CMD файл
Следва пример на CMD скрипт за показване на системна информация.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Препратки

* [Как да напишем CMD скрипт](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD файл (CP/M) - от Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))


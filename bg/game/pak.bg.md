{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "файлов формат", "какво е pak файл", "файл", "пак пример", "файл с пакет за видео игра", "разширение"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за .pak файла и API, които могат да създават и отварят PAK файлове.",
  "title" :"Файлов формат PAK – пакетен файл за видеоигри",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Какво е PAK файл?

PAK файлът е пакетен файл, създаден от различни видеоигри за архивиране на данни от играта. По същество това е файлов формат за игра. Това може да включва множество елементи на играта като графики, текстури, звуци, обекти, заедно с други данни за играта. Архивът се запазва предимно като .zip файл и може да бъде извлечен с популярен софтуер за декомпресия като WinZip и WinRAR. Примери за видеоигри, използващи PAK файлове, включват Quake, Hexen, Crysis и Half-Life.

## PAK файлов формат - повече информация

В повечето случаи PAK файловете се записват в [ZIP файлов формат](/bg/compression/zip/). Но различните приложения могат да използват различен файлов формат за съхраняване на тези файлове.


## Как да отворите PAK файлове?

Можете да отваряте PAK файлове с приложения като [PakExplorer](https://www.quaketerminus.com/tools.shtml) и [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- ----------------------**

## Файлов формат PAK - обектен файл Simutrans

Файл с разширение .pak е файлов формат за игра за симулация на транспорт [Simutrans](https://www.simutrans.com/en/). Той съдържа обекти, използвани в симулацията, като създадени от потребителя графики и съдържание на данни. Той може да има няколко различни обекта, като игрални превозни средства, сгради, терен и др. PAK файловете се генерират с помощта на MakeObject, помощна програма, която компилира .dat файлове и .png картини за създаване на тези симулационни обекти. Simutrans позволява на играчите да управляват успешна транспортна система чрез изграждане и управление на транспортни системи за пътници, поща и стоки по суша

## Как да създадете PAK файлове?

Simutrans е изброил примерни примери за създаване на PAK файлове на Windows и Linux OS.

### Windows OS

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Препратки

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)


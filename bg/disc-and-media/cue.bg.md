{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "file", "разширение", "format", "какво е cue файл", "музика", "cue файлов формат", "cue файлов формат спецификация", "cue лист", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за CUE файловия формат и API, които могат да създават, конвертират и отварят CUE файлове.",
  "title" :"CUE - файл с Cue Sheet",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Какво е CUE файл?

Файл с разширение .cue, известен също като файл с реплики, е файл с метаданни, който съдържа информация за оформлението на песните на CD или DVD. Те се поддържат от медийни плейъри и приложения за създаване на оптични дискове. Основните аудио данни, съхранени на компактдиска, се посочват от cue файла, заедно със спецификациите на дължини на песни, заглавия на дискове и изпълнители. По този начин, ако един аудио файл съдържа множество песни, cue файлът може да се използва за разделяне на аудиото на множество файлове или за препратка към различни песни.

## CUE файлов формат

Файловете CUE или cue sheet се съхраняват в обикновен текстов формат, който е четим от хора. Информацията в cue файл са команди с един или повече параметри. Тези команди се отнасят или за целия файл, или за отделна песен, в зависимост от конкретната команда и контекста. Ръководството за потребителя на CDRWIN описва спецификациите за синтаксиса и семантиката на листа с реплики.

## CUE Sheet Основни команди

|Команда|Описание|
---|---|
|ФАЙЛ| Отнася се за файла, съдържащ данните и неговия формат като [MP3](/bg/audio/mp3/), [WAV](/bg/audio/wav/) или обикновен двоичен образ на диск)|
|ПЛЕТА| Дефинира информация за контекста на песента, като нейния номер и тип или режим.|
|ИНДЕКС| Представя позицията като индекс във ФАЙЛА. Форматът е mm:ss:ff (минута-секунда-кадър).|
|PREGAP и POSTGAP|Това показва pregap или post-gap на песен, която не се съхранява в никакъв файл с данни. Дължината е посочена в същия формат минута-секунда-кадър като за INDEX.|

### Пример за CUE лист

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Препратки

* [.cda файл - от Wikipedia](https://en.wikipedia.org/wiki/.cda_file)


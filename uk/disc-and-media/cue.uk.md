{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "файл", "розширення", "формат", "що таке cue-файл", "музика", "cue-файл", "специфікація формату cue-файлу", "cue sheet", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу CUE та API, які можуть створювати, конвертувати та відкривати файли CUE.",
  "title" :"CUE - файл аркуша підказок",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Що таке файл CUE?

Файл із розширенням .cue, також відомий як файл підказок, — це файл метаданих, який містить інформацію про розташування доріжок на CD або DVD. Вони підтримуються медіаплеєрами та програмами для створення оптичних дисків. Основні аудіодані, що зберігаються на компакт-диску, посилаються на файл cue разом із специфікаціями тривалості треків, назв дисків і виконавців. Таким чином, якщо один аудіофайл містить кілька доріжок, файл підказки можна використовувати для розділення аудіофайлів на кілька файлів або посилання на різні доріжки.

## Формат файлу CUE

Файли CUE або аркуша підказок зберігаються у форматі звичайного тексту, який легко читається людиною. Інформація у файлі підказок — це команди з одним або кількома параметрами. Ці команди застосовуються до всього файлу або до окремої доріжки, залежно від конкретної команди та контексту. Посібник користувача CDRWIN описує специфікації синтаксису та семантики аркуша підказок.

## Основні команди таблиці CUE

|Команда|Опис|
---|---|
|ФАЙЛ| Посилається на файл, що містить дані, і його формат, як-от [MP3](/uk/audio/mp3/), [WAV](/uk/audio/wav/) або простий бінарний образ диска)|
|ТРЕК| Визначає контекстну інформацію треку, наприклад його номер, тип або режим.|
|ІНДЕКС| Представляє позицію як індекс у ФАЙЛІ. Формат: mm:ss:ff (хвилина-секунда-кадр).|
|PREGAP і POSTGAP|Це вказує на попередній або построзрив треку, який не зберігається в жодному файлі даних. Довжина вказується у тому самому форматі хвилина-секунда кадру, що й для INDEX.|

### Приклад аркуша CUE

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
## Список літератури

* [.cda файл – Вікіпедія](https://en.wikipedia.org/wiki/.cda_file)


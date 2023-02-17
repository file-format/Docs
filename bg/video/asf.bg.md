{
  "date" : "2021-02-15",
  "keywords" :[ "asf файл", "asf файлов формат", "какво е asf файл", "файл", "asf пример", "asf файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF – Файлов формат за разширени системи",
  "description":"Научете за файловия формат ASF и API, които могат да създават и отварят ASF файлове.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Какво е ASF файл?

Файл с разширение .asf е мултимедиен файлов формат за съхраняване и възпроизвеждане на цифрови медийни потоци по мрежата. Това е контейнерен файлов формат, който може да има както видео, така и аудио съдържание за стрийминг онлайн. Рядко ще намерите ASF файлове и по-вероятно ще попаднете на Windows Media Audio ([WMA](/bg/audio/wma/)) и Windows Media Video ([WMV](/bg/video/wmv/)) файлове, които и двата указват ASF файлове със съдържание, кодирано със съответните кодеци. Медийните файлове на Windows могат да се създават и четат с помощта на SDK на Windows Media Format.

## ASF файлов формат

Един ASF файл може да съдържа множество независими или зависими потоци. Това може да включва множество аудио потоци за многоканално аудио или множество видео потоци с битрейт. Множеството битрейтове правят потоците подходящи за предаване през различни ленти. Освен това потоците в ASF файл могат да бъдат в компресиран или некомпресиран формат. Най-добрата компресия се постига с кодеците Microsoft Windows Media Audio and Video 9 Series. Пълните спецификации на файловия формат ASF са налични на [уебсайта на Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### ASF файлова структура от най-високо ниво

ASF файловете логично съдържат три типа обекти от най-високо ниво:

* `Header Object` - задължителен и трябва да се постави в началото на всеки ASF файл
* `Data Object` - задължително и трябва да следва заглавния обект
* `Индексен(ни) обект(и)` - незадължителен, но полезен при осигуряване на базиран на времето произволен достъп до ASF файлове

Следното изображение показва файловата структура от най-високо ниво на ASF файлове.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF Обект на заглавката от най-високо ниво

Обектът Header предоставя добре позната последователност от байтове в началото на ASF файловете и по избор може да съдържа метаданни, като например библиографска информация. Той съдържа цялата информация, необходима за правилното интерпретиране на информацията в обекта на данни. Заглавният обект може да включва няколко стандартни обекта, включително, но не само:

* File Properties Object - Съдържа глобални файлови атрибути.
* Stream Properties Object - Дефинира цифров медиен поток и неговите характеристики.
* Header Extension Object - Позволява добавянето на допълнителна функционалност към ASF файл, като същевременно поддържа обратна съвместимост.
* Обект на описание на съдържанието - Съдържа библиографска информация.
* Script Command Object - Съдържа команди, които могат да бъдат изпълнени на времевата линия за възпроизвеждане.
* Маркерен обект - Предоставя именувани точки за прескачане във файл.

Обектът Header е представен чрез следната структура:

|Име на поле |Тип поле |Размер (битове)|
---|---|---|
|ID на обект| GUID| 128|
|Размер на обекта| QWORD| 64|
|Брой заглавни обекти| DWORD| 32|
|Запазено1| БАЙТ| 8|
|Запазено2| БАЙТ| 8|

#### ASF Обект на данни от най-високо ниво

Всички цифрови медийни данни за ASF файл се съдържат в обекта с данни и се съхраняват под формата на ASF пакети с данни. Всеки пакет данни е с фиксирана дължина и съдържа данни за един или повече цифрови медийни потоци.

#### ASF индексни обекти от най-високо ниво

ASF индексните обекти от най-високо ниво имат следните два типа:

* `Simple Index Object` - Съдържа базиран на времето индекс на видео данните в ASF файл. Интервалът от време между записите в индекса е постоянен и се съхранява в Simple Index Object.
* `Индексен обект` - Отнася се за индексния обект, индексния обект на медийния обект и индексния обект на времеви код, чиито формати са подобни. Подобно на Simple Index Object, Index Object индексира по време с фиксиран интервал от време, но не се ограничава до видео потоци.

## Препратки

* [ASF файлов формат - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Файлов формат QuickTime – Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

{
  "date" : "2021-01-21",
  "keywords" :[ "ai файл", "ai файлов формат", "какво е ai файл", "файл", "ai пример", "ai файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI – Файл с произведения на Adobe Illustrator",
  "description":"Научете за AI файлов формат и API, които могат да създават и отварят AI файлове.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Какво е AI файл?

Файл с разширение .ai е файл с произведения на Adobe Illustrator, който съдържа векторни графики в една страница. той използва точки, за да създаде пътища за показване на данните за изображението, като по този начин го предпазва от загуба на качество на изображението, ако бъде увеличено. AI файловият формат е основата на PGF файловия формат, който е подобен на AI файловете. AI форматът намира основното си приложение за лога и печатни медии и първоначалните му версии се смятаха за подобни на тези на [EPS](/bg/image/eps/) файловете. AI файловете могат да се отварят с инструменти на Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro и CorelDraw Graphics.

## AI файлов формат

AI е собствен файлов формат на Adobe Illustrator и използва подход с двоен път, подобен на PGF, за запазване на EPS-съвместими файлове. [Спецификациите на файловия формат на Adobe Illustrator] (https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) предоставят подробна справка на програмиста за вътрешни подробности за този файлов формат. Всички документи (файлове), създадени от Adobe Illustrator, са документи на езика PostScript и имат две основни части, съответстващи на конвенциите за структуриране на документи: „пролог“ и „скрипт“.

### Пролог

Секцията пролог капсулира информацията, необходима за тълкуване на файла. Пример може да бъде ограничителната кутия, която съдържа всички знаци на страницата. Той също така съдържа информация за ресурси като шрифтове и дефиниции на процедури. Тези ресурси са логически групирани в набори, наречени procsets, и съдържат изрични методи за инициализиране и прекратяване на техните процедури.

### Скрипт

Графичните елементи на страницата се описват от скрипта. Скриптът съдържа препратки към операторите и процедурите в пролога, заедно с операнди и данни. Трите логически раздела на скрипта включват:

* Последователност за настройка - която инициализира и активира ресурсите, дефинирани в пролога
* Последователност от описателни оператори
* Трейлър, който деактивира ресурсите

Операторите в скрипта са последователности от графични елементи, написани на езика, дефиниран от procsets в пролога. Тези последователности се състоят от колекции от елементи на данни, дефиниции на графични атрибути и извиквания на процедурите, дефинирани в процесите.

### Обектни етикети

Обектните етикети се използват за прикачване на персонализирана информация към арт обект на Adobe Illustrator. Етикетите се състоят от:

* Идентификатор на етикет
* Тип етикет
* Данни

## Препратки
* [Спецификации на файловия формат на Adobe Illustrator] (https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [AI файлов формат от PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

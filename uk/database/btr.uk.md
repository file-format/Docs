{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "розширення", "файл", "формат файлу", "Тип файлу бази даних", "Формат файлу бази даних", "База даних Btrieve" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу BTR та API, які можуть створювати та відкривати файли BTR.",
  "title" :"BTR - файл бази даних Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Що таке файл BTR?

Файл із розширенням .btr – це файл бази даних, створений програмою транзакційної бази даних [Btrieve](https://www.actian.com/). На відміну від систем керування реляційними базами даних (RBMS), Btrieve базується на методі індексованого послідовного доступу (ISAM), який є способом зберігання даних для швидкого пошуку. Файл BTR зберігає колекцію записів і використовується для створення звітів відповідно до вимог. Файли BTR можна відкрити за допомогою Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility та Legend Software BTRIEVE Viewer.

## Структура файлу BTR – більше інформації

Внутрішня структура даних і вирівнювання кожного байта в структурі файлу BTR не є загальнодоступними. Однак Btrieve
надає [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm), який можна використовувати для читання інформації з файлів BTR. Він сумісний із такими мовами програмування та середовищами розробки.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Отримання даних із файлу BTR залежить від пов’язаного з ним файлу DDF. Без DDF отримати інформацію з такого файлу буде нелегко.

## Список літератури

* [Btrieve - Вікіпедія](https://en.wikipedia.org/wiki/Btrieve)
* [Вступ до API Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)


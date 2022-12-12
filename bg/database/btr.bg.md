{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "разширение", "файл", "файлов формат", "Тип файл на база данни", "Файлов формат на база данни", "Btrieve база данни" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за BTR файловия формат и API, които могат да създават и отварят BTR файлове.",
  "title" :"BTR – Btrieve файл с база данни",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Какво е BTR файл?

Файл с разширение .btr е файл с база данни, създаден от [Btrieve](https://www.actian.com/) приложение за транзакционна база данни. За разлика от системите за управление на релационни бази данни (RBMS), Btrieve се основава на метода за индексиран последователен достъп (ISAM), който е начин за съхраняване на данни за бързо извличане. BTR файлът съхранява колекция от записи и се използва за генериране на отчети според изискванията. BTR файловете могат да се отварят с помощта на Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility и Legend Software BTRIEVE Viewer.

## BTR файлова структура - повече информация

Вътрешната структура на данните и подравняването на всеки байт в структурата на BTR файл не е публично достъпна. Въпреки това, Btrieve
предоставя [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm), който може да се използва за четене на информация от BTR файлове. Той е съвместим със следните езици за програмиране и среди за разработка.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Извличането на данни от BTR файл зависи от свързания с него DDF файл. Без DDF няма да е лесно да извлечете информацията от такъв файл.

## Препратки

* [Btrieve – Уикипедия](https://en.wikipedia.org/wiki/Btrieve)
* [Въведение в API на Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)


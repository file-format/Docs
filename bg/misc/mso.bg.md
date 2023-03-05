{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO – референтен файл с макроси на Microsoft Office",
  "description":"Научете за MSO файла и API, които могат да създават и отварят MSO файлове.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Какво е MSO файл?

MSO файлът е файлов формат на контейнер за данни, който се създава, когато HTML съобщение се изпраща с помощта на Microsoft Outlook. Това се случва най-вече с приложенията на Microsoft Office 2000. В повечето случаи имейл съобщението е прикачено с име **Oledata.mso** файл. Получателят на имейл, когато отвори такъв имейл, може да прегледа файла правилно, дори и да няма инсталиран същия софтуер. MSO файловете се отнасят до [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Microsoft MSO файлов формат

MSO файловете се записват във формат на Microsoft Compound Document File Format (MCDF), който е известен също като Object Linking and Embedding (OLE) или Component Object Model (COM) структуриран складов съставен файл за реализация на двоичен файлов формат.

### Структура на файловия формат на MSO

Вътрешната структура на файловия формат на файловия формат MSO е добре дефинирана в [Структури](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) раздел от документацията на MCDF. Таблицата за разпределение на файлове (FAT) управлява разпределението на секторите и веригите на секторите. Той съдържа масив от 32-битови номера на сектори. Всеки индекс в масива представлява номер на сектор, докато неговата стойност представлява следващия сектор във веригата или специална стойност.

## Препратки

* [COM Structured Storage](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)


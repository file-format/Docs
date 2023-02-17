{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "разширение", "файл", "файлов формат", "Тип файл на база данни", "Файлов формат на база данни", "Файлове на база данни"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за файловия формат ACCDB и API, които могат да създават и отварят ACCDB файлове.",
  "title" :"Файлов формат ACCDB – файл с база данни на Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Какво е ACCDB файл?

Файл с разширение .accdb е файл с база данни на Microsoft Access 2007, който съхранява потребителски данни в таблици. Поддържа съхранение
персонализирани формуляри, SQL заявки и други данни. ACCDB файловете замениха [MDB](/bg/база данни/mdb/) файлове, след като Microsoft премина към файлова структура, базирана на XML. ACCDB файловете все още могат да бъдат конвертирани в MDB със стара съвместимост. Въпреки това, ACCDB е широко използваният файлов формат на базата данни на Access сега. Microsoft също поддържа допълнителни функции във формат ACCDB, като например възможност за съхраняване на прикачени файлове, двоични данни и поддръжка на поле с много стойности.

## ACCDB файлов формат

Подобно на MDB, няма налични публични спецификации за ACCDB файлов формат. Microsoft поддържа програмен достъп до тези файлове чрез стандарт Open Database Connectivity (ODBC) и Visual Basic for Applications (VBA).

### Прозрение

Шестнадесетичен дъмп на прост ACCDB файл предполага, че има общи прилики в структурата с най-новите версии на предшественика MDB Format Family. И двата файлови формата използват фиксирани размери на страницата от 4096 байта. Друго сходство между ACCDB и MDB е формата на магическото число, което включва низа „Стандартен ACE DB“ за ACCDB. Версия или код за съвместимост е на едно и също място и в двата формата. Инструментите mdbtools | HACKING файлът гласи „Offset 0x14 съдържа Jet версията на тази база данни“ и неофициалното ръководство на MDB се съгласява. Информацията в тези източници, комбинирана със запис в Wikipedia за [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), предполага, че стойност 0x02 показва ACE 12 (Access 2007), а 0x03 показва ACE 14 (Access 2010). Обаче минимална база данни, създадена в Access 2010, и подобна, създадена в Access 2016, имат 0x02 на това място. Минимална база данни, създадена в Access 2016, но дефинираща колона с нововъведения тип данни „голямо цяло число“, имаше стойност 0x05. В ACCDB файлове този индикатор изглежда отразява съвместимостта на файла, а не версията на ACE машината, използвана за създаването му.

## Препратки

* [Файлов формат за достъп](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Спецификации на Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Кой файлов формат на Access трябва да използвам?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=en-us&rs=en-us&ad=us)

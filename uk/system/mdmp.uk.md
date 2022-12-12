{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл MDMP – формат файлу мінідамп Windows",
  "description":"Дізнайтеся про формат файлу MDMP та API, які можуть створювати та відкривати файли MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Що таке файл MDMP?

Файл MDMP — це дамп пам’яті програми в Microsoft Windows, який створюється, коли програма закривається ненормально або виходить з ладу. Він містить інформацію та дампи даних, які можна використовувати для усунення причини збою. Файли MDMP застосовуються до додатків, створених будь-якою платформою, наприклад Java, C++, .NET та іншими. На додаток до MDMP,

Програми, які можуть відкривати файли MDMP, включають Microsoft Visual Studio Debugger.

## Формат файлу MDMP

Файли MDMP зберігаються як двійкові файли на диск і можуть бути відкриті за допомогою налагоджувача Microsoft Visual Studio. Він містить наступну інформацію, яка допоможе визначити причину збою.

* Деталі повідомлення Stop, його параметри та інші дані
* Список завантажених драйверів
* Контекст процесора (PRCB) для процесора, який перестав працювати
* Інформація про процес і контекст ядра (EPROCESS) для процесу, який зупинився
* Інформація про процес і контекст ядра (ETHREAD) для потоку, який зупинився
* Стек викликів режиму ядра для потоку, який зупинився

Ця інформація допомагає з’ясувати, що сталося, усунути проблему та запобігти її повторенню.

### Проаналізуйте мінідамп

Для створення файлу дампа пам’яті Windows потрібен файл підкачки на завантажувальному томі. Файл підкачки створюється на завантажувальному томі та має мати розмір принаймні 2 мегабайти (МБ). Файл дампа створюється під час збою програми. У разі другої проблеми створюється другий невеликий файл дампа пам’яті, а попередній зберігається. Ім’я файлу дампа є чітким, щоб уникнути перезапису.

Windows зберігає список усіх файлів дампа пам’яті в папці %SystemRoot%\Minidump. Ви можете проаналізувати файли MDMP, запустивши їх у Visual Studio Debugger, як описано нижче.

## Як відкрити файл MDMP у Visual Studio?

Щоб відкрити файл MDMP у Visual Studio, можна використати наступні дії.

* У Visual Studio в меню «Файл» виберіть «Відкрити |». Збійний дамп.
* Перейдіть до файлу дампа, який ви хочете відкрити.
* Виберіть Відкрити.

## довідка

* [Як прочитати файл невеликого дампа пам’яті, створений Windows, якщо стався збій](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -файл)

{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "розширення", "файл", "формат файлу", "Тип файлу бази даних", "Формат файлу бази даних", "Файли бази даних" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу ACCDT та API, які можуть створювати та відкривати файли ACCDT.",
  "title" :"ACCDT - формат файлу шаблону бази даних Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Що таке файл ACCDT?

Файл із розширенням .accdt — це файл шаблону бази даних Microsoft Access, який містить попередньо визначені елементи бази даних. Ці елементи являють собою набір структур, які визначають програми бази даних, такі як схеми бази даних для зберігання даних, опис макета для представлень даних і метадані, що описують базу даних. Будучи файлами шаблонів, файли ACCDT можна використовувати для створення баз даних на основі налаштувань шаблонів, доступних у них. Отримані файли бази даних зберігаються як файли [ACCDB](/uk/database/accdb/) і заповнюються даними в таблицях. Microsoft Access 2007 і новіші версії можуть відкривати файли ACCDT.

## Формат файлу ACCDT

Файли шаблонів ACCDT базуються на специфікаціях Office Open XML, і всі дані містяться в пакеті ZIP. Інформація про структуру та вміст бази даних міститься у файлах [XML](/uk/web/xml/) і текстових файлах і пов’язана один з одним через зв’язки. Ви можете змінити назву файлу ACCDT на розширення [.zip](/uk/compression/zip/) і використати будь-яке програмне забезпечення для стиснення, щоб розпакувати вміст ZIP-архіву.

### Структура файлу

Файли ACCDT — це пакети, які містять набір пов’язаних частин. Кожна **частина** зберігає інформацію про вміст програми бази даних за допомогою XML, текстового та двійкового форматів, яка включає:

* Об'єкти бази даних
* Пов’язані метадані
* Структура упаковки

#### Пакет

Пакет — це [ZIP](/uk/compression/zip/) архів, який містить кілька частин і відповідає Конвенціям про відкрите пакування, визначеним у [ISO/IEC-29500-2](https://go.microsoft.com/fwlink/ ?LinkId=150883). Файли ACCDT мають містити принаймні одну частину метаданих шаблону, яка має бути метою зв’язку. Ці метадані шаблону є початковою частиною файлу ACCDT.

#### Частина

Частина — це потік байтів, який має пов’язаний тип для визначення характеру та типу вмісту, що зберігається в ньому. Перелік частин визначає дійсні частини, дійсні типи вмісту та необхідні зв’язки між усіма частинами в пакеті.

#### Стосунки

`Зв'язок між пакетами' - де target є частиною, а джерело - пакетом у цілому.

`Зв'язок між частинами' - де мета є частиною, а джерело - частиною в пакеті.

`Явний зв’язок’ – де на ресурс посилається вміст вихідної частини шляхом посилання на елемент зв’язку за значенням його атрибута ID.

`Implicit Relationship` - зв'язок, який не є явним.

`Внутрішній зв'язок` - де мета є частиною пакета.

`Зовнішній зв'язок` - де цільовим є зовнішній ресурс, якого немає в пакеті.

## Посилання ##

* [Формат файлу шаблону доступу](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

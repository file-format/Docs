{
  "date" : "2021-05-25",
  "keywords" :[ "DML", "файл DML", "формат файлу DML", "тип файлу DML", "файл", "тип", "що таке файл DML" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - HTML-файл DynaScript",
  "description":"Дізнайтеся про формат файлу DML та API, які можуть створювати та відкривати файли DML.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Що таке файл DML?

Файл із розширенням .dml — це файл коду сторінки веб-скрипту, створений за допомогою DyanScript. DynaScript — це динамічна [HTML](/uk/web/html/) мова сценаріїв, яка сумісна з ECMAScript і надає більшість тих самих функцій, що й інші мови сценаріїв. Він схожий на код ColdFusion і код Microsoft Active Server Pages (ASP). Файли DML можна відкривати та переглядати в стандартних веб-переглядачах, подібних до інших сторінок HTML.

## Формат файлу DML

Файли DML створюються у форматі звичайного текстового файлу, і їх можна відкрити за допомогою текстового редактора для перегляду коду. Написання коду за допомогою мови сценаріїв DML можна використовувати для динамічного створення HTML на сторінках DML, розміщених на сервері. DynaScript побудовано з таких елементів мови:


* Тег SCRIPT – вони вбудовані в документи як коментарі HTML. HTML-коментар позначається \ <!-- tag.
* Літерали – це фіксовані значення у файлах DynaScript. Прикладами таких є цілі числа, такі як s 123, 0x3F, 0123, числа з плаваючою комою, такі як 456.789, 3.2e-8, логічні значення, такі як true або false, і рядки, такі як "Дощ в Іспанії"
* Змінні - змінні DynaScript не потрібно визначати або призначати їм фіксований тип даних. Змінна повинна мати значення, перш ніж використовувати її у виразі; інакше генерується попередження під час виконання.
* Вирази – це комбінації змінних, літеральних значень, операторів та інших виразів. Права частина оператора присвоєння є виразом.
* Оператори - вони працюють з одним або кількома виразами, які називаються операндами. Вони можуть бути потрійними, двійковими або унарними: потрійні оператори діють на три вирази, двійкові – на два вирази, а унарні – на одне.
* Інструкції - вони керують потоком сценаріїв, маніпулюють об'єктами та загальним програмуванням. Загалом ці оператори відповідають стандартному синтаксису C і Java. Прикладами є цикли if-else, do-while, switch, break, continue тощо, як і будь-яка інша мова сценаріїв.
* Функції. Функції, як і будь-яка інша мова сценаріїв, дозволяють інкапсулювати набір інструкцій один раз у документ як функцію, а потім використовувати його кілька разів у документі (викликаючи функцію). DynaScript також підтримує функції.
* Об’єкти – DynaScript об’єктно-орієнтований і підтримує «об’єкти» та основні об’єктно-орієнтовані концепції інкапсуляції, поліморфізму та успадкування.

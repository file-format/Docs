{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - мовний файл визначення звіту",
  "keywords" :[ "rdl", "мова визначення звіту", "XmlTextWriter", "XSD", "елемент RDL"],
  "description":"Дізнайтеся про формат файлу RDL, який є XML-представленням визначення звіту SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Що таке файл RDL? ##

RDL (Report Definition Language) — це стандарт, встановлений Microsoft для визначення звітів. Файл RDL складається з одного або кількох елементів RDL. Тоді як RDL-елемент складається з його типу даних і потужності. Елемент може бути простим і складним. Простий елемент не має дочірніх елементів або атрибутів, тоді як складний елемент має дочірні та додаткові атрибути.

## Визначення схеми RDL XML
Файл визначення схеми XML (XSD) перевіряє файл RDL. Схема визначає правила розміщення елементів RDL у файлі .rdl. Елемент RDL може бути простим і складним. Простий елемент не має дочірніх елементів або атрибутів, а складний елемент має дочірні елементи та необов’язкові атрибути.

## Створення RDL
Оскільки RDL є відкритим і розширюваним за своєю природою, можна створити багато програм і інструментів, які створюють файли RDL на основі його XML-схеми. Одним із найпростіших способів створення RDL із програми є використання класів Microsoft .NET Framework простору імен **System.Xml** і простору імен System.Linq. Зокрема, клас **XmlTextWriter** можна використовувати для написання RDL. Ви можете створити повне визначення звіту від початку до кінця в будь-якій програмі .NET Framework за допомогою **XmlTextWriter**. Розробники також можуть додавати спеціальні елементи звіту з настроюваними властивостями, щоб розширити RDL.

## Типи RDL
У наведеній нижче таблиці перераховано типи та атрибути, які використовуються в елементах RDL.

|Тип|Опис|
---|---|
|Двійковий |Властивість із двійковим значенням у форматі base-64.|
|Логічний| Властивість зі значенням об’єкта true або false. Якщо не вказано інше, значенням пропущеного додаткового логічного об’єкта є False.|
|Дата |Властивість із повністю вказаною датою або значенням дати-часу, указаним у форматі дати ISO8601: РРРР-ММ-ДД[ЧТГ:ХМ[:СС[.С]]].|
|Enum |Властивість із текстовим значенням рядка, яке має бути одним зі списку визначених значень.|
|Float |Властивість із значенням float. Крапка (.) використовується як необов’язковий десятковий роздільник.|
|Ціле |Властивість із цілим значенням (int32).|
|Мова |Властивість із текстовим значенням, що містить код мови та культури, наприклад "en-us" для американської англійської мови. Значення має бути певною мовою або нейтральною мовою, для якої мова за замовчуванням визначена в Microsoft .NET Framework.|
|Назва |Властивість із текстовим значенням рядка. Імена мають бути унікальними в просторі імен елемента. Якщо не вказано, простір імен для елемента — це внутрішній об’єкт, що містить ім’я.|
|NormalizedString |Властивість із текстовим значенням рядка, яке було нормалізовано.|
|Розмір |Елемент розміру має містити число (із символом крапки, який використовується як додатковий десятковий роздільник). Після числа має йти позначення одиниці вимірювання довжини CSS, як-от см, мм, дюйм, пункт або шт. Пробіл між числом і позначником необов’язковий. Щоб отримати додаткові відомості про позначки розміру, див. Довідник про значення та одиниці CSS. У RDL максимальне значення для розміру становить 160 дюймів. Мінімальний розмір — 0 дюймів.|
|Рядок |Властивість із текстовим значенням рядка.|
|UnsignedInt |Властивість зі значенням цілого числа без знаку (uint32).|
|Варіант |Властивість з будь-яким простим типом XML.|

## Типи даних RDL
У RDL DataType Enumeration визначає тип даних атрибута, виразу або параметра. У наведеній нижче таблиці показано, як типи даних CLR відповідають типам даних RDL.

|Тип(и) CLR |Відповідний тип даних|
---|---|
|Логічний| Логічний|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Один, Двомісний |Float|
|Рядок, символ, GUID, проміжок часу |рядок|


## Посилання ##

- [Мова визначення звіту (Вікіпедія)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Мова визначення звітів (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

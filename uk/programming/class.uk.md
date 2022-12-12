{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class", "що таке файл класу", "як відкрити файл класу", "розширення", "файл", "файл класу", "формат файлу класу", "розширення .class ", "файл класу в java"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Клас - формат файлу класу Java",
  "description":"Дізнайтеся про формат файлу класу та API, які можуть створювати та відкривати файли класу.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Що таке файл класу?

**Файл класу в Java** — це скомпільований вихід класу [.java](/uk/programming/java/), який фактично виконується віртуальною машиною Java (JVM). Файли класів можуть виконуватися окремо, а також можуть бути частиною файлу [JAR](/uk/programming/jar/) як пакет разом з іншими файлами пакетів. Їх можна створити за допомогою команди **`javac`** з інтерфейсу командного рядка. Деякі Java IDE, як-от [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) і NetBeans, забезпечують створення вихідних файлів .class із Java проекту файли.

## Формат файлу класу

Файл класу Java містить байт-код, який є проміжним кодом для запуску JVM. Файл класу складається з потоку 8-бітних байтів і багатобайтових елементів даних завжди зберігаються в порядку старшого.

### Структура ClassFile

Структура файлу класу показана нижче.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
де:

* u1 = однобайтова кількість без знаку
* u2 = двобайтова кількість без знаку
* u4 = чотирибайтова кількість без знаку

Детальну інформацію про структуру файлу .class також описано в [форматі файлу класу] Oracle (https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html), і можна отримати посилання розробників для довідки. Короткий опис цих полів наведено нижче.

* `magic` - чарівний елемент надає магічне число, що ідентифікує формат файлу класу; він має значення 0xCAFEBABE.
* `minor_version`, `major_version` – значення елементів minor_version і major_version є номерами другорядної та основної версій цього файлу класу.
* `constant_pool_count` - значення елемента constant_pool_count дорівнює кількості записів у таблиці constant_pool плюс один. Індекс constant_pool вважається дійсним, якщо він більший за нуль і менший за constant_pool_count, за винятком констант типу long і double.
* `constant_pool[]` – Constant_pool — це таблиця структур (§4.4), що представляє різні рядкові константи, імена класів та інтерфейсів, імена полів та інші константи, на які посилаються в структурі ClassFile та її підструктурах. Формат кожного запису таблиці constant_pool вказується його першим байтом "tag".
* `access_flags` - значення елемента access_flags є маскою прапорів, які використовуються для позначення прав доступу та властивостей цього класу або інтерфейсу.
* `this_class` - значення елемента this_class має бути дійсним індексом у таблиці constant_pool.
* `super_class` - для класу значення елемента super_class має дорівнювати нулю або бути дійсним індексом у таблиці constant_pool.
* `interfaces_count` - значення елемента interfaces_count дає кількість прямих суперінтерфейсів цього класу або типу інтерфейсу.
* `interfaces[]` – кожне значення в масиві інтерфейсів має бути дійсним індексом у таблиці constant_pool.
* `fields_count` – значення поля fields_count визначає кількість структур field_info у таблиці fields.
* `fields[]` – кожне значення в таблиці fields має бути структурою field_info, яка дає повний опис поля в цьому класі або інтерфейсі.
* `methods_count` - значення елемента methods_count визначає кількість структур method_info у таблиці методів.
* `methods[]` – кожне значення в таблиці методів має бути структурою method_info, яка дає повний опис методу в цьому класі або інтерфейсі. Якщо жоден із прапорів ACC_NATIVE та ACC_ABSTRACT не встановлено в елементі access_flags структури method_info, інструкції віртуальної машини Java, що реалізують метод, також надаються.
* `attributes_count` - значення атрибутів_count елемента визначає кількість атрибутів (§4.7) у таблиці атрибутів цього класу.
* `attributes[]` – кожне значення таблиці атрибутів має бути структурою attribute_info.




## Список літератури

* [Формат файлу класу](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)


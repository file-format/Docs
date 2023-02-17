{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Вбудована мова Maya", "файл", "розширення", "формат файлу", "Maya 3D", "Посібник з програмування" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - формат файлу вбудованої мови Maya",
  "description":"Дізнайтеся про формат файлу MEL та API, які можуть створювати та відкривати файли MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Що таке файл MEL?

Файл із розширенням .mel (вбудована мова Maya) — це мова сценаріїв, яка використовується Autodesk Maya для створення графічних інтерфейсів. Він дозволяє автоматизувати створення графічних елементів за допомогою виконуваних сценаріїв на додаток до графічного інтерфейсу Maya. MEL дає змогу створювати графічні інтерфейси без вивчення програмування. Це досягається шляхом створення макросів і спеціальних дій, які прискорюють повторювані завдання. Ці процедури та сценарії дозволяють створювати власне моделювання, анімацію, динаміку та рендеринг завдань. Autodesk Maya 2020 можна використовувати для відкриття та перегляду вмісту файлу EML.

## Формат файлу MEL - Додаткова інформація

[Довідковий посібник для програміста](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) доступний для розробників у розділі документації Maya. MEL базується на командах сценаріїв оболонки, подібних до UINX, для досягнення результатів. Команди на основі сценаріїв роблять його невідповідним для традиційного та об’єктно-орієнтованого програмування (ООП), що призводить до відсутності використання структур даних, виклику функцій або використання ООП, як в інших мовах.

Деякі ключові моменти щодо MEL наведені нижче.

`Коментарі` - кожен оператор у MEL має закінчуватися крапкою з комою (;), навіть у кінці блоку.

`Значення, що повертаються` – вказівка виразу, який повертає значення, не друкує значення автоматично в MEL. Натомість це викликає помилку.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Команди для створення, редагування та видалення` - та сама команда використовується для створення речей, редагування речей або запиту інформації про існуючі речі. Однак прапор керує тим, що (створення, редагування або запит) виконує команда.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Значення, що повертається функцією` – синтаксис функції автоматично повертає значення. Щоб отримати значення, що повертається, за допомогою синтаксису команди, потрібно взяти команду у зворотні лапки.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Список літератури

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

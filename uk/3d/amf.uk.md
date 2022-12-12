{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "файл amf", "формат файлу amf", "формат файлу", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу AMF та API, які можуть відкривати та створювати файли AMF.",
  "title" :"AMF - файл аддитивного виробництва",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл AMF?
Файл AMF містить вказівки щодо опису об’єктів для використання в процесах адитивного виробництва. Він містить отвір<amf> Тег XML і закінчується на a</amf> елемент. Цьому передує рядок декларації XML із зазначенням версії XML і кодування файлу. Декларації можуть містити інформацію про одиниці вимірювання, а за відсутності такої інформації міліметри використовуються як одиниці вимірювання за умовчанням.


## Формат файлу AMF

Формат файлу Additive Manufacturing (**AMF**) визначає відкриті стандарти для опису об’єктів, щоб їх можна було використовувати в процесах адитивного виробництва, таких як 3D-друк. Програми САПР використовують формат файлу AMF, використовуючи таку інформацію, як геометрія, колір і матеріал об’єктів. Формат AMF відрізняється від формату STL, оскільки боковий не підтримує колір, матеріали, решітки та сузір’я.

### Елементи файлу AMF

П'ять елементів верхнього рівня, визначені за допомогою<AMF> теги, як описано нижче. Наявність єдиного елемента об’єкта є обов’язковою для повнофункціонального файлу AMF.

`<object> ` - Елемент об'єкта визначає обсяг або обсяги матеріалу, кожен з яких пов'язаний з ідентифікатором матеріалу для друку. Принаймні один елемент об'єкта повинен бути присутнім у файлі. Додаткові об’єкти необов’язкові.

`<material> ` – додатковий елемент material визначає один або кілька матеріалів для друку з ідентифікатором відповідного матеріалу. Якщо елемент матеріалу не включено, передбачається один матеріал за замовчуванням.

`<texture> ` – необов’язковий елемент текстури визначає одне або кілька зображень або текстур для відображення кольору або текстури, кожне з пов’язаним ідентифікатором текстури.

`<constellation> ` – необов’язковий елемент сузір’я ієрархічно поєднує об’єкти та інші сузір’я у відносний шаблон для друку.

`<metadata> ` – необов’язковий елемент метаданих визначає додаткову інформацію про об’єкт(и) та елементи, що містяться у файлі.

## Приклад AMF

Нижче наведено приклад файлу AMF, який можна скопіювати у файл [text](/uk/word-processing/txt/) і зберегти як стиснутий файл [zip](/uk/compression/zip/) для відкриття.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Список літератури

* [AMF - Вікіпедія](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Специфікації AMF щодо ISO](https://www.iso.org/standard/67472.html)


{
  "date" : "2020-03-16",
  "keywords" :[ "Файл IGES", "Формат файлу", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу IGES та API, які можуть створювати та відкривати файли IGES.",
  "title" :"Формат файлу IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Що таке файл IGES?

Файл із розширенням .iges використовується для обміну проектною інформацією між програмами автоматизованого проектування (CAD). IGES означає Initial Graphics Exchange Specifications. Інформація, якою обмінюються за допомогою IGES, включає принципову схему, каркас, поверхню довільної форми або представлення твердотільного моделювання. IGES знаходить застосування в традиційних інженерних кресленнях, аналізі моделей і функціях виробництва. Цей формат може обмінюватися як двовимірною, так і тривимірною інформацією про дизайн між програмами САПР. Файли IGES можна відкривати за допомогою кількох програм САПР, таких як Autodesk і CADSoftTools ABViewer. Існує також кілька доступних API для програмного відкриття та перетворення файлів IGES.

## Формат файлу IGES

Файли IGES мають текстовий формат ASCII і їх можна відкрити в будь-якому текстовому редакторі для перегляду вмісту файлу. Текстова інформація у файлі IGES представлена у форматі "Hollerith". Звичайний файл IGES може містити тисячі рядків для представлення 2D або 3D інформації, якою можна обмінюватися відповідно до цього формату. Файл IGES розділений на п’ять розділів, які позначаються великою літерою в 73-му стовпці. Це розділи «Початок» (S), «Глобальний» (G), «Введення даних» (D), «Дані параметрів» (P) і «Завершення» (T). Розділи «Введення даних» і «Дані параметрів» зазвичай позначаються абревіатурами DE і PD відповідно.

### Заголовок файлу IGES

Розділи «Початок» і «Загальний» містять основну інформацію про:
* Назва файлу та його джерело
* Роздільники для розділу параметрів
* Автор файлу та інша загальна інформація.

Розділи «Початок» і «Глобальний» із прикладу документа у Вікіпедії наведені нижче.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Як можна побачити, початкове поле містить зрозумілі людині описи файлу, і я маю будь-які символи в стовпцях 1-72, при цьому рядок закінчується заголовком розділу та номером рядка розділу. Повинен бути хоча б 1 рядок розділу «Пуск». Глобальний розділ містить дані препроцесора. Він також має бути присутнім у файлі та закінчуватися форматом G000000#.

### Розділ введення даних (DE) і даних параметрів (PD).

#### Розділ введення даних
Файл IGES складається з кількох сутностей, які містять інформацію про основні дані формату файлу IGES. Сутність містить інформацію про різні елементи формату даних IGES і використовується для малювання. Більш часто використовувані сутності включають:
* Дуга кола
* Композитна крива
* Конічна дуга
* Літак
* Лінія

Це лише деякі з них, а в IGES близько 150 різних об’єктів. Кожна сутність ідентифікується номером типу, наприклад:
* ДУГА КОЛО (Тип 100)
* ЛІНІЯ (Тип 110)

##### Властивості сутності

Кожна оголошена сутність має такі властивості.

|Назва поля|Опис|
---|---|
|Тип сутності |Це тип сутності, що описується. Наприклад, 116 описує сутність Point.|
|Покажчик PD |Це вказує розташування даних сутностей у розділі параметрів. Це просто номер рядка в розділі PD, який містить перший рядок даних цієї сутності.|
|Структура |Нуль або вказівник на сутність визначення. Не застосовується для більшості організацій|
|Шрифт лінії| Номер або вказівник на сутність шаблону рядкового шрифту. Число означає: * 0 Шаблон не вказано (за замовчуванням) * 1 Суцільний * 2 Штриховий * 3 Фантом * 4 Центральна лінія * 5 Пунктирний|
|Рівень| Визначає рівні, пов’язані з цією сутністю. Дозволяє об’єкту відображатися на кількох рівнях|
|Перегляд| Визначає параметри перегляду. Це: 0 Вказує на однакову видимість і характеристики в усіх поданнях. Покажчик за замовчуванням на сутність View (тип 410), з якої її можна переглянути. Посилання на сутність видимої асоціативності View (тип 402, форма 3)
|Покажчик матриці перетворення| Посилається на сутність матриці перетворення (тип 124) або дорівнює нулю за замовчуванням (без перетворення)|
|Асоціативність відображення мітки| Посилається на асоціативність відображення мітки (тип 402, форма 5), яка визначає, як відображається мітка сутності.|
|Номер статусу| Містить чотири розділи по два номери. 1-2: Пустий статус. 00 для нормального або 01 для порожнього. 3-4: Перемикач підпорядкованого об’єкта: 00 для незалежного, 01 для фізично залежного, 02 для логічно залежного та 03 для обох. 5-6: Прапор використання сутності: 00 для геометрії, 01 для анотації, 02 для визначення, 03 для іншого, 04 для логічного, 05 для параметричного 2D та 06 для геометрії конструкції. Нарешті, 7-8 – це ієрархія, де 00 вказує на глобальний напрям зверху вниз (використовуйте характеристики цієї сутності), 01 – глобальну відкладену (не використовуйте характеристики цієї сутності), а 02 – використання властивості ієрархії (використовуйте сутність ієрархії (тип 406, форма) 10) визначити характеристики ієрархічного групування).|
|Порядковий номер| Визначається D#, де # — це номер рядка для цього розділу (не з початку файлу). Це також використовується для вказівки на цю сутність введення даних.|
|Тип сутності| воно вказується двічі для списку сутностей|
|Номер ваги лінії| Визначає товщину під час відображення сутності. Найменший — 1, 0 — за умовчанням|
|Номер кольору| Визначає колір сутності. Дозволені цілі значення: 0 Без кольору (за замовчуванням) 1 Чорний 2 Червоний 3 Зелений 4 Синій 5 Жовтий 6 Маджента 7 Блакитний 8 Білий|
|Параметр Кількість рядків| Визначає кількість рядків, які займає ця сутність у розділі даних параметрів|
|Номер форми| Вказує на форму або представлення цієї сутності. Змінює спосіб інтерпретації даних параметрів. За замовчуванням 0|
|Заповідне поле| Не використовується|
|Заповідне поле| Не використовується|
|Мітка сутності| Ідентифікатор, визначений програмою - вирівнювання по правому краю|
|Нижковий номер| Числовий кваліфікатор для мітки сутності. Обидва разом утворюють унікальний ідентифікатор для сутності|
|Порядковий номер Див. вище. |Це буде D#+1, оскільки кожна сутність указана у двох рядках.|

#### Розділ даних параметрів
За розділом «Записи даних» слідує розділ «Дані параметрів». У ньому наведено дані для кожного відповідного запису та параметри для сутності на основі роздільників, указаних у розділі Global (зазвичай коми для розділення параметрів і крапка з комою для завершення списку).


## Список літератури
* [IGES від WikiPedia](https://en.wikipedia.org/wiki/IGES)

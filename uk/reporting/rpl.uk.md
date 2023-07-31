{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - макет сторінки звіту",
  "keywords" :[ "rpl", "Макет сторінки звіту", "XSD", "SQL Server", "звітування"],
  "description":"Дізнайтеся про формат потоку RPL, який є внутрішнім двійковим форматом, який використовується службами звітування Microsoft SQL Server під час контакту з елементами керування переглядачем.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Що таке файл RPL? ##

Формат потоку RPL (макет сторінки звіту) — це внутрішній двійковий формат, який використовується MS SQL Server Reporting Services під час зв’язку з елементами керування переглядачем, щоб зменшити частину роботи з відтворення від сервера до клієнтського елемента керування переглядачем. Розробники можуть створювати користувацькі конструктори звітів за допомогою RPL, який генеруватиме RPL, а також спеціальні рендерери звітів, які обробляють і відображають файл RPL для відображення звітів.

## Структури RPL

Потік RPL включає структуру потоку, структуру звіту, властивості звіту та перерахування. Кожна структура включає наступне:

- Визначення структури.

- Граматика доповненої форми Бекуса-Наура (ABNF) для структури.

- Розрядна схема структури.

- Визначення всіх полів, що містяться в структурі.

Ось короткі примітки щодо деяких структур RPL:

### Структура потоку
Структура потоку складається з серії записів. Запис містить нуль або більше структурованих полів, які містять макет звіту.

#### Потік RPL
Потік RPL має містити лише один запис звіту, а потік має бути серією двійкових записів, які зберігають ієрархію звіту.

#### Запис
Запис — це основний будівельний блок, який використовується для збереження інформації про звіт. Запис складається з послідовності байтів різної довжини. Запис складається з двох компонентів:
- Тип запису
- Дані запису, характерні для цього типу запису.
Тип запису — це один байт, який визначає, який тип інформації визначено записом і як структура даних запису, що стосуються запису, впорядкована та структурована. Значення запису залежить від типу даних, які стосуються цього запису.

#### Прості структури типів даних

У наведеній нижче таблиці визначено типи даних у потоці RPL.

|Опис| формат|
---|---|
|Char|Представляє 16-бітне (2-байтове) числове (порядкове) значення.|
|Байт|Представляє 8-бітне (1-байтове) ціле число без знаку.|
|Int16|Представляє 16-бітне (2-байтове) ціле число зі знаком.|
|Single|Представляє 32-бітове (4-байтове) значення з плаваючою комою одинарної точності.|
|Decimal|Представляє 128-бітний (16-байтний) тип даних.|
|DateTime|Представляє 64-бітове (8-байтове) кодування значення дати й часу.|
|Int64|Представляє 64-розрядне (8-байтове) ціле число зі знаком.|
|Int32|Представляє 32-розрядне (4-байтове) ціле число зі знаком.|
|Float|Представляє 32-бітове (4-байтове) значення з плаваючою комою одинарної точності.|
|Boolean|Представляє 8-бітове (1-байтове) логічне значення булевого типу. Дійсні значення: true (1) і false (0).|
|Long|Представляє 64-бітове (8-байтове) ціле число зі знаком.|
|Рядок|Усі рядкові значення в протоколі ПОВИННІ бути UNICODE UTF-16. За замовчуванням усі значення String починаються з цілого числа, яке визначає довжину String. Рядкові значення представлені в протоколі у вигляді масиву байтів; кількість байтів ПОВИННА дорівнювати кількості символів у рядку, помноженій на два.|

### Структури звітів
Структури звіту містять визначення та розміри відповідних структур і елементів.

Наступний список визначає структури звіту:

- Доповідь
- Версія
- Властивості звіту
- Зсув елемента масиву
- Вміст сторінки
- Сторінка
- Властивості сторінки
- Макет сторінки
- Розділ
- Простий розділ
- Змішаний розділ
- Властивості розділу
- Елемент області тіла
- Елемент заголовка сторінки
- Елемент нижнього колонтитула сторінки
- Елемент тіла
- Властивості елемента
- Спільні властивості елемента
- Використовуйте властивості спільного елемента
- InlineSharedElementProperties
- NonSharedElementProperties
- Стиль
- SharedStyleProperties
- NonSharedStyleProperties
- ActionInfo
- ActionInfoContent
- Дія
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- Елемент звіту
- Лінія
- Імідж
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- Дані зображення
- ImageMapAreas
- ImageMapArea
- Діаграма
- GaugePanel
- Карта
- Прямокутник
- Підзвіт
- RichTextBox
- Вміст абзацу
- TextRun
- Абзац
- RichTextBoxStructure
- Таблікс
- TablixContent
- TablixStructure
- TablixMeasurements
- ColumnsWidths
- Інформація про стовпець
- Висота рядків
- RowInfo
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Вимірювання
- Вимірювання
- ReportElementEnd

### Властивості
Нижче наведено список властивостей, які можна використовувати в потоці RPL:

- ID
- Підрахунок стовпців
- Інтервал між стовпцями
- Унікальне ім'я
- Ім'я
- Етикетка
- Закладка
- Підказка
- ToggleItem
- Опис
- Місцезнаходження
- ConsumeContainerWhiteSpace (RPL 10.6)
- Мову
- Час виконання
– Автор
- Автооновлення
- Назва звіту
- Висота сторінки
- PageWidth
- MarginTop
- MarginLeft
- MarginRight
- MarginBottom
- Стовпці
- Назва сторінки (RPL 10.6)
- Коса
- Може рости
- CanShrink
- Значення
- ToggleState
- CanSort
- SortState
- Формула
- IsToggleParent
- TypeCode
- Оригінальне значення
- Це просто
- ContentOffset
- Назва потоку
- Розміри
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- Назва зображення
- Ширина
- Висота
- Горизонтальна роздільна здатність
- Вертикальна роздільна здатність
- RawFormat
- Гіперпосилання
- Посилання на закладку
- DrillthroughId
- DrillthroughUrl
- BorderColor
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- BorderStyle
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- BorderWidth
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- PaddingRight
- PaddingTop
- PaddingBottom
- Стиль шрифту
- FontFamily
- Розмір шрифту
- FontWeight
- Формат
- TextDecoration
- Вирівнювання тексту
- Вертикальне вирівнювання
- Колір
- Висота лінії
- Напрямок
- Режим письма
- UnicodeBiDi
- Фонове зображення
- Колір фону
- Фонове повторення
- Числівна мова
- NumeralVariant
- Календар
- Рядки заголовків стовпців
- Заголовок рядка Стовпці
- ColsBeforeRowHeader
- LayoutDirection
- Шлях визначення
- Рівень
- MemberCellIndex
- CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- Індекс стовпця
- RowIndex
- Мітка групи
- RecursiveToggleLevel
- ListStyle
- ListLevel
- Номер абзацу
- Відступ справа
- Відступ зліва
- Висячий відступ
- SpaceBefore
- SpaceAfter
- Перша лінія
- Розмітка
- ContentTop
- ContentLeft
- ContentWidth
- ContentHeight
- Держава
- CellItemState
- MemberDefState

### Перерахування
У наведеному нижче списку показано перерахування, які можна використовувати в потоці RPL:

- Параметри сортування
- Розміри
- ShapeType
- ImageRawFormat
- Стилі шрифтів
- Вага шрифту
- TextDecorations
- Вирівнювання тексту
- Вертикальні вирівнювання
- Напрямки
- Режими написання
- UnicodeBiDiTypes
- Календарі
- Стилі меж
- BackgroundRepeatTypes
- ListStyles
- Стилі розмітки
- TypeCode
- StateValues
- TablixMemberStateValues
- TablixMemberDefStateValues
- Розмір RPLS





## Посилання ##

- [Формат бінарного потоку макета сторінки звіту (RPL)](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)


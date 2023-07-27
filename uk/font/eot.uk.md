{
  "date" : "2020-08-20",
  "keywords" :[ "файл eot", "формат файлу eot", "що таке файл eot", "файл", "приклад eot", "розширення файлу eot", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - формат файлу шрифту TrueType",
  "description":"Дізнайтеся про формат файлу EOT та API для створення та відкриття файлів EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Що таке файл EOT?

Файл із розширенням .eot — це шрифт OpenType, вбудований у документ. Вони здебільшого використовуються у веб-файлах, таких як веб-сторінки. Він був створений Microsoft і підтримується продуктами Microsoft, включаючи файл презентації PowerPoint [.pps](/uk/presentation/pps). Файл не призначений для основного використання, а є свого роду супровідним документом до основного документа або веб-сторінки. Подібно до шрифтів OTF, EOT підтримує контури Postscript і TrueType для гліфів. Файли EOT менші за розміром через те, що вони стискаються за допомогою стиснення LZ. EOT використовує інструмент Microsoft для створення шрифту з існуючих шрифтів TTF/OTF.

## Коротка історія

Шрифт EOT був представлений W3C у 2007 році як частина CSS3, але через його вимоги до постійного встановлення на віддаленій системі стало причиною його відхилення. Він був повторно поданий у березні 2008 року, але W3C зрештою вибрав [Формат веб-шрифту](/uk/font/woff/) (WOFF), який тоді був стандартизований.

## Формат файлу EOT

Деталі формату файлу EOT можна знайти на [сторінці подання W3](https://www.w3.org/Submission/EOT/#FileFormat) і детально описує структуру, яку використовує цей формат шрифту. EOT складається з єдиної структури EMBEDDEDFONT, яка надає достатньо базової інформації про назву шрифту та підтримувані символи. Упаковка цієї інформації дозволяє агентам користувача уникнути розпакування, розпакування або встановлення шрифту, якщо він уже присутній на машині.

### Структура EMBEDDEDFONT
Структура EMBEDDEDFONT зазнала трьох переглядів із додаванням додаткових даних у кінці структури з кожним переглядом. Остання версія структури EMBEDDEDFONT виглядає так, як показано нижче.

|Тип даних|Назва запису|Опис|
---|---|---|
|unsigned long|EOTSize|Загальна довжина структури в байтах (включаючи дані рядка та шрифту)|
|unsigned long|FontDataSize|Довжина шрифту OpenType (FontData) у байтах|
|unsigned long|Version|Номер версії цього формату - 0x00020002|
|unsigned long|Flags|Processing Flags|
|byte[10]|FontPANOSE|Значення PANOSE для цього шрифту – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|У Windows це похідне від TEXTMETRIC.tmCharSet. Це значення визначає набір символів шрифту. DEFAULT_CHARSET (0x01) вказує на відсутність уподобань. - Див. https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|курсив|Якщо біт для ITALIC установлено в OS/2.fsSelection, значення буде 0x01 - див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Вага|Значення ваги для цього шрифту – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Позначки типу, які надають інформацію про дозволи на вбудовування – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|Магічне число для файлу EOT - 0x504C. Використовується для перевірки даних на пошкодження.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (біти 0-31) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (біти 32-63) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (біти 64-95) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (біти 96-127) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (біти 0-31) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (біти 32-63) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment – Див. https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|Reserved - має бути 0|
|unsigned long|Reserved2|Reserved - має бути 0|
|unsigned long|Reserved3|Reserved - має бути 0|
|unsigned long|Reserved4|Reserved - має бути 0|
|unsigned short|Padding1|Заповнення для підтримки довгого вирівнювання. Значення заповнення завжди має бути 0x0000.|
|unsigned short|FamilyNameSize|Кількість байтів, які використовуються масивом FamilyName|
|байт|НазваРодини[РозмірРодини]|Масив із символів UTF-16 довжиною в байти РозмірРодини. Це рядок сімейства шрифтів англійської мови, знайдений у таблиці імен шрифту (ідентифікатор назви = 1) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Значення заповнення завжди має бути встановлено на 0x0000.|
|unsigned short|StyleNameSize|Кількість байтів, використовуваних StyleName|
|byte|StyleName[StyleNameSize]|Масив символів UTF-16 довжиною StyleNameSize байтів. Це рядок підсімейства шрифтів англійської мови, знайдений у таблиці імен шрифту (ідентифікатор імені = 2) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Значення заповнення завжди має бути встановлено на 0x0000.|
|unsigned short|VersionNameSize|Кількість байтів, які використовує VersionName|
|bytes|VersionName[VersionNameSize]|Масив символів UTF-16 довжиною в VersionNameSize байтів. Це рядок англійської версії, знайдений у таблиці імен шрифту (ідентифікатор назви = 5) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Значення заповнення завжди має бути встановлено на 0x0000.|
|unsigned short|FullNameSize|Кількість байтів, які використовує FullName|
|byte|FullName[FullNameSize]|Масив символів UTF-16 довжиною в FullNameSize байтів. Це рядок повної назви англійською мовою, знайдений у таблиці імен шрифту (ідентифікатор назви = 4) – див. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Значення заповнення завжди має бути 0x0000.|
|unsigned short|RootStringSize|Кількість байтів, які використовуються масивом RootString|
|byte|RootString[RootStringSize]|Масив символів UTF-16 довжиною RootStringSize байтів.|
|unsigned long|RootStringCheckSum|Значення контрольної суми RootString. Нижче наведено алгоритм обробки RootStringChecksum.|
|unsigned long|EUDCCodePage|Значення кодової сторінки, необхідне для підтримки шрифту EUDC.|
|unsigned short|Padding6|Значення заповнення завжди має бути встановлено на 0x0000.|
|unsigned short|SignatureSize|Кількість байтів, які використовуються масивом Signature. Наразі зарезервовано та має бути встановлено на 0x0000.|
|байт|Підпис[SignatureSize]|Наразі зарезервовано. Якщо SignatureSize дорівнює 0x0000, цей масив не має довжини.|
|unsigned long|EUDCFlags|Прапори обробки для шрифту EUDC. Типовими значеннями можуть бути TTEMBED_XORENCRYPTDATA і TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Кількість байтів, які використовуються масивом Signature.|
|byte|EUDCFontData[EUDCFontSize]|Кількість байтів, що використовуються для даних шрифту EUDC. Якщо EUDCFontSize дорівнює 0x00000000, цей масив не має довжини.|
|byte|FontData[FontDataSize]|Дані шрифту для цього файлу EOT. Дані можуть бути стиснуті або зашифровані XOR, як зазначено прапорами обробки.|

## Список літератури

* [Формат файлу EOT](https://www.w3.org/Submission/EOT/)
* [Вбудований OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Вбудовування шрифту](https://en.wikipedia.org/wiki/Font_embedding)


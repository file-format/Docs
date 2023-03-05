{
  "date" : "2020-08-20",
  "keywords" :[ "файл EOT", "формат файла EOT", "что такое файл EOT", "файл", "пример EOT", "расширение файла EOT", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT — формат файла шрифта TrueType",
  "description":"Узнайте о формате файлов EOT и API для создания и открытия файлов EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## .EOT вариант №

Файл с расширением .eot — это шрифт OpenType, встроенный в документ. Они в основном используются в веб-файлах, таких как веб-страницы. Он был создан Microsoft и поддерживается продуктами Microsoft, включая файл презентации PowerPoint [.pps](/ru/presentation/pps). Файл не имеет основного назначения и является своего рода сопроводительным документом к основному документу или веб-странице. Подобно шрифтам OTF, EOT поддерживает контуры Postscript и TrueType для глифов. Файлы EOT имеют меньший размер по той причине, что они сжаты с использованием сжатия LZ. EOT использует инструмент Microsoft для создания шрифта из существующих шрифтов TTF/OTF.

## Краткая история

Шрифт EOT был представлен W3C в 2007 году как часть CSS3, но из-за его требований к постоянной установке в удаленной системе стал причиной его отклонения. Он был повторно представлен в марте 2008 года, но W3C в конечном итоге выбрал [формат веб-шрифта](/ru/font/woff/) (WOFF), который тогда был стандартизирован.

## Формат файла EOT

Подробную информацию о формате файла EOT можно найти на [странице отправки W3](https://www.w3.org/Submission/EOT/#FileFormat), где подробно описана структура, используемая этим форматом шрифта. EOT состоит из одной структуры EMBEDDEDFONT, которая предоставляет достаточно базовой информации о имени шрифта и поддерживаемых символах. Упаковка этой информации позволяет агентам пользователя избежать распаковки, распаковки или установки шрифта, если он уже присутствует на машине.

### Структура EMBEDDEDFONT
Структура EMBEDDEDFONT претерпела три ревизии с добавлением дополнительных данных в конце структуры с каждой ревизией. Последняя версия структуры EMBEDDEDFONT показана ниже.

|Тип данных|Имя записи|Описание|
---|---|---|
|unsigned long|EOTSize|Общая длина структуры в байтах (включая данные строки и шрифта)|
|unsigned long|FontDataSize|Длина шрифта OpenType (FontData) в байтах|
|unsigned long|Версия|Номер версии этого формата — 0x00020002|
|unsigned long|Флаги|Флаги обработки|
|byte[10]|FontPANOSE|Значение PANOSE для этого шрифта — см. http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|В Windows это производное от TEXTMETRIC.tmCharSet. Это значение определяет набор символов шрифта. DEFAULT_CHARSET (0x01) указывает отсутствие предпочтения. - См. http://msdn2.microsoft.com/en-us/library/ms534202.aspx|
|byte|Italic|Если в OS/2.fsSelection установлен бит для ITALIC, значение будет 0x01 — см. http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|Значение веса для этого шрифта — см. http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Типовые флаги, предоставляющие информацию о разрешениях на встраивание — см. http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|Magic number для файла EOT — 0x504C. Используется для проверки на повреждение данных.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (биты 0–31) — см. http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (биты 32–63) — см. http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (биты 64–95) — см. http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (биты 96–127) — см. http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (биты 0–31) — см. http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (биты 32–63) — см. http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment — см. http://www.microsoft.com/typography/otspec/head.htm|
|unsigned long|Reserved1|Reserved — должно быть 0|
|unsigned long|Reserved2|Reserved — должно быть 0|
|unsigned long|Reserved3|Reserved — должно быть 0|
|unsigned long|Reserved4|Reserved — должно быть 0|
|unsigned short|Padding1|Padding для сохранения выравнивания по длине. Значение заполнения всегда должно быть установлено на 0x0000.|
|unsigned short|FamilyNameSize|Число байтов, используемых массивом FamilyName|
|byte|FamilyName[FamilyNameSize]|Массив символов UTF-16 длиной FamilyNameSize в байтах. Это строка семейства шрифтов для английского языка, найденная в таблице имен шрифта (идентификатор имени = 1). См. http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|Значение заполнения всегда должно быть установлено на 0x0000.|
|unsigned short|StyleNameSize|Число байтов, используемых StyleName|
|byte|StyleName[StyleNameSize]|Массив символов UTF-16 длиной StyleNameSize в байтах. Это строка подсемейства шрифтов английского языка, найденная в таблице имен шрифта (идентификатор имени = 2). См. http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|Значение заполнения всегда должно быть установлено на 0x0000.|
|unsigned short|VersionNameSize|Число байтов, используемых VersionName|
|bytes|VersionName[VersionNameSize]|Массив символов UTF-16 длиной в байтах VersionNameSize. Это строка версии на английском языке, найденная в таблице имен шрифта (идентификатор имени = 5). См. http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|Значение заполнения всегда должно быть установлено на 0x0000.|
|unsigned short|FullNameSize|Число байтов, используемых FullName|
|byte|FullName[FullNameSize]|Массив символов UTF-16 длиной FullNameSize в байтах. Это строка полного имени на английском языке, найденная в таблице имен шрифта (идентификатор имени = 4). См. http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|Значение заполнения всегда должно быть установлено на 0x0000.|
|unsigned short|RootStringSize|Число байтов, используемых массивом RootString|
|byte|RootString[RootStringSize]|Массив символов UTF-16 длиной RootStringSize в байтах.|
|unsigned long|RootStringCheckSum|Значение контрольной суммы RootString. См. алгоритм обработки RootStringChecksum ниже.|
|unsigned long|EUDCodePage|Значение кодовой страницы, необходимое для поддержки шрифтов EUDC.|
|unsigned short|Padding6|Значение заполнения всегда должно быть установлено на 0x0000.|
|unsigned short|SignatureSize|Число байтов, используемых массивом Signature. В настоящее время зарезервировано и должно быть установлено на 0x0000.|
|byte|Signature[SignatureSize]|В настоящее время зарезервировано. Если SignatureSize равен 0x0000, этот массив не имеет длины.|
|unsigned long|EUDCFlags|Флаги обработки для шрифта EUDC. Типичными значениями могут быть TTEMBED_XORENCRYPTDATA и TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Число байтов, используемых массивом подписи.|
|byte|EUDCFontData[EUDCFontSize]|Количество байтов, используемых для данных шрифта EUDC. Если EUDCFontSize равен 0x00000000, этот массив не имеет длины.|
|byte|FontData[FontDataSize]|Данные шрифта для этого файла EOT. Данные могут быть сжаты или зашифрованы XOR, как указано в флагах обработки.|

## использованная литература

* [Формат файла EOT](https://www.w3.org/Submission/EOT/)
* [Встроенный OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Внедрение шрифта](https://en.wikipedia.org/wiki/Font_embedding)


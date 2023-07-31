{
  "date" : "2020-08-20",
  "keywords" :[ "eot файл", "eot файлов формат", "какво е eot файл", "файл", "eot пример", "eot файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - TrueType Font File Format",
  "description":"Научете за EOT файловия формат и API за създаване и отваряне на EOT файлове.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Какво е EOT файл?

Файл с разширение .eot е OpenType шрифт, който е вграден в документ. Те се използват най-вече в уеб файлове като уеб страница. Създаден е от Microsoft и се поддържа от продукти на Microsoft, включително файл с презентация на PowerPoint [.pps](/bg/presentation/pps/). Файлът не е за основна употреба и е нещо като придружаващ документ към основния документ или уеб страница. Подобно на OTF шрифтовете, EOT поддържа както Postscript, така и TrueType очертания за глифовете. EOT файловете са с по-малък размер поради причината, че са компресирани чрез LZ компресия. EOT използва инструмент на Microsoft за създаване на шрифт от съществуващи TTF/OTF шрифтове.

## Кратка история

Шрифтът EOT беше представен на W3C през 2007 г. като част от CSS3, но поради изискванията му да бъде постоянно инсталиран на отдалечена система стана причина за отхвърлянето му. Беше изпратен отново през март 2008 г., но W3C в крайна сметка избра [Формат на уеб шрифта](/bg/font/woff/) (WOFF), който беше стандартизиран тогава.

## EOT файлов формат

Подробностите за файловия формат на EOT могат да бъдат намерени на [страницата за изпращане на W3](https://www.w3.org/Submission/EOT/#FileFormat) и уточняват структурата, използвана от този формат на шрифта. EOT се състои от една структура EMBEDDEDFONT, която предоставя достатъчно основна информация за името на шрифта и поддържаните знаци. Опаковането на тази информация позволява на потребителските агенти да избегнат разопаковането, декомпресирането или инсталирането на шрифта, ако той вече присъства на машината.

### Структура на EMBEDDEDFONT
Структурата EMBEDDEDFONT е претърпяла три ревизии, с добавяне на допълнителни данни в края на структурата с всяка ревизия. Последната ревизия на структурата EMBEDDEDFONT е както е показано по-долу.

|Тип данни|Име на запис|Описание|
---|---|---|
|unsigned long|EOTSize|Обща дължина на структурата в байтове (включително данни за низ и шрифт)|
|unsigned long|FontDataSize|Дължина на OpenType шрифта (FontData) в байтове|
|неподписан дълъг|Версия|Номер на версията на този формат - 0x00020002|
|неподписани дълги|Флагове|Флагове за обработка|
|byte[10]|FontPANOSE|Стойността на PANOSE за този шрифт – Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|В Windows това се извлича от TEXTMETRIC.tmCharSet. Тази стойност определя набора от знаци на шрифта. DEFAULT_CHARSET (0x01) показва липса на предпочитание. - Вижте https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Ако битът за ITALIC е зададен в OS/2.fsSelection, стойността ще бъде 0x01 - Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Weight|Стойността на теглото за този шрифт - Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Флагове за тип, които предоставят информация за разрешенията за вграждане - Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|Магическо число за EOT файл - 0x504C. Използва се за проверка за повреда на данните.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (битове 0-31) – Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (битове 32-63) – Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (битове 64-95) – Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (битове 96-127) – Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (битове 0-31) – Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (битове 32-63) – Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment – Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|Reserved - трябва да бъде 0|
|unsigned long|Reserved2|Reserved - трябва да бъде 0|
|unsigned long|Reserved3|Reserved - трябва да бъде 0|
|unsigned long|Reserved4|Reserved - трябва да бъде 0|
|unsigned short|Padding1|Попълване за поддържане на дълго подравняване. Стойността на запълване винаги трябва да бъде зададена на 0x0000.|
|unsigned short|FamilyNameSize|Брой байтове, използвани от масива FamilyName|
|byte|FamilyName[FamilyNameSize]|Масив от UTF-16 символи с дължина от FamilyNameSize байтове. Това е низът от семейството на шрифтовете на английски език, който се намира в таблицата с имена на шрифта (идентификатор на име = 1) – вижте https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Стойността на запълването винаги трябва да бъде зададена на 0x0000.|
|unsigned short|StyleNameSize|Брой байтове, използвани от StyleName|
|byte|StyleName[StyleNameSize]|Масив от UTF-16 символи с дължина StyleNameSize байтове. Това е низът на подсемейството на шрифта на английски език, който се намира в таблицата с имена на шрифта (ID на името = 2) – вижте https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Стойността на запълването винаги трябва да бъде зададена на 0x0000.|
|unsigned short|VersionNameSize|Брой байтове, използвани от VersionName|
|bytes|VersionName[VersionNameSize]|Масив от UTF-16 символи с дължина VersionNameSize байтове. Това е низът на версията на английски език, който се намира в таблицата с имена на шрифта (идентификатор на име = 5) - Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Стойността на запълването винаги трябва да бъде зададена на 0x0000.|
|unsigned short|FullNameSize|Брой байтове, използвани от пълното име|
|byte|FullName[FullNameSize]|Масив от UTF-16 символи с дължина FullNameSize байтове. Това е низът с пълно име на английски език, който се намира в таблицата с имена на шрифта (ID на името = 4) - Вижте https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Стойността на запълването винаги трябва да бъде зададена на 0x0000.|
|unsigned short|RootStringSize|Брой байтове, използвани от масива RootString|
|byte|RootString[RootStringSize]|Масив от UTF-16 символи с дължина RootStringSize байтове.|
|unsigned long|RootStringCheckSum|Стойност на RootString CheckSum. Вижте алгоритъма за обработка на RootStringChecksum по-долу.|
|unsigned long|EUDCCodePage|Стойност на кодовата страница, необходима за поддръжка на EUDC шрифт.|
|unsigned short|Padding6|Стойността на запълването винаги трябва да бъде зададена на 0x0000.|
|unsigned short|SignatureSize|Брой байтове, използвани от масива Signature. В момента е запазено и трябва да бъде зададено на 0x0000.|
|byte|Подпис[SignatureSize]|В момента запазено. Ако SignatureSize е 0x0000, този масив няма дължина.|
|unsigned long|EUDCFlags|Флагове за обработка на EUDC шрифта. Типичните стойности може да са TTEMBED_XORENCRYPTDATA и TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Брой байтове, използвани от масива Signature.|
|байт|EUDCFontData[EUDCFontSize]|Брой байтове, използвани за данните за EUDC шрифта. Ако EUDCFontSize е 0x00000000, този масив няма дължина.|
|byte|FontData[FontDataSize]|Данните за шрифта за този EOT файл. Данните могат да бъдат компресирани или криптирани чрез XOR, както е посочено от флаговете за обработка.|

## Препратки

* [EOT файлов формат](https://www.w3.org/Submission/EOT/)
* [Вграден OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Вграждане на шрифт](https://en.wikipedia.org/wiki/Font_embedding)


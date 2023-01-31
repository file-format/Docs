{
  "date" : "2020-08-20",
  "keywords" :[ "cff файл", "cff файлов формат", "какво е cff файл", "файл", "cff пример", "cff файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - компактен файлов формат на шрифта",
  "description":"Научете за CFF файловия формат и API за създаване и отваряне на CFF файлове.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Какво е CFF файл?

Файл с разширение .cff е компактен шрифтов формат и е известен също като PostScript Type 1 или CIDFont. CFF действа като контейнер за съхраняване на множество шрифтове заедно в една единица, известна като FontSet. Дизайнът на CFF шрифтовете позволява вграждане на езиков код PostScript, който позволява допълнителна гъвкавост и разширяемост на формата за използване с принтерни среди. Файловете с CFF шрифтове могат да се отварят и конвертират с помощта на API като [Aspose.Font](https://products.aspose.com/font).

## CFF файлов формат

CFF файловете са двоични файлове, които съдържат оформление на структурирани данни, имат дефинирани типове данни, заглавка, организация на глифове и речници на таблици. Повече подробности за тях можете да намерите в [спецификациите на формата на компактния шрифт](https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### Оформление на данните
Оформлението на данните във файловия формат CFF е както е показано по-долу.

|Вписване|Коментари|
---|---|
|Заглавка|–|
|ИмеИНДЕКС|–|
|Нагоре DICT ИНДЕКС|–|
|ИНДЕКС на низ|–|
|Глобален подИНДЕКС|–|
|Кодировки–Набори на знаци|–|
|FDSelect|Само CIDFonts|
|CharStrings INDEX|на шрифт|
|Font DICT INDEX|за шрифт, само CIDFonts|
|Частен DICT|на шрифт|
|Local Subr INDEX|за шрифт или за частен DICT за CIDFonts|
|Бележки за авторски права и търговски марки|–|

### Типове данни

Типовете данни CFF са както е показано в следващата таблица.

|Име|Диапазон|Описание|
---|---|---|
|Card8|0 –255|1-байтов номер без знак|
|Card16|0 – 65535|2-байтов номер без знак|
|Отместване|варира|1, 2, 3 или 4 байта отместване (определено от полето OffSize)|
|OffSize|1–4|1-байтово число без знак указва размера на поле или полета за отместване|
|SID|0 – 64999|2-байтов идентификатор на низ|

### Заглавие

Двоичните данни започват със заглавка, имаща формата, показан в следващата таблица.

|Тип|Име|Описание|
---|---|---|
|Card8|major|Форматирайте основна версия (започваща от 1)|
|Card8|минор|Форматиране на второстепенна версия (започваща от 0)|
|Карта8|hdrSize| Размер на заглавието (байтове)|
|OffSize|offSize|Размер на абсолютното отместване (0)|

## Препратки

* [Таблица с компактни формати на шрифтове](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [Файлов формат CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 Chartset](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

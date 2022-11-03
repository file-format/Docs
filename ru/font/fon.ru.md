{
  "date" : "2020-08-20",
  "keywords" :[ "файл fon", "формат файла fon", "что такое файл fon", "файл", "пример fon", "расширение файла fon", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON — файл библиотеки шрифтов",
  "description":"Узнайте о формате файла FON и API-интерфейсах, которые могут создавать и открывать файлы FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## .FON вариант №

Файл с расширением .fon представляет собой библиотеку шрифтов Microsoft Windows 3.x, которая на самом деле является исполняемым файлом, но переименована в .fon. Это набор файлов [.fnt](/ru/font/fnt/) сам по себе, и приложения ссылаются на него при доступе к системному шрифту. Вот почему он действует как файл ресурсов. Его можно открыть в ОС Windows с помощью приложения Microsoft Windows Font View.

## FON Формат файла

Файл FON содержит ресурсы шрифтов и имеет формат файла ресурсов (.res). Формат файла .res определяет заголовок файла, а также спецификации раздела данных. .fnt также является файлом данных ресурсов, включенным в файл ресурсов. Файлы FON имеют двоичный формат и тип MIME application/octet-stream.

Ресурсы шрифтов, в отличие от других типов ресурсов, не добавляются к ресурсам приложения. Вместо этого они добавляются в файлы EXE и переименовываются в файлы .fon, в результате чего вместо приложений появляются файлы библиотек. Несколько отдельных шрифтов составляют компоненты группы шрифтов, где каждая группа следует структуре группы ресурсов. Ресурсы шрифтов используют эти структуры групп ресурсов. Заголовок группы содержит всю информацию, необходимую для доступа к определенному шрифту из группы. Ресурс компонента шрифта имеет следующий формат.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/ru/font/fnt/) file)
```
Один файл ресурсов .rc может иметь смешанные объявления ресурсов. Группы шрифтов могут находиться где угодно в файле ресурсов и не обязательно должны быть непрерывными. Для программ, создающих файлы .RES, необходимо добавить ручной ввод FONTDIR. Ниже приведена структура заголовка группы.

```
[Обычный заголовок ресурса (тип = 7)]

СЛОВО КоличествоШрифтов; // Общее количество в файле .RES
```     
The remaining data is repeated for every font in the .RES file.

```
СЛОВО шрифтOrdinal;
struct FontDirEntry {
СЛОВО dfВерсия;
Двойное слово dfSize;
char dfCopyright[60];
СЛОВО dfType;
СЛОВО dfPoints;
СЛОВО dfVertRes;
СЛОВО dfHorizRes;
СЛОВО dfAscent;
СЛОВО dfInternalLeading;
СЛОВО dfExternalLeading;
БАЙТ dfItalic;
БАЙТ dfUnderline;
БАЙТ dfStrikeOut;
СЛОВО dfWeight;
БАЙТ dfCharSet;
СЛОВО dfPixWidth;
СЛОВО dfPixHeight;
БАЙТ dfPitchAndFamily;
СЛОВО
СЛОВО dfMaxWidth;
БАЙТ dfFirstChar;
БАЙТ dfLastChar;
БАЙТ dfDefaultChar;
БАЙТ dfBreakChar;
СЛОВО dfWidthBytes;
DWORD dfDevice;
Двойное слово dfFace;
DWORD dfReserved;
char szDeviceName[];
символ szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)


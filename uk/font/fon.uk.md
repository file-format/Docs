{
  "date" : "2020-08-20",
  "keywords" :[ "файл fon", "формат файлу fon", "що таке файл fon", "файл", "приклад fon", "розширення файлу fon", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - файл бібліотеки шрифтів",
  "description":"Дізнайтеся про формат файлу FON та API, які можуть створювати та відкривати файли FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Що таке файл FON?

Файл із розширенням .fon — це бібліотека шрифтів Microsoft Windows 3.x, яка насправді є виконуваним файлом, але перейменована на .fon. Це набір файлів [.fnt](/uk/font/fnt/), і програми посилаються на нього під час доступу до системного шрифту. Ось чому він діє як файл ресурсу. Його можна відкрити в ОС Windows за допомогою програми Microsoft Windows Font View.

## Формат файлу FON

Файл FON містить ресурси шрифтів і має формат файлу Resource (.res). Формат файлу .res визначає заголовок файлу, а також специфікації розділу даних. .fnt також є файлом даних ресурсу, який включено до файлу ресурсу. Файли FON мають двійковий формат файлів і мають тип прикладного/октетного потоку MIME.

Ресурси шрифтів, на відміну від інших типів ресурсів, не додаються до ресурсів програми. Натомість вони додаються до файлів EXE і перейменовуються на файли .fon, у результаті чого замість програм отримують файли бібліотек. Кілька окремих шрифтів є компонентами групи шрифтів, де кожна група відповідає структурі групи ресурсів. Ресурси шрифтів використовують ці структури груп ресурсів. Заголовок групи містить усю інформацію, необхідну для доступу до певного шрифту з групи. Ресурс компонента шрифту має такий формат.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/uk/font/fnt/) file)
```
Один файл ресурсів .rc може мати змішані оголошення ресурсів. Групи шрифтів можуть бути будь-де у файлі ресурсів і не повинні бути суміжними. Програми, які створюють файли .RES, повинні додавати вручну FONTDIR. Нижче наведено структуру заголовка групи.

```
[Звичайний заголовок ресурсу (тип = 7)]

WORD NumberOfFonts; // Загальна кількість у файлі .RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
WORD dfVertRes;
WORD dfHorizRes;
WORD dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfкурсив;
BYTE dfUnderline;
BYTE dfStrikeOut;
WORD dfWeight;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
WORD dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD dfReserved;
char szDeviceName[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)


{
  "date" : "2020-08-20",
  "keywords" :[ "fon файл", "fon файлов формат", "какво е fon файл", "файл", "fon пример", "fon файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Файл с библиотека с шрифтове",
  "description":"Научете за файловия формат FON и API, които могат да създават и отварят FON файлове.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Какво е FON файл?

Файл с разширение .fon е библиотека с шрифтове на Microsoft Windows 3.x, която всъщност е изпълним файл, но преименуван на .fon. Това е колекция от [.fnt](/bg/font/fnt/) файлове сама по себе си и приложенията го препращат, докато осъществяват достъп до системния шрифт. Ето защо той действа като файл с ресурси. Може да се отвори на Windows OS с помощта на Microsoft Windows Font View приложение.

## Файлов формат FON

FON файл съдържа ресурси за шрифтове и има файлов формат Resource (.res). Файловият формат .res указва заглавката на файла, както и спецификациите на секцията с данни. .fnt също е файл с данни за ресурси, който е включен в файл с ресурси. FON файловете имат двоичен файлов формат и MIME тип приложение/октет-поток.

Ресурсите за шрифтове, за разлика от други видове ресурси, не се добавят към ресурсите на приложението. Вместо това те се добавят към EXE файловете и се преименуват на .fon файлове, което води до библиотечни файлове вместо приложения. Множество индивидуални шрифтове представляват компоненти на група шрифтове, където всяка група следва структура на група ресурси. Ресурсите за шрифтове използват тези групи ресурси. Заглавката на групата съдържа цялата информация, необходима за достъп до определен шрифт от групата. Ресурсът на компонент на шрифта има следния формат.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/bg/font/fnt/) file)
```
Един файл с ресурси .rc може да има смесени декларации за ресурси. Групите шрифтове могат да бъдат навсякъде във файла с ресурси и не е необходимо да са съседни. Задължително е програмите, създаващи .RES файлове, да добавят ръчно въвеждане на FONTDIR. Следва структурата на заглавката на групата.

```
[Нормално заглавие на ресурс (тип = 7)]

WORD NumberOfFonts; // Общ брой в .RES файл
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
ДУМА dfHorizRes;
WORD dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItalic;
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


{
  "date": "2020-08-20",
  "keywords": [
"fon faylı",
"fon fayl formatı",
"fon faylı nədir",
"fayl",
"fon nümunəsi",
"fon fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FON - Şrift Kitabxana Faylı",
  "description": "FON faylları yarada və aça bilən FON fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "FON",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fo-azn"
}
},
  "lastmod": "2020-10-30"
}

## FON faylı nədir?

.fon uzantılı fayl əslində icra edilə bilən fayl olan, lakin adı .fon olaraq dəyişdirilmiş Microsoft Windows 3.x şrift kitabxanasıdır. Bu, özlüyündə [.fnt](/font/fnt/) faylların toplusudur və proqramlar sistem şriftinə daxil olarkən ona istinad edir. Buna görə də o, resurs faylı kimi çıxış edir. Microsoft Windows Font View proqramından istifadə edərək Windows ƏS-də açıla bilər.

## FON fayl formatı

FON faylı şrift resurslarını ehtiva edir və Resurs (.res) fayl formatına malikdir. .res fayl formatı fayl başlığını və məlumat bölməsinin spesifikasiyalarını təyin edir. .fnt həm də resurs faylına daxil olan resurs məlumat faylıdır. FON faylları ikili fayl formatına malikdir və proqram/oktet axını MIME növünə malikdir.

Şrift resursları, digər növ resurslardan fərqli olaraq, tətbiqin resurslarına əlavə edilmir. Əvəzində onlar EXE fayllarına əlavə edilir və .fon faylları olaraq adlandırılır, nəticədə proqramlar əvəzinə kitabxana faylları yaranır. Çoxsaylı Fərdi şriftlər hər bir qrupun resurs qrupu strukturunu izlədiyi şrift qrupunun komponentlərini təşkil edir. Şrift resursları bu resurs qrup strukturlarından istifadə edir. Qrup başlığında qrupdan müəyyən bir şriftə daxil olmaq üçün tələb olunan bütün məlumatlar var. Şrift komponenti resursu aşağıdakı formata malikdir.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
Tək .rc resurs faylında qarışıq resurs bəyannamələri ola bilər. Şrift qrupları resurs faylının istənilən yerində ola bilər və bitişik olmamalıdır. .RES faylları yaradan proqramlar üçün FONTDIR-in əl ilə daxil edilməsini əlavə etmək lazımdır. Aşağıda qrup başlığının strukturu verilmişdir.

```
[Normal resurs başlığı (növ = 7)]

WORD NumberOfFonts; // .RES faylında ümumi sayı
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


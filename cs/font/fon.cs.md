{
  "date" : "2020-08-20",
  "keywords" :[ "soubor fon", "formát souboru fon", "co je soubor fon", "soubor", "příklad fon", "přípona souboru fon", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - soubor knihovny písem",
  "description":"Další informace o formátu souborů FON a rozhraních API, která mohou vytvářet a otevírat soubory FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Co je soubor FON?

Soubor s příponou .fon je knihovna písem Microsoft Windows 3.x, která je ve skutečnosti spustitelným souborem, ale je přejmenována na .fon. Je to sbírka souborů [.fnt](/cs/font/fnt/) sama o sobě a aplikace na něj odkazují při přístupu k systémovému písmu. Proto funguje jako zdrojový soubor. Lze jej otevřít v operačním systému Windows pomocí aplikace Microsoft Windows Font View.

## Formát souboru FON

Soubor FON obsahuje prostředky písem a má formát souboru Resource (.res). Formát souboru .res určuje záhlaví souboru a také specifikace datové části. FNT je také zdrojový datový soubor, který je součástí souboru prostředků. Soubory FON mají binární formát souboru a mají typ MIME aplikace/oktetový proud.

Prostředky písem, na rozdíl od jiných typů zdrojů, se nepřidávají do prostředků aplikace. Místo toho jsou přidány do souborů EXE a přejmenovány na soubory .fon, což vede k souborům knihovny namísto aplikací. Více jednotlivých písem tvoří součásti skupiny písem, kde každá skupina sleduje strukturu skupiny prostředků. Prostředky písem používají tyto struktury skupin prostředků. Záhlaví skupiny obsahuje všechny informace potřebné pro přístup ke konkrétnímu písmu ze skupiny. Prostředek součásti písma má následující formát.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/cs/font/fnt/) file)
```
Jeden zdrojový soubor .rc může mít smíšené deklarace prostředků. Skupiny písem mohou být kdekoli v souboru prostředků a nemusí být souvislé. Pro programy vytvářející soubory .RES je nutné přidat ruční zadání FONTDIR. Následuje struktura hlavičky skupiny.

```
[Normální záhlaví zdroje (typ = 7)]

WORD NumberOfFonts; // Celkový počet v souboru .RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinální;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
WORD dfVertRes;
WORD dfHorizRes;
SLOVO dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItalic;
BYTE dfPodtržení;
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


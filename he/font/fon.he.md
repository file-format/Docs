{
  "date" : "2020-08-20",
  "keywords" :[ "קובץ fon", "פורמט קובץ fon", "מהו קובץ fon", "קובץ", "דוגמה של fon", "סיומת קובץ fon", "סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - קובץ ספריית גופנים",
  "description":"למד על פורמט קובץ FON וממשקי API שיכולים ליצור ולפתוח קובצי FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## מהו קובץ FON?

קובץ עם סיומת .fon הוא ספריית גופנים של Microsoft Windows 3.x שהיא למעשה קובץ הפעלה אך שמה שונה ל-.fon. זהו אוסף של קבצי [.fnt](/he/font/fnt/) בפני עצמו ויישומים מפנים אליו תוך גישה לגופן המערכת. זו הסיבה שהוא פועל כקובץ משאבים. ניתן לפתוח אותו במערכת ההפעלה Windows באמצעות יישום Microsoft Windows Font View.

## פורמט קובץ FON

קובץ FON מכיל משאבי גופנים ויש לו פורמט קובץ Resource (.res). פורמט הקובץ .res מציין את כותרת הקובץ וכן את מפרטי מקטע הנתונים. .fnt הוא גם קובץ נתוני משאבים הכלול בקובץ משאבים. לקבצי FON יש פורמט קובץ בינארי ויש להם סוג MIME‏ של application/octet-stream.

משאבי גופנים, בניגוד לסוגים אחרים של משאבים, אינם מתווספים למשאבים של יישום. במקום זאת הם מתווספים לקבצי EXE ומשנים את שמם לקבצי .fon, וכתוצאה מכך נוצרים קבצי ספרייה במקום יישומים. גופנים בודדים מרובים מהווים רכיבים של קבוצת גופנים כאשר כל קבוצה עוקבת אחר מבנה קבוצת משאבים. משאבי גופנים משתמשים במבני קבוצות משאבים אלה. בכותרת הקבוצה יש את כל המידע שנדרש כדי לגשת לגופן ספציפי מהקבוצה. למשאב רכיב גופן יש את הפורמט הבא.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/he/font/fnt/) file)
```
לקובץ משאבים .rc בודד יכולים להיות הצהרות משאבים מעורבות. קבוצות גופנים יכולות להיות בכל מקום בקובץ המשאבים ואינן צריכות להיות צמודות. זה חובה עבור תוכניות היוצרות קבצי RES להוסיף הזנה ידנית של FONTDIR. להלן המבנה של כותרת הקבוצה.

```
[כותרת משאב רגילה (סוג = 7)]

WORD NumberOfFonts; // המספר הכולל בקובץ RES
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


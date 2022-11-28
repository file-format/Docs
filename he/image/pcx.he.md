{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ PCX - Paintbrush Bitmap Image File",
  "description":"למד על פורמט קובץ PCX וממשקי API שיכולים ליצור ולפתוח קובצי PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## מהו קובץ PCX?

קובץ PCX, קובץ Picture Exchange, הוא פורמט קובץ תמונת רסטר ששימש כפורמט קובץ מקורי עבור יישום PC Paintbrush. הוא פותח על ידי ZSoft Corporation, ארה"ב עבור פלטפורמות DOS ו-Windows ואומץ כפורמט קובץ ההדמיה הראשי לפני הגעתם של [BMP](/he/image/bmp/), [JPEG](/he/image/jpeg/) ו-[ PNG](/he/image/png/) פורמטים של קבצים. קבצי PCX קטנים יותר בגודלם מכיוון שהם נדחסים באמצעות קידוד RLE. הוא משמש בקובץ [DCX](/he/image/dcx/) מרובה עמודים המשמש בעיקר ליצירת קובצי פקס דיגיטליים.

## פורמט קובץ PCX

קבצי PCX נשמרים על דיסק בפורמט קובץ בינארי. מבנה הפורמט הפנימי של הקבצים עוקב אחר סדר בתים של אנדיאן קטן ויש לו את שלושת הסעיפים הבאים:

**`PCX Header`** - כותרת PCX היא באורך 128 בתים. הוא מכיל מזהה, מספר גרסה, ממדי תמונה, 16 צבעי לוח, מישורי צבע מספרים ועומק סיביות של כל מישור, וערך עבור שיטת הדחיסה.

כותרת PCX היא כפי שמוצג להלן עם הפניה מאנציקלופדיה של פורמטים של קבצים גרפיים (מהדורה שנייה).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`נתוני תמונה`** - נתוני תמונה של PCX מופיעים ממש אחרי הכותרת. נתוני התמונה עשויים להיות דחוסים בהתאם להגדרת השדה בכותרת. אחסון הנתונים בקובץ PCX תלוי במספר מישורי הצבע שצוינו. נתוני התמונה מאורגנים בשורות. במקרה של מספר מישורים, אלה מאוחסנים לפי מישור בתוך שורה בסידור רציף של נתונים אדומים, ירוקים וכחולים. דפוס זה חוזר על עצמו עבור כל שורה במישור.

## הפניות

* [PCX - מאת ויקיפדיה](https://en.wikipedia.org/wiki/PCX)


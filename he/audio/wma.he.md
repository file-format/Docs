{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "קובץ", "הרחבה", "פורמט", "פורמט קובץ החלפת שמע", "מוזיקה" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קבצי WMA וממשקי API שיכולים ליצור ולפתוח קובצי WMA.",
  "title" :"WMA - קובץ שמע של Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## מהו קובץ WMA?

קובץ עם סיומת .wma מייצג קובץ שמע שנשמר בפורמט Advanced Systems Format (ASF). ASF הוא הפורמט הקנייני של מיקרוסופט המכיל זרמי סיביות המקודדים על ידי Windows Media Audio 9. בנוסף לתוכן האודיו, קובץ WMA מכיל גם אובייקטים של מטא נתונים כגון כותרת, אלבום, אמן וז'אנר של הרצועה. קובצי WMA משמשים בעיקר להזרמה דרך האינטרנט בדומה לקבצי [.mp3](/he/audio/mp3/).

## פורמט קובץ WMA

קובץ WMA הוא פורמט קובץ בינארי והוא כלול בפורמט קובץ ASF. הוא מציין את הקידוד של מטא נתונים על הקובץ בדומה לתגיות ה-ID3 המשמשות את קבצי ה-MP3. ה-Codec WMA נמצא בשימוש על ידי מיקרוסופט בפורמט ה-Protected Interoperable File Format שלה (PIFF) מאז 2008. עם זאת, הוא לא הוכרז כ-Codec שמע סטנדרטי על ידי תקני התעשייה הקשורים כגון DECE UltraViolet ו-MPEG-DASH.

### נתונים ספציפיים לסוג WMA

המידע הספציפי לסוג עבור ה-codec של Windows Media Audio מאוחסן בפורמט הבא כחלק מהנתונים הספציפיים לסוג של אובייקט ה-stream Properties.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## הפניות

* [סקירה כללית של ASF - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


{
  "date" : "2022-02-16",
  "keywords" :[ "קובץ obb", "פורמט קובץ obb", "מהו קובץ obb", "קובץ", "דוגמה ל-obb", "סיומת קובץ obb","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ OBB - קובץ קוביות בינארי אטום של אנדרואיד",
  "description":"למד על פורמט קבצי OBB וממשקי API שיכולים ליצור ולפתוח קובצי OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## מהו קובץ OBB?

קובץ OBB הוא קובץ הרחבה שמכיל נתונים נוספים שמתווספים לקובץ Android [APK](/he/compression/apk/). חנות Google Play אינה מאפשרת להחזיק קובץ APK של Android בגודל של יותר מ-100 MB. אבל יישומים מסוימים עשויים לדרוש גרפיקה בחדות גבוהה, קבצי מדיה או נכסים גדולים אחרים להתארח בנוסף לקבצי ה-APK. זה המקום שבו נכנסים סוגי קבצי OBB. Google Play מאפשר לצרף קבצי הרחבה אלה כתוספת לקובץ ה-APK.

## פורמט קובץ OBB

קבצי OBB נשמרים כקבצים בינאריים יחד עם קבצי ה-APK. כאשר APK מלווה את קבצי ה-OBB, Google Play מארח את קבצי ההרחבה בשרת שלו ולא נגבית עלות נוספת מהמפתח. הקבצים הנוספים האלה מאוחסנים באחסון המשותף של המכשיר בכרטיס SD או במחיצה הניתנת להרכבה ב-USB כאשר האפליקציה יורדת להתקנה.

קבצי OBB מורידים ומותקנים עם ההורדה. אבל במקרים מסוימים, אלה מורידים להתקנה כאשר האפליקציה מופעלת בפעם הראשונה.

### גודל קובץ מקסימלי של OBB

חנות Google Play מאפשרת להעלות קובצי הרחבה של OBB בגודל של עד 2 GB. מומלץ להעלות קבצים בגודל גדול כקבצי [ZIP](/he/compression/zip/) דחוסים להעלאה יעילה דרך האינטרנט.

ניתן לארח קובצי הרחבה אלו כקובץ הרחבה ראשי **ראשי** עבור משאבים נוספים הנדרשים על ידי האפליקציה או כקובץ הרחבת תיקון אופציונלי המיועד לעדכונים קטנים לקובץ ההרחבה הראשי.

## הפניות

* [מפתחי אנדרואיד - קבצי הרחבה](https://developer.android.com/google/play/expansion-files)

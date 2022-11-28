{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ KEY וממשקי API שיכולים ליצור ולפתוח קובצי KEY.",
  "title" :"פורמט קובץ KEY - קובץ מפתח פרטי דואר משופר בפרטיות",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## מהו קובץ KEY?

קובץ KEY הוא החלק הפרטי של מנגנון אבטחה שנשמר בתקליטור בפורמט קובץ Mal (PEM) משופרת. הוא משמש לפענוח מידע המוחלף בין דפדפן אינטרנט לשרת האינטרנט המשרת את בקשות הגלישה. קובץ KEY מכיל מחרוזות מקודדות שאינן שימושיות לעין אנושית אך מהוות את המהות של הצפנה/פענוח חילופי מידע כחלק מתעודת SSL בשרתי אינטרנט. קבצי KEY נוצרים באופן אוטומטי ומותקנים בקצה הלקוח.

אתה יכול לפתוח קבצי **KEY** עם כל עורך טקסט כגון Microsoft Notepad (Windows), Apple TextEdit (Mac), או GitHub Atom (בפלטפורמות שונות). קבצי KEY דומים לפורמטים של [CRT](/he/web/crt/) ו-[CER](/he/web/cer/).

## פורמט קובץ KEY - מידע נוסף

קבצי KEY מאוחסנים בדיסק כקובצי טקסט רגיל, אך הם מחרוזות מקודדות שאינן ידידותיות לקריאה. למעשה, למשתמשים יש אפס הבנה של המחרוזות כאשר הם נפתחים בעורך טקסט. אישור המפתח הפרטי הוא סודי ואין לחלוק אותו עם אף אחד. התהליך המלא של אבטחת חילופי מידע דרך האינטרנט כולל:

* **מפתח ציבורי** - משמש להצפנת מידע המשתמש לצורך חילופי נתונים בין הדפדפן לשרתי האינטרנט
* **מפתח פרטי** - משמש לפענוח המידע כפי שהוא מתקבל על ידי שרת האינטרנט

אישורי ה-SSL, הידועים גם כאישורי X.509, הינם ייחודיים לכל אתר אינטרנט. קבצי מפתח באמצעות התחביר הבא:

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### דוגמה לקובץ KEY

להלן דוגמה לקובץ מפתח פרטי.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## הפניות

* [מפתחות ציבוריים, מפתחות פרטיים ואישורים](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)


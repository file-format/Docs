{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "קובץ crt", "פורמט קובץ crt", "סוג קובץ crt", "קובץ", "סוג", "מהו קובץ crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - פורמט קובץ תעודת אבטחה",
  "description":"למד על פורמט קובץ CRT וממשקי API שיכולים ליצור ולפתוח קובצי CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ CRT?

קובץ עם סיומת .crt הוא קובץ תעודת אבטחה המשמש אתרים מאובטחים ליצירת חיבורים מאובטחים משרת אינטרנט לדפדפן. אתרים מאובטחים מאפשרים לאבטח העברות נתונים, התחברות, עסקאות בכרטיסי תשלום, ולספק גלישה מוגנת לאתר. אם אתה פותח אתר מאובטח, אתה רואה סמל "נעילה" בשורת הכתובת. אם תלחץ עליו, תוכל לראות את פרטי התעודה המותקנת. חברות בינלאומיות כמו Verisign ו-Thawte מפיצות את תעודות SSL אלו.

## פורמט קובץ CRT

קובצי CRT הם בפורמט ASCII וניתן לפתוח אותם בכל עורך טקסט כדי להציג את תוכן קובץ האישור. הוא עוקב אחר תקן ההסמכה X.509 המגדיר את מבנה התעודה. הוא מגדיר את שדות הנתונים שיש לכלול בתעודת SSL. CRT שייך לפורמט PEM של אישורים שהם קבצים מקודדים Base64 ASCII.

### מבנה קובץ PEM

לקובץ PEM יכול להיות מספר תעודות. במקרה כזה, כל תעודה בקובץ PEM עוקבת אחר המבנה הבא.

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

### דוגמה לפורמט קובץ CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## הפניות ##

* [מפתחות ציבוריים, מפתחות פרטיים ואישורים](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)


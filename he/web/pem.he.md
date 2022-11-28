{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ PEM - פורמט קובץ אישור דואר משופר בפרטיות",
  "description":"למד על פורמט קובץ PEM וממשקי API שיכולים ליצור ולפתוח קובצי PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## מהו קובץ PEM?

קובץ PEM הוא קובץ תעודת אבטחה המשמש ליצירת ערוץ תקשורת מאובטח בין שרת אינטרנט לדפדפן. הוא מקודד Base64 ויכול להכיל מפתח פרטי, אישור שרת ו/או שילוב של אישורים אחרים. קובצי PEM דומים לקובצי תעודת .der מבחינת השימוש אך מאוחסנים כטקסט מקודד Base64 ולא כנתונים בינאריים. פורמטים דומים אחרים של קבצי אישור כוללים קבצי [.cer](/he/web/cer/) ו-[.crt](/he/web/crt/).

יישומים שיכולים **לפתוח קובצי PEM** כוללים עורכי טקסט כגון Microsoft Notepad ו-Apple TextEdit.

## פורמט קובץ PEM

PEM הוא פורמט קובץ מיכל המגדיר את המבנה וסוג הקידוד של הקובץ המשמש לאחסון הנתונים. קובצי PEM מאוחסנים בדיסק כפורמט קובץ מקודד Base64 שאינו קריא לאדם. התקן מגדיר שקובץ PEM מתחיל ב:

```
-----BEGIN <type>-----
```
ומסתיים ב:
```
-----END <type>-----
```

כל שאר התוכן שבתוך אלה מקודד base64 (אותיות גדולות וקטנות, ספרות, + ו-/). קובץ PEM יחיד יכול להכיל מספר בלוקים שבהם ניתן להשתמש בתוכניות אחרות. אם קובץ PEM מכיל אישורים מרובים, כל אישור מופרד על ידי בלוקים בודדים כדלקמן:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### דוגמה לקובץ PEM

קובץ PEM עם בלוק CERTIFICATE נראה בדרך כלל כך:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

קובץ PEM עם RSA מתחיל כמו הבא.

```
-----BEGIN RSA PRIVATE KEY-----
```

## הפניות ##

* [קריפטוגרפיה של מפתח ציבורי](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [כיצד ליצור קובץ P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


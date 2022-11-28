{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - קובץ אישורים PKCS 7",
  "description":"למד על פורמט קובץ P7C וממשקי API שיכולים ליצור ולפתוח קבצי P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ P7C?

קובץ P7C, כמו קבצי אישורי אבטחה אחרים, הוא אישור דיגיטלי המשמש לאימות זהות דרך הרשת. יישומים המשתמשים באישורים מאמתים זהות באמצעות המפתח הציבורי הכלול בקובצי האישורים הללו. קריפטוגרפיה של מפתח ציבורי, או קריפטוגרפיה א-סימטרית, משתמשת בזוג מפתחות שאחד מהם הוא המפתח הציבורי והשני מכונה מפתח פרטי. המפתח הפרטי נשמר מאובטח לאבטחה יעילה, בעוד המפתח הציבורי ניתן לשיתוף עם אחרים. פורמטים נפוצים אחרים של קבצי אישור כוללים [CRT](/he/web/crt/), DER ו-PEM.

## פורמט קובץ P7C - מידע נוסף

קבצי P7C נשמרים בדיסק כקבצים בינאריים וכוללים את מידע המפתח הציבורי שנוצר באמצעות אלגוריתמים קריפטוגרפיים המבוססים על בעיות מתמטיות. ניתן לפתוח אותם בכל עורך טקסט אך התוכן שלהם אינו בצורה קריא אנושית. חלק מהיישומים שיכולים לפתוח קבצי P7C כוללים Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager ו-Microsoft Windows Contacts.

### דוגמה לפורמט קובץ P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## הפניות ##

* [קריפטוגרפיה של מפתח ציבורי](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [כיצד ליצור קובץ P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


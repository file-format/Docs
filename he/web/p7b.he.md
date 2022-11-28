{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - קובץ אישורים PKCS 7",
  "description":"למד על פורמט קובץ P7C וממשקי API שיכולים ליצור ולפתוח קבצי P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ P7B?

קובץ P7B הוא קובץ תעודת אבטחה המכיל אישור דיגיטלי מאובטח לאימות אדם או מכשיר. בדומה לקובץ אישור [.cer](/he/web/cer/), ניתן להתקין קובץ P7B באמצעות האפשרות "התקן אישור" על ידי שימוש באפשרות לחיצה ימנית על הקובץ. P7B משתמש באפשרות עיצוב שונה מפורמט הקובץ CER. הוא מכיל אחד או יותר קבצי אישור דיגיטלי X.509 המשתמשים בקידוד base64 (ASCII). קובצי P7B מתקבלים כקובץ [ZIP](/he/compression/zip/) או מתקבלים מרשות האישורים.

## פורמט קובץ P7B

קבצי P7B מאוחסנים כקבצי ASCII רגילים שניתן לפתוח בכל עורך טקסט. הוא מכיל את המפתח הציבורי שהוא מחרוזת מקודדת שאין לה משמעות מנקודת מבט של קריאות.

### דוגמה לפורמט קובץ P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## הפניות ##

* [קריפטוגרפיה של מפתח ציבורי](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [כיצד ליצור קובץ P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ CSR - פורמט קובץ בקשת חתימה על אישור",
  "description" :"למד על מהו קובץ CSR וממשקי API שיכולים ליצור ולפתוח קובצי CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## מהו קובץ CSR?

קובץ CSR הוא קובץ **בקשת חתימת אישור** המשמש לבקשת אישור SSL/TLS. כאשר אתה צריך לקבל את אישור ה-SSL/TLS שלך, אתה יוצר את ה-CSR באותו שרת שבו הוא יותקן לבסוף. קובץ CSR זה משותף עם רשות האישורים (CA) ליצירת האישור. הוא מכיל מידע כגון שם נפוץ, ארגון, מדינה, וחשוב מכך, **המפתח הציבורי** המשולב בקובץ התעודה שלך וחתום במפתח הפרטי המתאים.

יישומים שיכולים **לפתוח קבצי CSR** כוללים OpenSSL ו-Microsoft IIS.

## פורמט קובץ בקשה לחתימה על אישור

קובץ CSR נוצר בפורמט Base-64 PEM שניתן לפתוח ולהציג בעורך טקסט פשוט כמו Microsoft Notepad. הוא כולל כותרת עליונה **-----BEGIN NEW CERTIFICAT REQUEST-----** בתחילת הקובץ וכותרת תחתונה **-----END NEW CERTIFICAT REQUEST-----** ב- סוף הקובץ.

### איך נראה קובץ CSR?

דוגמה פשוטה לקובץ CSR היא כדלקמן.

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## איזה מידע כלול ב-CSR?

קובץ CSR מכיל את המידע הבא.

1. `מידע על עסקים ואתר` - כולל מידע כגון שם משותף, ארגון, יחידה ארגונית, עיר/יישוב, מדינה/מחוז/אזור (S), מדינה וכתובת דוא"ל
1. `מפתח ציבורי` - הוא כלול בתעודה ומשמש להצפנת נתונים משודרים המפוענחים באמצעות המפתח הפרטי המתאים
1. `מידע על סוג מפתח ואורך` - זה בדרך כלל RSA 2048 אך עשוי להגיע גם בגדלים גדולים יותר כגון RSA 4096+

## הפניות

* [שרת יישומים קונספט](https://github.com/Devronium/ConceptApplicationServer)


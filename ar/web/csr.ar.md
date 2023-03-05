{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف CSR - تنسيق ملف طلب توقيع الشهادة" ,
  "description" :"تعرف على ما هو ملف CSR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CSR وفتحها." ,
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
} ,
  "lastmod" : "2022-09-04"
}

## ما هو ملف CSR؟

ملف CSR هو ملف ** طلب توقيع الشهادة ** يُستخدم لطلب شهادة SSL / TLS. عندما تحتاج إلى الحصول على شهادة SSL / TLS الخاصة بك ، فإنك تنشئ CSR على نفس الخادم حيث سيتم تثبيته أخيرًا. تتم مشاركة ملف CSR هذا مع المرجع المصدق (CA) لإنشاء الشهادة. يحتوي على معلومات مثل الاسم الشائع والمنظمة والبلد ، والأهم من ذلك ، ** المفتاح العام ** المدمج في ملف الشهادة والموقع بالمفتاح الخاص المقابل.

تتضمن التطبيقات التي يمكنها ** فتح ملفات CSR ** OpenSSL و Microsoft IIS.

## تنسيق ملف طلب توقيع الشهادة

يتم إنشاء ملف CSR بتنسيق Base-64 PEM الذي يمكن فتحه وعرضه في محرر نصوص بسيط مثل Microsoft Notepad. يشتمل على رأس ** ----- BEGIN NEW CERTIFICATE REQUEST ----- ** في بداية الملف وتذييل الصفحة ** ----- نهاية طلب الشهادة الجديد ----- ** في نهاية الملف.

### كيف يبدو ملف CSR؟

مثال بسيط لملف CSR هو على النحو التالي.

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

## ما هي المعلومات المدرجة في CSR؟

يحتوي ملف CSR على المعلومات التالية.

1. "معلومات حول النشاط التجاري وموقع الويب" - تتضمن معلومات مثل الاسم الشائع والمؤسسة والوحدة التنظيمية والمدينة / المنطقة والولاية / المقاطعة / المنطقة (المناطق) والبلد وعنوان البريد الإلكتروني
1. "المفتاح العام" - يتم تضمينه في الشهادة ويستخدم لتشفير البيانات المرسلة التي يتم فك تشفيرها باستخدام المفتاح الخاص المقابل
1. "معلومات حول نوع المفتاح وطوله" - عادةً ما تكون RSA 2048 ولكنها قد تأتي أيضًا بأحجام أكبر مثل RSA 4096+

## مراجع

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)


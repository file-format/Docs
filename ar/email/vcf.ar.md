{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - ملف جهات الاتصال الظاهري" ,
  "description":"تعرف على تنسيق ملف VCF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات VCF وفتحها." ,
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف VCF؟

VCF (تنسيق البطاقة الافتراضية) أو vCard هو تنسيق ملف رقمي لتخزين معلومات جهات الاتصال. يستخدم التنسيق على نطاق واسع لتبادل البيانات بين تطبيقات تبادل المعلومات الشائعة. تأتي معظم أنظمة التشغيل مثل Windows و MacOS مع تطبيقات افتراضية لإنشاء هذه الملفات وفتحها. يمكن أن يحتوي ملف VCF واحد على معلومات الاتصال لواحد أو عدة جهات اتصال. يحتوي ملف VCF عادةً على معلومات مثل اسم جهة الاتصال والعنوان ورقم الهاتف والبريد الإلكتروني وتاريخ الميلاد والصور والصوت بالإضافة إلى عدد من الحقول الأخرى. كونها مدعومة من قبل عملاء وخدمات البريد الإلكتروني ، لا يوجد فقدان للبيانات أثناء نقل جهات الاتصال عبر استخدام تنسيق vCard. نوع الوسائط لتنسيق ملف VCF هو text / vcard.

## تنسيق ملف VCF

ملفات VCF نصية بطبيعتها ويمكن للبشر قراءتها. يمكن فتحها في برامج تحرير النصوص مثل Notepad على Microsoft Windows و TextEdit على نظام MacOS. إذا كانت هناك صورة في الملف ، فلن تظهر في محرر النصوص.

يوفر [Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) دعمًا لـ فتح ملفات VCF وكذلك التحويل إلى عدد من التنسيقات الأخرى مثل تنسيق [MSG](/ar/email/msg/) الشائع . تم تحسين تنسيق ملف VCF بمرور الوقت من الإصدار 2.1 إلى 4.0 مضيفًا معلومات مفصلة إلى تنسيق الملف. يستخدم التنسيق أيضًا لتصدير جهات اتصال الهاتف والاستيراد لاحقًا في جهاز آخر.

{{< figure src="../VCF.png" alt="تنسيق ملف VCF" >}}

### VCF 2.1 مثال

فيما يلي مثال على الإصدار 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### VCF 3.0 مثال

فيما يلي مثال على الإصدار 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### VCF 4.0 مثال

فيما يلي مثال على الإصدار 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## مراجع

* [VCF - بواسطة Wikipedia](https://en.wikipedia.org/wiki/VCard)


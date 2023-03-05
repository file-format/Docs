{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - تنسيق ملف Apple Mail" ,
  "description":"تعرف على تنسيق ملف EMLX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات EMLX وفتحها." ,
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف EMLX؟

يتم تنفيذ وتطوير تنسيق ملف EMLX بواسطة Apple. يستخدم تطبيق Apple Mail تنسيق ملف EMLX لتصدير رسائل البريد الإلكتروني. هناك أيضًا تطبيقات أخرى يمكنها فتح ملفات EMLX وتحويلها إلى تنسيقات ملفات أخرى.

## تاريخ موجز لتنسيق ملف EMLX

اعتمد نظام التشغيل Mac OS X برنامج البريد الإلكتروني الحالي ، NeXTMail ، الذي أنشأته NeXT كجزء من نظام التشغيل NeXTSTEP. قامت Apple بعد الاستحواذ على NeXT بترقية ميزاتها وأصبحت الآن تطبيق بريد Apple Mail ليتم استخدامه كعميل بريد افتراضي. يتم حفظ رسائل البريد الإلكتروني المصدرة عبر Apple Mail مباشرة كملفات EMLX. بالإضافة إلى ذلك ، فهو عميل البريد الافتراضي لملفات EMLX عندما يفتحها شخص ما عن طريق النقر المزدوج على نظام التشغيل Mac OS.

## تنسيق ملف EMLX

ملفات EMLx عبارة عن ملفات نصية بسيطة يمكن فتحها في أي محرر نصوص مثل Notepad. يتكون هيكل ملف EMLX من ثلاثة أجزاء:

* عدد البايت للرسالة - طول الرسالة نفسها ، المكتوبة بـ ASCII بالنظام العشري ، منتهية بـ 0x0a
* الرسالة نفسها
* البيانات الوصفية للرسالة في شكل XML plist

يمكن شرح ذلك بشكل أفضل بمساعدة اتباع نموذج البريد الإلكتروني المستخرج من Apple Mail كـ EMLX وفتحه في محرر نصوص.

### مثال على EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

في هذا المثال ، يُظهر الرقم 875 إجمالي طول الرسالة. يتم تضمين البيانات الوصفية للرسالة في ملف<plist> العلامات والأعلام كما يلي:

| الحقل | الوصف | القيمة
---|---|---|
| 0 | قراءة | 1 << 0
| 1 | محذوف | 1 << 1
| 2 | مجاب | 1 << 2
| 3 | مشفر | 1 << 3
| 4 | تم وضع علامة عليه | 1 << 4
| 5 | حديث | 1 << 5
| 6 | مسودة | 1 << 6
| 7 | أولي (لم يعد مستخدمًا) | 1 << 7
| 8 | مُعاد توجيهه | 1 << 8
| 9 | تمت إعادة توجيهه | 1 << 9
| 10-15 | عدد المرفقات | 3 فهرنهايت << 10 (6 بت)
| 16-22 | مستوى الأولوية | 7 درجة فهرنهايت << 16 (7 بت)
| 23 | موقّع | 1 << 23
| 24 | خردة | 1 << 24
| 25 | ليس خردة | 1 << 25
| 26-28 | حجم الخط دلتا | 7 << 26 (3 بت)
| 29 | مستوى البريد غير الهام المسجل | 1 << 29
| 30 | تمييز النص في toc | 1 << 30
| 31 | (غير مستخدم) |

## أنظر أيضا ##

* [EML](/ar/ email / eml /)
* [MSG](/ar/ email / msg /)


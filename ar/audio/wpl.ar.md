{
  "date" : "2021-06-11",
  "keywords" :["wpl" , "ملف wpl" , "امتداد" , "تنسيق" , "ما هو ملف wpl" , "موسيقى" , "تنسيق ملف wpl"] ,
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف WPL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات WPL وتحويلها وفتحها." ,
  "title" :"WPL - ملف قائمة تشغيل Windows Media Player" ,
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
} ,
  "lastmod" : "2021-06-11"
}

## ما هو ملف WPL؟

يحتوي ملف بامتداد .wpl على قائمة تشغيل الأغاني التي سيتم تشغيلها على Microsoft Windows Media Player. عادةً ما يتم إنشاء هذه الملفات بواسطة المستخدمين لمجموعات الفيديو والصوت الخاصة بهم. المحتوى المكتوب في ملف WPL هو مجرد مسارات أو مواقع لملفات الوسائط المتعددة المحددة من قبل منشئ ملف .wpl ، لذلك يمكن لتطبيق مشغل الوسائط العثور على محتوى الوسائط المتعددة وتشغيله على الفور من مواقع الدليل الخاصة بهم.

## تنسيق ملف WPL

WPL (قائمة تشغيل Windows Media Player) هو تنسيق ملف خاص يستخدم في إصدارات Microsoft Windows Media Player 9 أو ما بعده. هو تنسيق ملف كمبيوتر يخزن قوائم تشغيل الوسائط المتعددة. بشكل افتراضي ، يتم حفظ قائمة التشغيل بامتداد .wpl (قائمة تشغيل Windows Media Player). يمكنك استخدام الامتداد [.m3u](/ar/ audio / m3u) بدلاً من ذلك ، إذا كنت تريد تشغيل أقراص البيانات في جهاز لا يدعم هذا الامتداد. يتم تمثيل عناصر ملف WPL بتنسيق XML.

يحدد عنصر المستوى الأعلى "smil" أن عناصر الملف تتبع بنية لغة تكامل الوسائط المتعددة المتزامنة (SMIL). يتم إنشاء الملف وحفظه بامتداد .wpl ونوع MIME الخاص به هو application / vnd.ms-wpl.

### مثال على WPL

فيما يلي مثال على ملف wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## مراجع ##

* [MPEG-1 Audio Layer II - By Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


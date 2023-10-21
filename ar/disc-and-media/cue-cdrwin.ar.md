{
   "date":"2023-10-18",
   "keywords":[
      "cue",
      "cue file",
      "cue cdrwin cue sheet file",
      "how to open a cue file",
      "file",
      "cue file extension",
      "extension",
      "file"
   ],
   "author":{
      "display_name":"Shakeel Faiz"
   },
   "draft":"false",
   "toc":true,
   "title":"CUE File Format - CDRWIN Cue Sheet",
   "description":"تعرف على تنسيق ملف CUE CDRWIN Cue Sheet وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CUE وفتحها.",
   "linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
         "parent":"disc-and-media"
      }
   },
   "lastmod":"2023-10-18"
}

## ما هو ملف CUE؟

الملف **.CUE**، المعروف أيضًا باسم **CDRWIN Cue Sheet**، هو ملف نصي عادي يحتوي على معلومات حول مسارات وتخطيط قرص صوتي مضغوط أو صورة قرص، عادةً بتنسيق BIN أو ISO . تُستخدم هذه الملفات غالبًا لوصف بنية القرص ومحتوياته، مما يسمح لبرنامج النسخ على الأقراص المضغوطة أو برنامج محرك الأقراص الظاهري بإعادة إنتاج القرص الأصلي بدقة.

## مثال لملف CUE

فيما يلي مثال لما قد يبدو عليه ملف ".cue":

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## ورقة جديلة CDRWIN

تعد CDRWIN Cue Sheet شكلاً محددًا لتنسيق الملف ".cue" الذي يستخدمه برنامج CDRWIN. CDRWIN هو برنامج لنسخ وتأليف أقراص CD/DVD، وقد تم تصميم أوراق ".cue" الخاصة به للاستخدام مع هذا البرنامج. تحتوي أوراق ".cue" هذه على معلومات ضرورية لـ CDRWIN لإنشاء قرص مضغوط أو قرص DVD أو نسخه بدقة.

فيما يلي بعض التفاصيل الأساسية الخاصة بأوراق CDRWIN Cue:

1. **فريد لـ CDRWIN**: أوراق CDRWIN ".cue" هي تنسيق خاص خاص ببرنامج CDRWIN. على الرغم من أنها تشترك في أوجه التشابه مع ملفات ".cue" القياسية، إلا أنها مصممة للعمل مع ميزات وإعدادات CDRWIN.
    
2. **واجهة سهلة الاستخدام**: يوفر CDRWIN واجهة سهلة الاستخدام لإنشاء أوراق ".cue" وتحريرها. يمكن للمستخدمين إضافة أو تعديل المعلومات حول المسارات والفهارس والفجوات والمعلمات الأخرى بطريقة سهلة الاستخدام.
    
3. **أنواع الأقراص المتوافقة**: تُستخدم أوراق CDRWIN Cue بشكل أساسي لإنشاء أنواع مختلفة من الأقراص المضغوطة وأقراص DVD، بما في ذلك أقراص البيانات، والأقراص المضغوطة الصوتية، والأقراص ذات الأوضاع المختلطة، والمزيد. يتيح التنسيق للمستخدمين تحديد نوع ومحتوى القرص الذي يرغبون في إنشائه.
    
4. **التحكم في تخطيط القرص**: توفر أوراق CDRWIN Cue تحكمًا تفصيليًا في تخطيط القرص وبنيته، بما في ذلك ترتيب المسار وإعدادات الإيقاف المؤقت/الفجوة وأي تفضيلات محددة أخرى قد تكون لدى المستخدم.
    
5. **دعم ISO وBIN**: يمكن لـ CDRWIN العمل مع تنسيقات صور الأقراص ISO وBIN. تحدد ورقة ".cue" ملف الصورة الذي سيتم استخدامه للقرص، مما يضمن التزامن المناسب بين الإشارات والصورة.
    
6. **النسخ والنسخ**: تعد أوراق ".cue" هذه ضرورية عند نسخ الأقراص أو نسخ المسارات من الأقراص باستخدام CDRWIN. فهي تساعد على ضمان تطابق المنتج النهائي مع التصميم والمحتوى المقصودين.
    
7. **النسخ الاحتياطي والاستعادة**: غالبًا ما يقوم مستخدمو CDRWIN بإنشاء أوراق ".cue" عند عمل نسخ احتياطية للأقراص المضغوطة أو أقراص DVD الخاصة بهم. يمكن استخدام هذه الأوراق لاحقًا لاستعادة محتوى القرص، بما في ذلك تخطيط المسار والتوقيت.

## كيفية فتح ملف CUE؟

تم تصميم أوراق CDRWIN Cue Sheets خصيصًا لبرنامج CDRWIN، لذلك من المفترض عادةً أن يتم فتحها واستخدامها داخل CDRWIN.

البرامج التي تفتح ملفات CUE أو تشير إليها

- CDRWIN
- Smart Projects IsoBuster
- EZB Systems UltraISO

## ملفات CUE أخرى

فيما يلي أنواع الملفات الأخرى التي تستخدم امتداد الملف **.cue**.

**Disk and Media**
- [CUE - Cue Sheet File](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## مراجع
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)
{
  "date" : "2021-06-09",
  "keywords" :["cue", "file", "extension", "format", "what is a cue file", "music", "cue file format", "cue file format specification", "cue sheet", "CDRWIN" ] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف CUE وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CUE وتحويلها وفتحها." ,
  "title" :"CUE - ملف Cue Sheet" ,
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
} ,
  "lastmod" : "2021-07-01"
}

## ما هو ملف كيو؟

الملف ذو الامتداد .cue ، المعروف أيضًا باسم ملف cue sheet ، هو ملف بيانات أولية يحتوي على معلومات حول تخطيط المسارات على قرص مضغوط أو قرص DVD. يتم دعمها بواسطة مشغلات الوسائط وتطبيقات تأليف الأقراص الضوئية. تتم الإشارة إلى بيانات الصوت الرئيسية المخزنة على القرص المضغوط بواسطة ملف جديلة ، جنبًا إلى جنب مع مواصفات أطوال المسارات وعناوين الأسطوانات وفناني الأداء. وبالتالي ، إذا كان ملف صوتي واحد يحتوي على مسارات متعددة ، فيمكن استخدام ملف cue لتقسيم الصوت إلى ملفات متعددة أو الرجوع إلى مسارات مختلفة.

## تنسيق ملف كيو

يتم تخزين ملفات CUE أو ملفات cue في تنسيق نص عادي يمكن قراءته من قبل الإنسان. المعلومات الموجودة في ملف جديلة هي أوامر ذات معلمة واحدة أو أكثر. تنطبق هذه الأوامر إما على الملف بأكمله أو على مسار فردي ، اعتمادًا على أمر معين والسياق. يصف دليل المستخدم CDRWIN المواصفات الخاصة بصيغة ورقة التلميح ودلالاتها.

## أوامر ورقة CUE الأساسية

| الأمر | الوصف |
---|---|
| ملف | يشير إلى الملف الذي يحتوي على البيانات وتنسيقها مثل [MP3](/ar/audio/mp3/) ، [WAV](/ar/audio/wav/) ، أو صورة قرص ثنائي عادي) |
| المسار | يحدد معلومات سياق المسار مثل رقمه ونوعه أو وضعه. |
| الفهرس | يمثل الموقف كمؤشر داخل FILE. التنسيق mm: ss: ff (إطار الدقيقة الثانية). |
| PREGAP و POSTGAP | يشير هذا إلى pregap أو ما بعد الفجوة للمسار ، والذي لا يتم تخزينه في أي ملف بيانات. تم تحديد الطول في نفس تنسيق الإطار بالدقائق الثانية مثل INDEX. |

### مثال على ورقة CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## مراجع

* [ملف .cda - بواسطة ويكيبيديا](https://en.wikipedia.org/wiki/.cda_file)


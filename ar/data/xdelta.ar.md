{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ملف XDELTA - ملف xdelta التفاضلي - ما هو ملف .xdelta وكيفية فتحه؟",
  "description" : "ملف XDELTA - ملف xdelta التفاضلي - ما هو ملف .xdelta وكيفية فتحه؟",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## ما هو ملف XDELTA؟

يحتفظ تنسيق ملف XDELTA بالاختلافات الثنائية بين ملفين آخرين ويتم إنشاؤه بواسطة أداة xdelta، وهي أداة مساعدة لسطر الأوامر لترميز دلتا، والتي تتضمن حساب الاختلافات بين ملفين وترميز تلك الاختلافات بتنسيق مضغوط. تقوم ملفات XDELTA بتخزين البيانات الثنائية التي تمثل التغييرات أو الاختلافات بين الملف الأصلي والملف المحدث. تمثل البيانات الثنائية في ملف XDELTA التغييرات اللازمة لتحويل ملف واحد (الأصلي) إلى ملف آخر (الإصدار المحدث أو المصحح).

تُستخدم ملفات XDELTA بشكل متكرر في مجتمع الألعاب لتوزيع التعديلات (التعديلات) لألعاب الفيديو. يمكن أن تتضمن هذه التعديلات أي شيء بدءًا من التغييرات التجميلية وحتى التعديلات المهمة في آليات اللعب. تسمح ملفات XDELTA للمستخدمين بتطبيق هذه التعديلات على عمليات تثبيت الألعاب الخاصة بهم عن طريق تصحيح ملفات اللعبة الأصلية بالتغييرات المحددة في ملف XDELTA.

## xdelta

`xdelta` هي أداة مساعدة لسطر الأوامر تستخدم لتشفير وفك تشفير دلتا؛ يتم استخدامه بشكل أساسي لإنشاء وتطبيق تصحيحات ثنائية، تسمى غالبًا تصحيحات دلتا أو تصحيحات xdelta، بين ملفين؛ تمثل هذه التصحيحات الاختلافات بين الملف الأصلي والإصدار المعدل أو المحدث، مما يسمح بالتوزيع الفعال للتحديثات، خاصة في السيناريوهات التي يكون فيها النطاق الترددي أو مساحة التخزين محدودة.

فيما يلي نظرة عامة مختصرة على الوظائف الرئيسية لـ `xdelta`:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

يُستخدم xdelta بشكل شائع في سيناريوهات مختلفة، مثل توزيع تحديثات البرامج وتصحيح ألعاب الفيديو وتحديث ملفات النظام في الأجهزة المدمجة أو أجهزة الشبكة. فهو يوفر طريقة مرنة وفعالة لإدارة تحديثات الملفات مع تقليل استخدام النطاق الترددي ومتطلبات التخزين.

## com.xdeltaui

xdeltaui هو تطبيق واجهة مستخدم رسومية (GUI) لإدارة وتطبيق تصحيحات XDELTA. يوفر xdelta gui واجهة سهلة الاستخدام للمستخدمين للتفاعل مع ملفات XDELTA وتطبيقها على الملفات الأصلية المقابلة، وتصحيحها أو تحديثها بشكل فعال.

على عكس إصدار سطر الأوامر من xdelta، الذي يعمل من خلال الأوامر المستندة إلى النص، يوفر xdeltaui طريقة أكثر سهولة للتعامل مع ملفات XDELTA، خاصة للمستخدمين الذين ليسوا على دراية بواجهات سطر الأوامر أو يفضلون الأدوات الرسومية.

باستخدام xdeltaui، يمكن للمستخدمين عادةً تنفيذ مهام مثل تحديد الملف الأصلي واختيار ملف تصحيح XDELTA وتطبيق التصحيح لإنشاء ملف محدث. يمكن أن يكون هذا مفيدًا بشكل خاص لتثبيت التعديلات أو التحديثات لألعاب الفيديو أو تطبيقات البرامج الأخرى.

## تحميل xdelta

في أنظمة Linux، يمكنك استخدام مديري الحزم مثل `apt` أو `yum` أو `dnf` لتثبيت xdelta. على سبيل المثال، على Ubuntu، يمكنك استخدام الأمر التالي:

```
sudo apt-get install xdelta3
```

## كيفية استخدام اكس دلتا

لاستخدام `xdelta`، يتعين عليك عادةً اتباع الخطوات العامة التالية:

1.  **التنزيل والتثبيت**: أولاً، تأكد من تثبيت xdelta على نظامك. يمكنك تنزيله من موقعه الرسمي أو من مديري الحزم أو من مصادر أخرى موثوقة.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **إنشاء التصحيح**:
    
- افتح واجهة سطر الأوامر (المحطة الطرفية أو موجه الأوامر).
- استخدم الأمر `xdelta` مع الخيارات المناسبة لإنشاء التصحيح. بناء الجملة الأساسي هو:
               
```
دلتا xdelta<original_file><updated_file><patch_output_file>
```
        
استبدال `<original_file> `مع المسار إلى الملف الأصلي، `<updated_file> `مع المسار إلى الملف المحدث، و`<patch_output_file> `بالاسم المطلوب لملف التصحيح.
- مثال:
               
```
xdelta delta original_file Update_file patch.xdelta
```
        
4.  **تطبيق التصحيح**:
    
- تأكد من توفر الملف الأصلي وملف التصحيح.
- افتح واجهة سطر الأوامر الخاصة بك.
- استخدم الأمر `xdelta` مع الخيارات المناسبة لتطبيق التصحيح. بناء الجملة الأساسي هو:
        
      
```
تصحيح xdelta<original_file><patch_file><output_file>
```
        
استبدال `<original_file> `مع المسار إلى الملف الأصلي، `<patch_file> `مع المسار إلى ملف التصحيح، و`<output_file> `بالاسم المطلوب لملف الإخراج.
- مثال:
                
```
تصحيح xdelta original_file patch.xdelta Update_file
```
        
5.  **عرض المساعدة**: إذا كنت بحاجة إلى مساعدة بشأن خيارات أو أوامر محددة، فيمكنك استخدام أمر `xdelta` مع خيار `--help` لعرض معلومات الاستخدام والخيارات المتاحة.
    
## كيفية فتح ملف XDELTA

ملفات XDELTA غير مخصصة للفتح المباشر. إذا كنت ترغب في تطبيق تصحيح XDELTA على لعبة أو ملف آخر، فلديك خيار استخدام إما xdelta، المتوافق عبر منصات متعددة، أو xdelta UI، المصمم خصيصًا لمستخدمي Windows.

## مراجع
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)